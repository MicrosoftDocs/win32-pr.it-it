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
# <a name="faq"></a><span data-ttu-id="a7be7-103">Domande frequenti</span><span class="sxs-lookup"><span data-stu-id="a7be7-103">FAQ</span></span>

### <a name="how-do-i-enable-directml-acceleration"></a><span data-ttu-id="a7be7-104">Ricerca per categorie abilitare l'accelerazione DirectML?</span><span class="sxs-lookup"><span data-stu-id="a7be7-104">How do I enable DirectML acceleration?</span></span> 

 
<span data-ttu-id="a7be7-105">Il dispositivo DirectML è abilitato per impostazione predefinita, supponendo che sia disponibile una GPU DirectX 12 appropriata.</span><span class="sxs-lookup"><span data-stu-id="a7be7-105">The DirectML device is enabled by default, assuming you have an appropriate DirectX 12 GPU available.</span></span> <span data-ttu-id="a7be7-106">Se possibile, le operazioni di TensorFlow verranno assegnate automaticamente al dispositivo DirectML.</span><span class="sxs-lookup"><span data-stu-id="a7be7-106">TensorFlow operations will automatically be assigned to the DirectML device if possible.</span></span> 

<span data-ttu-id="a7be7-107">Se si verificano problemi nel determinare se il modello viene eseguito usando l'accelerazione DirectML o meno, è possibile inserire `tf.debugging.set_log_device_placement(True)` come prima istruzione del programma e TensorFlow stamperà le informazioni sul posizionamento dei dispositivi nella console.</span><span class="sxs-lookup"><span data-stu-id="a7be7-107">If you're having trouble determining whether your model is running using DirectML acceleration or not, you can put `tf.debugging.set_log_device_placement(True)` as the first statement of your program and TensorFlow will print device placement information to the console.</span></span>

### <a name="how-do-i-control-device-placement-of-specific-operations"></a><span data-ttu-id="a7be7-108">Ricerca per categorie controllare il posizionamento del dispositivo di operazioni specifiche?</span><span class="sxs-lookup"><span data-stu-id="a7be7-108">How do I control device placement of specific operations?</span></span> 
 

<span data-ttu-id="a7be7-109">Come per qualsiasi altro dispositivo (vedere [la Guida di TensorFlow: usare una GPU](https://www.tensorflow.org/guide/gpu)), è possibile usare `tf.device()` per controllare il dispositivo in cui eseguire.</span><span class="sxs-lookup"><span data-stu-id="a7be7-109">As with any other device (see [TensorFlow Guide: Use a GPU](https://www.tensorflow.org/guide/gpu)), you can use `tf.device()` to control which device to run on.</span></span> 
 

<span data-ttu-id="a7be7-110">La stringa del dispositivo DirectML è `'DML'` .</span><span class="sxs-lookup"><span data-stu-id="a7be7-110">The DirectML device string is `'DML'`.</span></span> 


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

### <a name="i-have-multiple-gpus-how-do-i-select-which-one-is-used-by-directml"></a><span data-ttu-id="a7be7-111">Sono disponibili più GPU.</span><span class="sxs-lookup"><span data-stu-id="a7be7-111">I have multiple GPUs.</span></span> <span data-ttu-id="a7be7-112">Ricerca per categorie selezionare quello utilizzato da DirectML?</span><span class="sxs-lookup"><span data-stu-id="a7be7-112">How do I select which one is used by DirectML?</span></span>

<span data-ttu-id="a7be7-113">È possibile eseguire questa operazione in due modi diversi, a seconda che si desideri controllarlo a livello di processo o per sessione (o entrambi).</span><span class="sxs-lookup"><span data-stu-id="a7be7-113">There are a couple of different ways to do this, depending on whether you want to control it process-wide or per-session (or both).</span></span>

<span data-ttu-id="a7be7-114">Se si vuole controllare quali dispositivi sono visibili a livello di processo di TensorFlow, usare la `DML_VISIBLE_DEVICES` variabile di ambiente.</span><span class="sxs-lookup"><span data-stu-id="a7be7-114">If you want to control which devices are visible to TensorFlow process-wide, use the `DML_VISIBLE_DEVICES` environment variable.</span></span> <span data-ttu-id="a7be7-115">Se si desidera controllarlo per ogni singola sessione, utilizzare `tf.GPUOptions.visible_device_list` .</span><span class="sxs-lookup"><span data-stu-id="a7be7-115">If you want to control it on a per-session basis, use `tf.GPUOptions.visible_device_list`.</span></span>

### <a name="how-do-i-use-the-dml_visible_devices-environment-variable-to-control-which-gpus-get-used-by-directml"></a><span data-ttu-id="a7be7-116">Ricerca per categorie usare la `DML_VISIBLE_DEVICES` variabile di ambiente per controllare quali GPU vengono usate da DirectML?</span><span class="sxs-lookup"><span data-stu-id="a7be7-116">How do I use the `DML_VISIBLE_DEVICES` environment variable to control which GPU(s) get used by DirectML?</span></span>

<span data-ttu-id="a7be7-117">TensorFlow con DirectML supporta una `DML_VISIBLE_DEVICES` variabile di ambiente, che assume la forma di un elenco delimitato da virgole di ID dispositivo (noti anche come "indici Adapter"). Quando è impostato, solo gli ID dispositivo in tale elenco saranno visibili per TensorFlow a livello di processo.</span><span class="sxs-lookup"><span data-stu-id="a7be7-117">TensorFlow with DirectML supports a `DML_VISIBLE_DEVICES` environment variable, which takes the form of a comma-separated list of device IDs (also known as "adapter indices".) When set, only the device IDs in that list will be visible to TensorFlow process-wide.</span></span> <span data-ttu-id="a7be7-118">I dispositivi esclusi usando `DML_VISIBLE_DEVICES` non verranno visualizzati nell'elenco dei dispositivi fisici disponibili per TensorFlow.</span><span class="sxs-lookup"><span data-stu-id="a7be7-118">Devices excluded using `DML_VISIBLE_DEVICES` will not appear in the list of physical devices available to TensorFlow.</span></span>

```python
import tensorflow as tf
tf.debugging.set_log_device_placement(True)
tf.enable_eager_execution()

a = tf.constant([1.])
b = tf.constant([2.])
c = tf.add(a, b)
print(c)
```

<span data-ttu-id="a7be7-119">Di seguito è riportato un esempio di output **senza** `DML_VISIBLE_DEVICES` set:</span><span class="sxs-lookup"><span data-stu-id="a7be7-119">Here is example output **without** `DML_VISIBLE_DEVICES` set:</span></span>

```
DirectML device enumeration: found 2 compatible adapters.
DirectML: creating device on adapter 0 (NVIDIA TITAN V)
DirectML: creating device on adapter 1 (AMD Radeon RX 5700 XT)
Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0
tf.Tensor([3.], shape=(1,), dtype=float32)
```

<span data-ttu-id="a7be7-120">Con `DML_VISIBLE_DEVICES="1"`:</span><span class="sxs-lookup"><span data-stu-id="a7be7-120">With `DML_VISIBLE_DEVICES="1"`:</span></span>

```
DirectML device enumeration: found 1 compatible adapters.
DirectML: creating device on adapter 0 (AMD Radeon RX 5700 XT)
Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0
tf.Tensor([3.], shape=(1,), dtype=float32)
```

<span data-ttu-id="a7be7-121">Si noti che limitando i dispositivi visibili solo a index 1 (AMD Radeon RX 5700 XT), TensorFlow ora assegna un ID 0 a questo dispositivo e lo rende il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="a7be7-121">Note that by restricting the visible devices to only index 1 (AMD Radeon RX 5700 XT), TensorFlow now assigns an ID of 0 to this device, and makes it the default.</span></span>

<span data-ttu-id="a7be7-122">È anche possibile riordinare i dispositivi usando questa variabile di ambiente.</span><span class="sxs-lookup"><span data-stu-id="a7be7-122">You may also re-order devices using this environment variable.</span></span> <span data-ttu-id="a7be7-123">Ad esempio, impostando `DML_VISIBLE_DEVICES="1,0"` :</span><span class="sxs-lookup"><span data-stu-id="a7be7-123">For example, setting `DML_VISIBLE_DEVICES="1,0"`:</span></span>

```
DirectML device enumeration: found 2 compatible adapters.
DirectML: creating device on adapter 0 (AMD Radeon RX 5700 XT)
DirectML: creating device on adapter 1 (NVIDIA TITAN V)
Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0
tf.Tensor([3.], shape=(1,), dtype=float32)
```

<span data-ttu-id="a7be7-124">Si noti che le due GPU (NVIDIA TITAN V e AMD Radeon RX 5700 XT) sono ora comunicate.</span><span class="sxs-lookup"><span data-stu-id="a7be7-124">Notice that the two GPUs (NVIDIA TITAN V and AMD Radeon RX 5700 XT) have now switched places.</span></span>

<span data-ttu-id="a7be7-125">Per impedire che dispositivi specifici risultino visibili, è possibile specificare un ID non valido (ad esempio `-1` ) nell'elenco delimitato da virgole.</span><span class="sxs-lookup"><span data-stu-id="a7be7-125">To prevent specific devices from being visible, you can supply an invalid ID (e.g. `-1`) in the comma-separated list.</span></span> <span data-ttu-id="a7be7-126">Tutti gli ID dispositivo dopo la voce non valida vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="a7be7-126">All device IDs after the invalid entry are ignored.</span></span> <span data-ttu-id="a7be7-127">È anche possibile usare questo per disabilitare completamente l'accelerazione DirectML.</span><span class="sxs-lookup"><span data-stu-id="a7be7-127">You can also use this to disable DirectML acceleration altogether.</span></span>

<span data-ttu-id="a7be7-128">`DML_VISIBLE_DEVICES="-1"`:</span><span class="sxs-lookup"><span data-stu-id="a7be7-128">`DML_VISIBLE_DEVICES="-1"`:</span></span>

```
DirectML device enumeration: found 0 compatible adapters.
Executing op Add in device /job:localhost/replica:0/task:0/device:CPU:0
tf.Tensor([3.], shape=(1,), dtype=float32)
```

### <a name="how-do-i-use-the-visible_device_list-session-option-to-control-which-gpus-directml-uses-to-run-the-session"></a><span data-ttu-id="a7be7-129">Ricerca per categorie utilizzare l' `visible_device_list` opzione Session per controllare le GPU utilizzate da DirectML per eseguire la sessione.</span><span class="sxs-lookup"><span data-stu-id="a7be7-129">How do I use the `visible_device_list` session option to control which GPU(s) DirectML uses to run the session?</span></span>

<span data-ttu-id="a7be7-130">Analogamente a `DML_VISIBLE_DEVICES` , è anche possibile impostare una stringa simile per controllare i dispositivi visibili a livello di sessione.</span><span class="sxs-lookup"><span data-stu-id="a7be7-130">Similar to `DML_VISIBLE_DEVICES`, you can also set a similar string to control visible devices at a session level.</span></span> <span data-ttu-id="a7be7-131">L' `visible_device_list` attributo è disponibile nella `GPUOptions` classe quando si crea la sessione TensorFlow.</span><span class="sxs-lookup"><span data-stu-id="a7be7-131">The `visible_device_list` attribute is available on the `GPUOptions` class when creating your TensorFlow session.</span></span>

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

<span data-ttu-id="a7be7-132">Per informazioni dettagliate, vedere le informazioni di [riferimento sull'API GPUOptions di TensorFlow](https://www.tensorflow.org/versions/r1.15/api_docs/python/tf/GPUOptions#visible_device_list) .</span><span class="sxs-lookup"><span data-stu-id="a7be7-132">You can read the [TensorFlow GPUOptions API reference](https://www.tensorflow.org/versions/r1.15/api_docs/python/tf/GPUOptions#visible_device_list) for more details.</span></span>