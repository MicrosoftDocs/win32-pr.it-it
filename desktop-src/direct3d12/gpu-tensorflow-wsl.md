---
title: Tensorflow con DirectML in WSL 2
description: Abilitare TensorFlow con DirectML nel sottosistema Windows per Linux
ms.topic: article
ms.date: 06/17/2020
ms.openlocfilehash: bfd776013e417760d52134d697439be60c5a1ae8
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "106300618"
---
# <a name="enable-tensorflow-with-directml-in-wsl-2"></a>Abilitare TensorFlow con DirectML in WSL 2

Questa versione di anteprima offre agli studenti e ai principianti un modo per iniziare a compilare le informazioni nello spazio di ML sull'hardware esistente usando il pacchetto TensorFlow con DirectML. Al termine della configurazione, gli utenti possono iniziare con i [modelli di esercitazione TensorFlow](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) o i nostri [esempi di DirectML](https://github.com/microsoft/DirectML). 

> [!NOTE]
> Le funzionalità seguenti sono disponibili nelle versioni provvisorie di Windows 10 e sono soggette a modifiche.

## <a name="install-the-latest-windows-insider-dev-channel-build"></a>Installare la versione più recente di Windows Insider dev Channel Build 

Per usare questa versione di anteprima, è necessario [registrarsi al programma Windows Insider](https://insider.windows.com/getting-started/#register). Al termine, seguire [questi instuctions](https://insider.windows.com/getting-started/#install) per installare la build più recente di insider. Quando si scelgono le impostazioni, assicurarsi di selezionare il [canale dev](/windows-insider/flight-hub/#active-development-builds-of-windows-10). 

Per questa anteprima è necessario compilare 20150 o versione successiva. È possibile controllare il numero di versione della build eseguendo `winver` tramite il comando **Run** (tasto logo Windows + R).

## <a name="install-the-preview-gpu-driver"></a>Installare il driver della GPU di anteprima 

Prima di installare il pacchetto TensorFlow con DirectML in WSL 2, è necessario installare i driver dal fornitore hardware della GPU. Questi driver consentono alla GPU Windows di funzionare con WSL 2.

### <a name="amd"></a>AMD 

[Scaricare e installare il driver di anteprima di AMD](https://www.amd.com/en/support/kb/release-notes/rn-rad-win-wsl-support) dal relativo sito Web. Questo driver di anteprima supporta i componenti hardware seguenti: 

* La serie AMD Radeon™ RX e la grafica Radeon™ VII. 
* Grafica della serie AMD Radeon™ Pro. 
* AMD Ryzen™ e Ryzen™ processori PRO con la grafica Radeon™ Vega. 
* AMD Ryzen™ e Ryzen™ processori per dispositivi mobili PRO con la grafica Radeon™ Vega. 

Per un elenco completo dei prodotti AMD compatibili, consultare le note sulla versione di AMD. 

### <a name="intel"></a>Intel 

[Scaricare e installare il driver di anteprima di Intel](https://downloadcenter.intel.com/download/29526) da usare con DirectML dal proprio sito Web. 

### <a name="nvidia"></a>NVIDIA 

[Scaricare e installare il driver di anteprima di NVIDIA](https://developer.nvidia.com/cuda/wsl/download) da usare con DirectML dal proprio sito Web. Per ulteriori informazioni, vedere la pagina relativa alla [GPU di NVIDIA nella pagina del sottosistema Windows per Linux (WSL)](https://developer.nvidia.com/cuda/wsl) .

## <a name="set-up-the-tensorflow-with-directml-preview"></a>Configurare TensorFlow con DirectML Preview 

### <a name="install-wsl-2"></a>Installare WSL 2 

Dopo aver installato il driver precedente, assicurarsi di [abilitare WSL 2](/windows/wsl/install-win10) e [installare una distribuzione basata su glibc](/windows/wsl/install-win10#install-your-linux-distribution-of-choice) (ad esempio Ubuntu o Debian). Per i test, abbiamo usato Ubuntu. Assicurarsi di avere il kernel più recente selezionando **Controlla aggiornamenti** nella sezione **Windows Update** dell'app Impostazioni. 

> [!NOTE]
> Assicurarsi di disporre degli **aggiornamenti di ricezione per altri prodotti Microsoft quando si aggiorna Windows** abilitato. È possibile trovarlo in **Opzioni avanzate** all'interno della sezione **Windows Update** dell'app Impostazioni. 

Per questa anteprima è necessaria una versione del kernel di 4.19.121 o superiore. È possibile controllare il numero di versione eseguendo il comando seguente in PowerShell. 

```
wsl cat /proc/version
```

### <a name="set-up-python-environment"></a>Configurare l'ambiente Python 

Si consiglia di configurare un ambiente Python virtuale all'interno dell'istanza di WSL 2. Sono disponibili molti strumenti che è possibile usare per configurare un ambiente Python virtuale. per queste istruzioni verrà usato [il Miniconda di Anaconda](https://docs.conda.io/en/latest/miniconda.html). Il resto di questa installazione presuppone l'uso di un ambiente miniconda. 

Installare Miniconda seguendo le [indicazioni sul sito di Anaconda](https://conda.io/projects/conda/en/latest/user-guide/install/index.html)oppure eseguendo i comandi seguenti in WSL. 

```
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh 
bash Miniconda3-latest-Linux-x86_64.sh 
```

Dopo l'installazione di Miniconda in WSL, creare un ambiente usando Python denominato "directml" e attivarlo tramite i comandi seguenti. 

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

2020-06-15 11:27:18.323949: I tensorflow/stream_executor/platform/default/dso_loader.cc:60] Successfully opened dynamic library libdirectml.so.ba106a7c621ea741d21598708ee581c11918380 

2020-06-15 11:27:18.337830: I tensorflow/core/common_runtime/eager/execute.cc:571] Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0 

tf.Tensor([4. 6.], shape=(2,), dtype=float32) 
```

## <a name="tensorflow-with-directml-samples-and-feedback"></a>Tensorflow con DirectML esempi e commenti e suggerimenti 

A questo punto si è pronti per iniziare a scoprire di più su ML training. Vedere le [esercitazioni di TensorFlow](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) o gli [esempi](https://github.com/microsoft/DirectML). Questo contenuto è stato usato come convalida per questo pacchetto di anteprima iniziale di TensorFlow con DirectML. 

Se si verificano problemi o si inviano commenti e suggerimenti sul pacchetto TensorFlow con DirectML, [connettersi al team](https://github.com/microsoft/DirectML/issues).
