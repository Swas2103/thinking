# Katana ML Skipper

## Overview

This is a helper library for Katana ML Skipper workflow product. The idea of this library is to wrap all reusable code to simplify and improve workflow implementation.

Supported functionality:

- API to communicate with RabbitMQ for event receiver/producer

## Author

Katana ML, Andrej Baranovskij

## Instructions

Version number should be updated in __init__.py and pyproject.toml

1. Install Poetry

```
pip install poetry
```

2. Add pika library

```
poetry add pika
```

3. Build

```
poetry build
```

4. Publish to TestPyPI

```
poetry publish -r testpypi
```

5. Install from TestPyPI

```
pip install -i https://test.pypi.org/simple/ --extra-index-url https://pypi.org/simple  skipper-lib
```

6. Publish to PyPI

```
poetry publish
```

7. Install from PyPI

```
pip install skipper-lib
```

8. Test imported library from CMD

```
python -m skipper_lib
```

9. Import EventReceiver

```
from skipper_lib.events.event_receiver import EventReceiver
```

10. Import EventProducer

```
from skipper_lib.events.event_producer import EventProducer
```

## Structure

```
.
├── app 
│   ├── queue
│       ├── event_producer.py
│       └── event_receiver.py
│   └── training_service.py
├── main.py
├── README.md
└── requirements.txt
```

## License

Licensed under the Apache License, Version 2.0. Copyright 2020-2021 Katana ML, Andrej Baranovskij. [Copy of the license](https://github.com/katanaml/katana-pipeline/blob/master/LICENSE).