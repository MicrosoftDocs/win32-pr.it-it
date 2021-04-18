---
title: Tensorflow con DirectML in Windows
description: Abilitare TensorFlow con DirectML direttamente in Windows
ms.topic: article
ms.date: 06/17/2020
ms.openlocfilehash: 665ba456d59f09f27a435135468cf71cb6f6f014
ms.sourcegitcommit: 8f3fb56ebad4615389dec5c74d965dec84ad4123
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/22/2020
ms.locfileid: "106299546"
---
# <a name="enable-tensorflow-with-directml-on-windows"></a>Abilitare TensorFlow con DirectML in Windows

Questa versione di anteprima offre a studenti e principianti un modo per iniziare a sviluppare le proprie conoscenze nello spazio di ML sull'hardware esistente usando il pacchetto TensorFlow con DirectML. Al termine della configurazione, gli utenti possono iniziare con i [modelli di esercitazione TensorFlow](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) o [i nostri esempi di DirectML](https://github.com/microsoft/DirectML). 

> [!NOTE]
> La seguente funzionalità è in anteprima e soggetta a modifiche.

## <a name="check-your-version-of-windows"></a>Controllare la versione di Windows 

Il pacchetto TensorFlow con DirectML in Windows nativo funziona a partire da Windows 10 versione 1709 (Build 16299 o successiva). È possibile controllare il numero di versione della build eseguendo `winver` tramite il comando **Run** (tasto logo Windows + R).

## <a name="check-for-gpu-driver-updates"></a>Verifica aggiornamenti driver GPU 

Verificare che sia installato il driver GPU più recente. Selezionare **Verifica disponibilità di aggiornamenti** nella sezione **Windows Update** dell'app Impostazioni.

## <a name="set-up-the-tensorflow-with-directml-preview"></a>Configurare TensorFlow con DirectML Preview 

Si consiglia di configurare un ambiente Python virtuale all'interno di Windows. Sono disponibili molti strumenti che è possibile usare per configurare un ambiente Python virtuale. per queste istruzioni verrà usato [il Miniconda di Anaconda](https://docs.conda.io/en/latest/miniconda.html). Il resto di questa installazione presuppone l'uso di un ambiente miniconda. 

### <a name="set-up-python-environment"></a>Configurare l'ambiente Python 

Scaricare e installare [Miniconda Windows Installer](https://docs.conda.io/en/latest/miniconda.html#windows-installers) nel sistema. Sono disponibili [altre linee guida per l'installazione](https://conda.io/projects/conda/en/latest/user-guide/install/windows.html) nel sito di Anaconda. Dopo aver installato Miniconda, creare un ambiente usando Python denominato **directml** e attivarlo tramite i comandi seguenti. 

> [!NOTE]
> Nei comandi seguenti viene usato Python 3,6. Tuttavia, il pacchetto tensorflow-directml funziona in un ambiente Python 3,5, 3,6 o 3,7. 

```
conda create --name directml python=3.6 

conda activate directml 
```

### <a name="install-the-tensorflow-with-directml-package"></a>Installare il pacchetto Tensorflow con DirectML 

Installare il pacchetto di TensorFlow con un back-end DirectML tramite PIP eseguendo il comando seguente.

> [!NOTE]
> Il pacchetto tensorflow-directml supporta solo TensorFlow 1,15. 

```
pip install tensorflow-directml
```

Dopo aver installato il pacchetto tensorflow-directml, è possibile verificare che venga eseguito correttamente aggiungendo due tensori. Copiare le righe seguenti in una sessione interattiva di Python. 

```
import tensorflow.compat.v1 as tf 

tf.enable_eager_execution(tf.ConfigProto(log_device_placement=True)) 

print(tf.add([1.0, 2.0], [3.0, 4.0])) 
```

Verrà visualizzato un output simile al seguente, con l'operatore Add inserito sul dispositivo DML. 

```
2020-06-15 11:27:18.235973: I tensorflow/core/common_runtime/dml/dml_device_factory.cc:45] DirectML device enumeration: found 1 compatible adapters. 

2020-06-15 11:27:18.240065: I tensorflow/core/common_runtime/dml/dml_device_factory.cc:32] DirectML: creating device on adapter 0 (AMD Radeon VII) 

2020-06-15 11:27:18.323949: I tensorflow/stream_executor/platform/default/dso_loader.cc:60] Successfully opened dynamic library DirectMLba106a7c621ea741d2159d8708ee581c11918380.dll 

2020-06-15 11:27:18.337830: I tensorflow/core/common_runtime/eager/execute.cc:571] Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0 

tf.Tensor([4. 6.], shape=(2,), dtype=float32) 
```

## <a name="tensorflow-with-directml-samples-and-feedback"></a>Tensorflow con DirectML esempi e commenti e suggerimenti 

A questo punto si è pronti per iniziare a scoprire di più su ML training. Vedere le [esercitazioni di TensorFlow](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) o gli [esempi](https://github.com/microsoft/DirectML). Questo contenuto è stato usato come convalida per questo pacchetto di anteprima iniziale di TensorFlow con un back-end DirectML. 

Se si verificano problemi o si inviano commenti e suggerimenti sul pacchetto TensorFlow con DirectML, [connettersi al team](https://github.com/microsoft/DirectML/issues). 
