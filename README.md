# Spring Boot Jaeger Example

**Objective:**
Implement a Jaeger logging system to facilitate tracing and monitoring within a distributed system architecture.

**Components:**

1. **Jaeger Tracer:**
   - Set up a Jaeger Tracer instance to trace the flow of requests through the distributed system.
   - Configure the tracer to collect and propagate trace information across different microservices.

2. **Instrumentation:**
   - Instrument each microservice with Jaeger client libraries to generate and propagate trace data.
   - Ensure that incoming requests are tagged with unique trace IDs and that these IDs are propagated across all subsequent service calls.

3. **Integration with Logging Infrastructure:**
   - Integrate Jaeger with existing logging infrastructure (e.g., ELK stack, Prometheus/Grafana) to visualize and analyze trace data alongside other system metrics.
   - Configure Jaeger to export trace data to the desired backend for long-term storage and analysis.

4. **Monitoring and Alerting:**
   - Set up alerts based on predefined thresholds for latency, error rates, or other relevant metrics derived from trace data.
   - Use Jaeger's query capabilities to create dashboards for real-time monitoring of request flow and performance.

5. **Documentation and Training:**
   - Provide comprehensive documentation on how to use the Jaeger logging system for developers, operations teams, and other stakeholders.
   - Conduct training sessions to familiarize team members with Jaeger's features and best practices for effective tracing and monitoring.

**Benefits:**
- **Visibility:** Gain insights into the flow of requests across distributed systems, allowing for better understanding and troubleshooting of complex interactions.
- **Performance Optimization:** Identify performance bottlenecks, latency issues, and areas for optimization by analyzing trace data.
- **Troubleshooting:** Facilitate faster resolution of issues by correlating trace data with logs and system metrics.
- **Scalability:** Scale the Jaeger infrastructure alongside the distributed system to handle increased tracing load as the system grows.

![Jaeger Architecture](https://www.jaegertracing.io/img/architecture-v1.png)

## Jaeger Setup
- Start Jaeger using Docker

docker run -d --name jaeger-ui -p 16686:16686 -p 6831:6831/udp jaegertracing/all-in-one:1.9

- Accessible at - http://localhost:16686/

## Endpoints
- /jaeger/client/{id} - Exposed in jaeger-client
- /jaeger/client/{id} - Exposed in jaeger-server. Connects to numbers api - numbersapi.com
