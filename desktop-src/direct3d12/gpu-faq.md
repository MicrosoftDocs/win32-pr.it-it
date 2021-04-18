---
title: 'Accelerazione GPU in WSL - Domande frequenti '
description: Domande frequenti sull'accelerazione GPU nel sottosistema Windows per Linux
ms.topic: article
ms.date: 09/28/2020
ms.openlocfilehash: 7c55a8c06bd2b62c670cbf532bc3aa65ddd919d7
ms.sourcegitcommit: f58718691e8b989650108b8c70aaa471d17bf3aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/08/2020
ms.locfileid: "106300646"
---
# <a name="faq"></a>Domande frequenti

### <a name="how-do-i-enable-directml-acceleration"></a>Ricerca per categorie abilitare l'accelerazione DirectML? 

 
Il dispositivo DirectML è abilitato per impostazione predefinita, supponendo che sia disponibile una GPU DirectX 12 appropriata. Se possibile, le operazioni di TensorFlow verranno assegnate automaticamente al dispositivo DirectML. 

Se si verificano problemi nel determinare se il modello viene eseguito usando l'accelerazione DirectML o meno, è possibile inserire `tf.debugging.set_log_device_placement(True)` come prima istruzione del programma e TensorFlow stamperà le informazioni sul posizionamento dei dispositivi nella console.

### <a name="how-do-i-control-device-placement-of-specific-operations"></a>Ricerca per categorie controllare il posizionamento del dispositivo di operazioni specifiche? 
 

Come per qualsiasi altro dispositivo (vedere [la Guida di TensorFlow: usare una GPU](https://www.tensorflow.org/guide/gpu)), è possibile usare `tf.device()` per controllare il dispositivo in cui eseguire. 
 

La stringa del dispositivo DirectML è `'DML'` . 


```python 

import tensorflow as tf 

tf.debugging.set_log_device_placement(True) 

tf.enable_eager_execution() 

 

# Explicitly place tensors on the DirectML device 

with tf.device('/DML:0'): 

  a = tf.constant([1.0, 2.0, 3.0]) 

  b = tf.constant([4.0, 5.0, 6.0]) 

 

c = tf.add(a, b) 

print(c) 

``` 


``` 

Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0 

tf.Tensor([5. 7. 9.], shape=(3,), dtype=float32) 

```

### <a name="i-have-multiple-gpus-how-do-i-select-which-one-is-used-by-directml"></a>Sono disponibili più GPU. Ricerca per categorie selezionare quello utilizzato da DirectML?

È possibile eseguire questa operazione in due modi diversi, a seconda che si desideri controllarlo a livello di processo o per sessione (o entrambi).

Se si vuole controllare quali dispositivi sono visibili a livello di processo di TensorFlow, usare la `DML_VISIBLE_DEVICES` variabile di ambiente. Se si desidera controllarlo per ogni singola sessione, utilizzare `tf.GPUOptions.visible_device_list` .

### <a name="how-do-i-use-the-dml_visible_devices-environment-variable-to-control-which-gpus-get-used-by-directml"></a>Ricerca per categorie usare la `DML_VISIBLE_DEVICES` variabile di ambiente per controllare quali GPU vengono usate da DirectML?

TensorFlow con DirectML supporta una `DML_VISIBLE_DEVICES` variabile di ambiente, che assume la forma di un elenco delimitato da virgole di ID dispositivo (noti anche come "indici Adapter"). Quando è impostato, solo gli ID dispositivo in tale elenco saranno visibili per TensorFlow a livello di processo. I dispositivi esclusi usando `DML_VISIBLE_DEVICES` non verranno visualizzati nell'elenco dei dispositivi fisici disponibili per TensorFlow.

```python
import tensorflow as tf
tf.debugging.set_log_device_placement(True)
tf.enable_eager_execution()

a = tf.constant([1.])
b = tf.constant([2.])
c = tf.add(a, b)
print(c)
```

Di seguito è riportato un esempio di output **senza** `DML_VISIBLE_DEVICES` set:

```
DirectML device enumeration: found 2 compatible adapters.
DirectML: creating device on adapter 0 (NVIDIA TITAN V)
DirectML: creating device on adapter 1 (AMD Radeon RX 5700 XT)
Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0
tf.Tensor([3.], shape=(1,), dtype=float32)
```

Con `DML_VISIBLE_DEVICES="1"`:

```
DirectML device enumeration: found 1 compatible adapters.
DirectML: creating device on adapter 0 (AMD Radeon RX 5700 XT)
Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0
tf.Tensor([3.], shape=(1,), dtype=float32)
```

Si noti che limitando i dispositivi visibili solo a index 1 (AMD Radeon RX 5700 XT), TensorFlow ora assegna un ID 0 a questo dispositivo e lo rende il valore predefinito.

È anche possibile riordinare i dispositivi usando questa variabile di ambiente. Ad esempio, impostando `DML_VISIBLE_DEVICES="1,0"` :

```
DirectML device enumeration: found 2 compatible adapters.
DirectML: creating device on adapter 0 (AMD Radeon RX 5700 XT)
DirectML: creating device on adapter 1 (NVIDIA TITAN V)
Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0
tf.Tensor([3.], shape=(1,), dtype=float32)
```

Si noti che le due GPU (NVIDIA TITAN V e AMD Radeon RX 5700 XT) sono ora comunicate.

Per impedire che dispositivi specifici risultino visibili, è possibile specificare un ID non valido (ad esempio `-1` ) nell'elenco delimitato da virgole. Tutti gli ID dispositivo dopo la voce non valida vengono ignorati. È anche possibile usare questo per disabilitare completamente l'accelerazione DirectML.

`DML_VISIBLE_DEVICES="-1"`:

```
DirectML device enumeration: found 0 compatible adapters.
Executing op Add in device /job:localhost/replica:0/task:0/device:CPU:0
tf.Tensor([3.], shape=(1,), dtype=float32)
```

### <a name="how-do-i-use-the-visible_device_list-session-option-to-control-which-gpus-directml-uses-to-run-the-session"></a>Ricerca per categorie utilizzare l' `visible_device_list` opzione Session per controllare le GPU utilizzate da DirectML per eseguire la sessione.

Analogamente a `DML_VISIBLE_DEVICES` , è anche possibile impostare una stringa simile per controllare i dispositivi visibili a livello di sessione. L' `visible_device_list` attributo è disponibile nella `GPUOptions` classe quando si crea la sessione TensorFlow.

```python
import tensorflow as tf

a = tf.constant([1.])
b = tf.constant([2.])
c = tf.add(a, b)

gpu_config = tf.GPUOptions()
gpu_config.visible_device_list = "1"

session = tf.Session(config=tf.ConfigProto(gpu_options=gpu_config))
print(session.run(c))
```

```
DirectML device enumeration: found 2 compatible adapters.
DirectML: creating device on adapter 1 (AMD Radeon RX 5700 XT)
[3.]
```

Per informazioni dettagliate, vedere le informazioni di [riferimento sull'API GPUOptions di TensorFlow](https://www.tensorflow.org/versions/r1.15/api_docs/python/tf/GPUOptions#visible_device_list) .