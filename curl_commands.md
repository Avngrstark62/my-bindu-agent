curl -X POST http://localhost:3773/ \
  -H "Content-Type: application/json" \
  -d '{
    "jsonrpc": "2.0",
    "method": "message/send",
    "params": {
      "message": {
        "role": "user",
        "parts": [
          {
            "kind": "text",
            "text": "Hello, what can you help me with?"
          }
        ],
        "kind": "message",
        "messageId": "550e8400-e29b-41d4-a716-446655440038",
        "contextId": "550e8400-e29b-41d4-a716-446655440038",
        "taskId": "550e8400-e29b-41d4-a716-446655440078"
      },
      "configuration": {
        "acceptedOutputModes": ["application/json"]
      }
    },
    "id": "550e8400-e29b-41d4-a716-446655440024"
  }'
  
  
  -----------------------------
  
  
  curl -X POST http://localhost:3773/ \
  -H "Content-Type: application/json" \
  -d '{
    "jsonrpc": "2.0",
    "method": "tasks/feedback",
    "params": {
      "taskId": "550e8400-e29b-41d4-a716-446655440075",
      "feedback": "Great",
      "rating": 5,
      "metadata": {
      }
    },
    "id": "550e8400-e29b-41d4-a716-446655440021"
  }'
  
  
  
  -----------------------------
  
  curl -X POST http://localhost:3773/ \
  -H "Content-Type: application/json" \
  -d '{
    "jsonrpc": "2.0",
    "method": "tasks/get",
    "params": {
      "taskId": "550e8400-e29b-41d4-a716-446655440078"
    },
    "id": "550e8400-e29b-41d4-a716-446655440014"
  }'
