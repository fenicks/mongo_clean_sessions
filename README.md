# mongo_clean_sessions
Utility program to cleanup MongoDB collection by a specific time field. 

## Usage

    Usage of ./main:
      -c string
            MongoDB collection to cleanup. (default "sessions")
      -f string
            MongoDB collection field with type 'time.Time'. (default "updated_at")
      -r int
            MongoDB retention delai in hour(s). Default is 7 days (168 hours).
      -url string
            MongoDB connection URI. (default "mongodb://localhost:27017/test")

## Example

    ./main -url=${MONGOLAB_URL} -c=sessions -f=updated_at -r=72
