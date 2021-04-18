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
# <a name="enable-tensorflow-with-directml-on-windows"></a><span data-ttu-id="2a3b2-103">Abilitare TensorFlow con DirectML in Windows</span><span class="sxs-lookup"><span data-stu-id="2a3b2-103">Enable TensorFlow with DirectML on Windows</span></span>

<span data-ttu-id="2a3b2-104">Questa versione di anteprima offre a studenti e principianti un modo per iniziare a sviluppare le proprie conoscenze nello spazio di ML sull'hardware esistente usando il pacchetto TensorFlow con DirectML.</span><span class="sxs-lookup"><span data-stu-id="2a3b2-104">This preview provides students and beginners a way to start building their knowledge in the ML space on their existing hardware by using the the TensorFlow with DirectML package.</span></span> <span data-ttu-id="2a3b2-105">Al termine della configurazione, gli utenti possono iniziare con i [modelli di esercitazione TensorFlow](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) o [i nostri esempi di DirectML](https://github.com/microsoft/DirectML).</span><span class="sxs-lookup"><span data-stu-id="2a3b2-105">Once set up, users can start with the [TensorFlow tutorial models](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) or [our DirectML samples](https://github.com/microsoft/DirectML).</span></span> 

> [!NOTE]
> <span data-ttu-id="2a3b2-106">La seguente funzionalità è in anteprima e soggetta a modifiche.</span><span class="sxs-lookup"><span data-stu-id="2a3b2-106">The following feature is in preview, and are subject to change.</span></span>

## <a name="check-your-version-of-windows"></a><span data-ttu-id="2a3b2-107">Controllare la versione di Windows</span><span class="sxs-lookup"><span data-stu-id="2a3b2-107">Check your version of Windows</span></span> 

<span data-ttu-id="2a3b2-108">Il pacchetto TensorFlow con DirectML in Windows nativo funziona a partire da Windows 10 versione 1709 (Build 16299 o successiva).</span><span class="sxs-lookup"><span data-stu-id="2a3b2-108">The TensorFlow with DirectML package on native Windows works starting with Windows 10 Version 1709 (Build 16299 or higher).</span></span> <span data-ttu-id="2a3b2-109">È possibile controllare il numero di versione della build eseguendo `winver` tramite il comando **Run** (tasto logo Windows + R).</span><span class="sxs-lookup"><span data-stu-id="2a3b2-109">You can check your build version number by running `winver` via the **Run** command (Windows logo key + R).</span></span>

## <a name="check-for-gpu-driver-updates"></a><span data-ttu-id="2a3b2-110">Verifica aggiornamenti driver GPU</span><span class="sxs-lookup"><span data-stu-id="2a3b2-110">Check for GPU driver updates</span></span> 

<span data-ttu-id="2a3b2-111">Verificare che sia installato il driver GPU più recente.</span><span class="sxs-lookup"><span data-stu-id="2a3b2-111">Ensure you have the latest GPU driver installed.</span></span> <span data-ttu-id="2a3b2-112">Selezionare **Verifica disponibilità di aggiornamenti** nella sezione **Windows Update** dell'app Impostazioni.</span><span class="sxs-lookup"><span data-stu-id="2a3b2-112">Select **Check for updates** in the **Windows Update** section of the Settings app.</span></span>

## <a name="set-up-the-tensorflow-with-directml-preview"></a><span data-ttu-id="2a3b2-113">Configurare TensorFlow con DirectML Preview</span><span class="sxs-lookup"><span data-stu-id="2a3b2-113">Set up the TensorFlow with DirectML preview</span></span> 

<span data-ttu-id="2a3b2-114">Si consiglia di configurare un ambiente Python virtuale all'interno di Windows.</span><span class="sxs-lookup"><span data-stu-id="2a3b2-114">We recommend setting up a virtual Python environment inside Windows.</span></span> <span data-ttu-id="2a3b2-115">Sono disponibili molti strumenti che è possibile usare per configurare un ambiente Python virtuale. per queste istruzioni verrà usato [il Miniconda di Anaconda](https://docs.conda.io/en/latest/miniconda.html).</span><span class="sxs-lookup"><span data-stu-id="2a3b2-115">There are many tools you can use to setup a virtual Python environment — for these instructions, we'll use [Anaconda’s Miniconda](https://docs.conda.io/en/latest/miniconda.html).</span></span> <span data-ttu-id="2a3b2-116">Il resto di questa installazione presuppone l'uso di un ambiente miniconda.</span><span class="sxs-lookup"><span data-stu-id="2a3b2-116">The rest of this setup assumes you use a miniconda environment.</span></span> 

### <a name="set-up-python-environment"></a><span data-ttu-id="2a3b2-117">Configurare l'ambiente Python</span><span class="sxs-lookup"><span data-stu-id="2a3b2-117">Set up Python environment</span></span> 

<span data-ttu-id="2a3b2-118">Scaricare e installare [Miniconda Windows Installer](https://docs.conda.io/en/latest/miniconda.html#windows-installers) nel sistema.</span><span class="sxs-lookup"><span data-stu-id="2a3b2-118">Download and install the [Miniconda Windows installer](https://docs.conda.io/en/latest/miniconda.html#windows-installers) on your system.</span></span> <span data-ttu-id="2a3b2-119">Sono disponibili [altre linee guida per l'installazione](https://conda.io/projects/conda/en/latest/user-guide/install/windows.html) nel sito di Anaconda.</span><span class="sxs-lookup"><span data-stu-id="2a3b2-119">There is [additional guidance for setup](https://conda.io/projects/conda/en/latest/user-guide/install/windows.html) on Anaconda’s site.</span></span> <span data-ttu-id="2a3b2-120">Dopo aver installato Miniconda, creare un ambiente usando Python denominato **directml** e attivarlo tramite i comandi seguenti.</span><span class="sxs-lookup"><span data-stu-id="2a3b2-120">Once Miniconda is installed, create an environment using Python named **directml** and activate it through the following commands.</span></span> 

> [!NOTE]
> <span data-ttu-id="2a3b2-121">Nei comandi seguenti viene usato Python 3,6.</span><span class="sxs-lookup"><span data-stu-id="2a3b2-121">In the commands below, we use Python 3.6.</span></span> <span data-ttu-id="2a3b2-122">Tuttavia, il pacchetto tensorflow-directml funziona in un ambiente Python 3,5, 3,6 o 3,7.</span><span class="sxs-lookup"><span data-stu-id="2a3b2-122">However, the tensorflow-directml package works in a Python 3.5, 3.6 or 3.7 environment.</span></span> 

```
conda create --name directml python=3.6 

conda activate directml 
```

### <a name="install-the-tensorflow-with-directml-package"></a><span data-ttu-id="2a3b2-123">Installare il pacchetto Tensorflow con DirectML</span><span class="sxs-lookup"><span data-stu-id="2a3b2-123">Install the Tensorflow with DirectML package</span></span> 

<span data-ttu-id="2a3b2-124">Installare il pacchetto di TensorFlow con un back-end DirectML tramite PIP eseguendo il comando seguente.</span><span class="sxs-lookup"><span data-stu-id="2a3b2-124">Install the package of TensorFlow with a DirectML backend through pip by running the following command.</span></span>

> [!NOTE]
> <span data-ttu-id="2a3b2-125">Il pacchetto tensorflow-directml supporta solo TensorFlow 1,15.</span><span class="sxs-lookup"><span data-stu-id="2a3b2-125">The tensorflow-directml package only supports TensorFlow 1.15.</span></span> 

```
pip install tensorflow-directml
```

<span data-ttu-id="2a3b2-126">Dopo aver installato il pacchetto tensorflow-directml, è possibile verificare che venga eseguito correttamente aggiungendo due tensori.</span><span class="sxs-lookup"><span data-stu-id="2a3b2-126">Once you’ve installed the tensorflow-directml package, you can verify that it runs correctly by adding two tensors.</span></span> <span data-ttu-id="2a3b2-127">Copiare le righe seguenti in una sessione interattiva di Python.</span><span class="sxs-lookup"><span data-stu-id="2a3b2-127">Copy the following lines into an interactive Python session.</span></span> 

```
import tensorflow.compat.v1 as tf 

tf.enable_eager_execution(tf.ConfigProto(log_device_placement=True)) 

print(tf.add([1.0, 2.0], [3.0, 4.0])) 
```

<span data-ttu-id="2a3b2-128">Verrà visualizzato un output simile al seguente, con l'operatore Add inserito sul dispositivo DML.</span><span class="sxs-lookup"><span data-stu-id="2a3b2-128">You should see output similar to the following, with the add operator placed on the DML device.</span></span> 

```
2020-06-15 11:27:18.235973: I tensorflow/core/common_runtime/dml/dml_device_factory.cc:45] DirectML device enumeration: found 1 compatible adapters. 

2020-06-15 11:27:18.240065: I tensorflow/core/common_runtime/dml/dml_device_factory.cc:32] DirectML: creating device on adapter 0 (AMD Radeon VII) 

2020-06-15 11:27:18.323949: I tensorflow/stream_executor/platform/default/dso_loader.cc:60] Successfully opened dynamic library DirectMLba106a7c621ea741d2159d8708ee581c11918380.dll 

2020-06-15 11:27:18.337830: I tensorflow/core/common_runtime/eager/execute.cc:571] Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0 

tf.Tensor([4. 6.], shape=(2,), dtype=float32) 
```

## <a name="tensorflow-with-directml-samples-and-feedback"></a><span data-ttu-id="2a3b2-129">Tensorflow con DirectML esempi e commenti e suggerimenti</span><span class="sxs-lookup"><span data-stu-id="2a3b2-129">Tensorflow with DirectML samples and feedback</span></span> 

<span data-ttu-id="2a3b2-130">A questo punto si è pronti per iniziare a scoprire di più su ML training.</span><span class="sxs-lookup"><span data-stu-id="2a3b2-130">Now you’re ready to start learning more about ML training.</span></span> <span data-ttu-id="2a3b2-131">Vedere le [esercitazioni di TensorFlow](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) o gli [esempi](https://github.com/microsoft/DirectML).</span><span class="sxs-lookup"><span data-stu-id="2a3b2-131">Check out the [TensorFlow tutorials](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) or [our samples](https://github.com/microsoft/DirectML).</span></span> <span data-ttu-id="2a3b2-132">Questo contenuto è stato usato come convalida per questo pacchetto di anteprima iniziale di TensorFlow con un back-end DirectML.</span><span class="sxs-lookup"><span data-stu-id="2a3b2-132">We used this content as validation for this initial preview package of TensorFlow with a DirectML backend.</span></span> 

<span data-ttu-id="2a3b2-133">Se si verificano problemi o si inviano commenti e suggerimenti sul pacchetto TensorFlow con DirectML, [connettersi al team](https://github.com/microsoft/DirectML/issues).</span><span class="sxs-lookup"><span data-stu-id="2a3b2-133">If you run into issues or have feedback on the TensorFlow with DirectML package, please [connect with our team here](https://github.com/microsoft/DirectML/issues).</span></span> 
