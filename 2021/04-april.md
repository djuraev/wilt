### April Log
#### Never Stop learning, be better than "yesterday you"

## 04-02
* Add  dependency from local(folder) in Spring project. 
     * First, add ```.jar``` file (library) to source folder (i.e. src/libs)
     * Then, edit ```build.gradle``` file as follows: <i>compile fileTree(dir: 'libs', include:[*.jar]</i>


## 04-06
* How to set Spring WebClient ```@LoadBalanced``` (Support @LoadBalanced WebClient)
     * As ```RestTemplate``` is different from ```WebClient``` in Spring (Reactive), WebClient @LoadBalanced is used differently.
     * While surfing internet to find solution I came accross this solution. It worked for me.
     * Add current @Bean configuration to your source code(i.e. SpringBootApplication file)
     ``` @Bean
          @LoadBalanced
          public WebClient.Builder loadBalancedWebClientBuilder() {
               return WebClient.builder();
          } 

    * Now you can you use WebClient like this.
         Flux responce = webClientBuilder.build()
                                         .get()
                                         .uri("http://your.service/endpoint/{id}", id)
                                         .retrieve()
                                         .bodyToFlux(Entity.class); 