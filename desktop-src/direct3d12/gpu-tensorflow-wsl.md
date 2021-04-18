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
# <a name="enable-tensorflow-with-directml-in-wsl-2"></a><span data-ttu-id="0b80c-103">Abilitare TensorFlow con DirectML in WSL 2</span><span class="sxs-lookup"><span data-stu-id="0b80c-103">Enable TensorFlow with DirectML in WSL 2</span></span>

<span data-ttu-id="0b80c-104">Questa versione di anteprima offre agli studenti e ai principianti un modo per iniziare a compilare le informazioni nello spazio di ML sull'hardware esistente usando il pacchetto TensorFlow con DirectML.</span><span class="sxs-lookup"><span data-stu-id="0b80c-104">This preview provides students and beginners a way to start building knowledge in the ML space on their existing hardware by using the TensorFlow with DirectML package.</span></span> <span data-ttu-id="0b80c-105">Al termine della configurazione, gli utenti possono iniziare con i [modelli di esercitazione TensorFlow](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) o i nostri [esempi di DirectML](https://github.com/microsoft/DirectML).</span><span class="sxs-lookup"><span data-stu-id="0b80c-105">Once set up, users can start with the [TensorFlow tutorial models](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) or our [DirectML samples](https://github.com/microsoft/DirectML).</span></span> 

> [!NOTE]
> <span data-ttu-id="0b80c-106">Le funzionalità seguenti sono disponibili nelle versioni provvisorie di Windows 10 e sono soggette a modifiche.</span><span class="sxs-lookup"><span data-stu-id="0b80c-106">The following features are available in prerelease versions of Windows 10, and are subject to change.</span></span>

## <a name="install-the-latest-windows-insider-dev-channel-build"></a><span data-ttu-id="0b80c-107">Installare la versione più recente di Windows Insider dev Channel Build</span><span class="sxs-lookup"><span data-stu-id="0b80c-107">Install the latest Windows Insider Dev Channel build</span></span> 

<span data-ttu-id="0b80c-108">Per usare questa versione di anteprima, è necessario [registrarsi al programma Windows Insider](https://insider.windows.com/getting-started/#register).</span><span class="sxs-lookup"><span data-stu-id="0b80c-108">To use this preview, you'll need to [register for the Windows Insider Program](https://insider.windows.com/getting-started/#register).</span></span> <span data-ttu-id="0b80c-109">Al termine, seguire [questi instuctions](https://insider.windows.com/getting-started/#install) per installare la build più recente di insider.</span><span class="sxs-lookup"><span data-stu-id="0b80c-109">Once you do, follow [these instuctions](https://insider.windows.com/getting-started/#install) to install the latest insider build.</span></span> <span data-ttu-id="0b80c-110">Quando si scelgono le impostazioni, assicurarsi di selezionare il [canale dev](/windows-insider/flight-hub/#active-development-builds-of-windows-10).</span><span class="sxs-lookup"><span data-stu-id="0b80c-110">When choosing your settings, ensure you're selecting the [Dev Channel](/windows-insider/flight-hub/#active-development-builds-of-windows-10).</span></span> 

<span data-ttu-id="0b80c-111">Per questa anteprima è necessario compilare 20150 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="0b80c-111">For this preview, you need Build 20150 or higher.</span></span> <span data-ttu-id="0b80c-112">È possibile controllare il numero di versione della build eseguendo `winver` tramite il comando **Run** (tasto logo Windows + R).</span><span class="sxs-lookup"><span data-stu-id="0b80c-112">You can check your build version number by running `winver` via the **Run** command (Windows logo key + R).</span></span>

## <a name="install-the-preview-gpu-driver"></a><span data-ttu-id="0b80c-113">Installare il driver della GPU di anteprima</span><span class="sxs-lookup"><span data-stu-id="0b80c-113">Install the preview GPU driver</span></span> 

<span data-ttu-id="0b80c-114">Prima di installare il pacchetto TensorFlow con DirectML in WSL 2, è necessario installare i driver dal fornitore hardware della GPU.</span><span class="sxs-lookup"><span data-stu-id="0b80c-114">Before installing the TensorFlow with DirectML package inside WSL 2, you need to install drivers from your GPU hardware vendor.</span></span> <span data-ttu-id="0b80c-115">Questi driver consentono alla GPU Windows di funzionare con WSL 2.</span><span class="sxs-lookup"><span data-stu-id="0b80c-115">These drivers enable the Windows GPU to work with WSL 2.</span></span>

### <a name="amd"></a><span data-ttu-id="0b80c-116">AMD</span><span class="sxs-lookup"><span data-stu-id="0b80c-116">AMD</span></span> 

<span data-ttu-id="0b80c-117">[Scaricare e installare il driver di anteprima di AMD](https://www.amd.com/en/support/kb/release-notes/rn-rad-win-wsl-support) dal relativo sito Web.</span><span class="sxs-lookup"><span data-stu-id="0b80c-117">[Download and install AMD’s preview driver](https://www.amd.com/en/support/kb/release-notes/rn-rad-win-wsl-support) from their website.</span></span> <span data-ttu-id="0b80c-118">Questo driver di anteprima supporta i componenti hardware seguenti:</span><span class="sxs-lookup"><span data-stu-id="0b80c-118">This preview driver supports the following hardware:</span></span> 

* <span data-ttu-id="0b80c-119">La serie AMD Radeon™ RX e la grafica Radeon™ VII.</span><span class="sxs-lookup"><span data-stu-id="0b80c-119">AMD Radeon™ RX series and Radeon™ VII graphics.</span></span> 
* <span data-ttu-id="0b80c-120">Grafica della serie AMD Radeon™ Pro.</span><span class="sxs-lookup"><span data-stu-id="0b80c-120">AMD Radeon™ Pro series graphics.</span></span> 
* <span data-ttu-id="0b80c-121">AMD Ryzen™ e Ryzen™ processori PRO con la grafica Radeon™ Vega.</span><span class="sxs-lookup"><span data-stu-id="0b80c-121">AMD Ryzen™ and Ryzen™ PRO Processors with Radeon™ Vega graphics.</span></span> 
* <span data-ttu-id="0b80c-122">AMD Ryzen™ e Ryzen™ processori per dispositivi mobili PRO con la grafica Radeon™ Vega.</span><span class="sxs-lookup"><span data-stu-id="0b80c-122">AMD Ryzen™ and Ryzen™ PRO Mobile Processors with Radeon™ Vega graphics.</span></span> 

<span data-ttu-id="0b80c-123">Per un elenco completo dei prodotti AMD compatibili, consultare le note sulla versione di AMD.</span><span class="sxs-lookup"><span data-stu-id="0b80c-123">For a complete list of compatible AMD products, please refer to the AMD Release Notes.</span></span> 

### <a name="intel"></a><span data-ttu-id="0b80c-124">Intel</span><span class="sxs-lookup"><span data-stu-id="0b80c-124">Intel</span></span> 

<span data-ttu-id="0b80c-125">[Scaricare e installare il driver di anteprima di Intel](https://downloadcenter.intel.com/download/29526) da usare con DirectML dal proprio sito Web.</span><span class="sxs-lookup"><span data-stu-id="0b80c-125">[Download and install Intel’s preview driver](https://downloadcenter.intel.com/download/29526) to use with DirectML from their website.</span></span> 

### <a name="nvidia"></a><span data-ttu-id="0b80c-126">NVIDIA</span><span class="sxs-lookup"><span data-stu-id="0b80c-126">NVIDIA</span></span> 

<span data-ttu-id="0b80c-127">[Scaricare e installare il driver di anteprima di NVIDIA](https://developer.nvidia.com/cuda/wsl/download) da usare con DirectML dal proprio sito Web.</span><span class="sxs-lookup"><span data-stu-id="0b80c-127">[Download and install NVIDIA's preview driver](https://developer.nvidia.com/cuda/wsl/download) to use with DirectML from their website.</span></span> <span data-ttu-id="0b80c-128">Per ulteriori informazioni, vedere la pagina relativa alla [GPU di NVIDIA nella pagina del sottosistema Windows per Linux (WSL)](https://developer.nvidia.com/cuda/wsl) .</span><span class="sxs-lookup"><span data-stu-id="0b80c-128">For more information, see [NVIDIA's GPU in Windows Subsystem for Linux (WSL)](https://developer.nvidia.com/cuda/wsl) page.</span></span>

## <a name="set-up-the-tensorflow-with-directml-preview"></a><span data-ttu-id="0b80c-129">Configurare TensorFlow con DirectML Preview</span><span class="sxs-lookup"><span data-stu-id="0b80c-129">Set up the TensorFlow with DirectML preview</span></span> 

### <a name="install-wsl-2"></a><span data-ttu-id="0b80c-130">Installare WSL 2</span><span class="sxs-lookup"><span data-stu-id="0b80c-130">Install WSL 2</span></span> 

<span data-ttu-id="0b80c-131">Dopo aver installato il driver precedente, assicurarsi di [abilitare WSL 2](/windows/wsl/install-win10) e [installare una distribuzione basata su glibc](/windows/wsl/install-win10#install-your-linux-distribution-of-choice) (ad esempio Ubuntu o Debian).</span><span class="sxs-lookup"><span data-stu-id="0b80c-131">Once you've installed the above driver, ensure you [enable WSL 2](/windows/wsl/install-win10) and [install a glibc-based distribution](/windows/wsl/install-win10#install-your-linux-distribution-of-choice) (like Ubuntu or Debian).</span></span> <span data-ttu-id="0b80c-132">Per i test, abbiamo usato Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="0b80c-132">For our testing, we used Ubuntu.</span></span> <span data-ttu-id="0b80c-133">Assicurarsi di avere il kernel più recente selezionando **Controlla aggiornamenti** nella sezione **Windows Update** dell'app Impostazioni.</span><span class="sxs-lookup"><span data-stu-id="0b80c-133">Ensure you have the latest kernel by selecting **Check for updates** in the **Windows Update** section of the Settings app.</span></span> 

> [!NOTE]
> <span data-ttu-id="0b80c-134">Assicurarsi di disporre degli **aggiornamenti di ricezione per altri prodotti Microsoft quando si aggiorna Windows** abilitato.</span><span class="sxs-lookup"><span data-stu-id="0b80c-134">Ensure you have the **Receive updates for other Microsoft products when you update Windows** enabled.</span></span> <span data-ttu-id="0b80c-135">È possibile trovarlo in **Opzioni avanzate** all'interno della sezione **Windows Update** dell'app Impostazioni.</span><span class="sxs-lookup"><span data-stu-id="0b80c-135">You can find it in **Advanced options** within the **Windows Update** section of the Settings app.</span></span> 

<span data-ttu-id="0b80c-136">Per questa anteprima è necessaria una versione del kernel di 4.19.121 o superiore.</span><span class="sxs-lookup"><span data-stu-id="0b80c-136">For this preview, you need a kernel version of 4.19.121 or higher.</span></span> <span data-ttu-id="0b80c-137">È possibile controllare il numero di versione eseguendo il comando seguente in PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0b80c-137">You can check the version number by running the following command in PowerShell.</span></span> 

```
wsl cat /proc/version
```

### <a name="set-up-python-environment"></a><span data-ttu-id="0b80c-138">Configurare l'ambiente Python</span><span class="sxs-lookup"><span data-stu-id="0b80c-138">Set up Python environment</span></span> 

<span data-ttu-id="0b80c-139">Si consiglia di configurare un ambiente Python virtuale all'interno dell'istanza di WSL 2.</span><span class="sxs-lookup"><span data-stu-id="0b80c-139">We recommend setting up a virtual Python environment inside your WSL 2 instance.</span></span> <span data-ttu-id="0b80c-140">Sono disponibili molti strumenti che è possibile usare per configurare un ambiente Python virtuale. per queste istruzioni verrà usato [il Miniconda di Anaconda](https://docs.conda.io/en/latest/miniconda.html).</span><span class="sxs-lookup"><span data-stu-id="0b80c-140">There are many tools you can use to setup a virtual Python environment — for these instructions, we'll use [Anaconda’s Miniconda](https://docs.conda.io/en/latest/miniconda.html).</span></span> <span data-ttu-id="0b80c-141">Il resto di questa installazione presuppone l'uso di un ambiente miniconda.</span><span class="sxs-lookup"><span data-stu-id="0b80c-141">The rest of this setup assumes you use a miniconda environment.</span></span> 

<span data-ttu-id="0b80c-142">Installare Miniconda seguendo le [indicazioni sul sito di Anaconda](https://conda.io/projects/conda/en/latest/user-guide/install/index.html)oppure eseguendo i comandi seguenti in WSL.</span><span class="sxs-lookup"><span data-stu-id="0b80c-142">Install Miniconda by following the [guidance on Anaconda’s site](https://conda.io/projects/conda/en/latest/user-guide/install/index.html), or by running the following commands in WSL.</span></span> 

```
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh 
bash Miniconda3-latest-Linux-x86_64.sh 
```

<span data-ttu-id="0b80c-143">Dopo l'installazione di Miniconda in WSL, creare un ambiente usando Python denominato "directml" e attivarlo tramite i comandi seguenti.</span><span class="sxs-lookup"><span data-stu-id="0b80c-143">Once Miniconda is installed in WSL, create an environment using Python named “directml” and activate it through the following commands.</span></span> 

> [!NOTE]
> <span data-ttu-id="0b80c-144">Nei comandi seguenti viene usato Python 3,6.</span><span class="sxs-lookup"><span data-stu-id="0b80c-144">In the commands below, we use Python 3.6.</span></span> <span data-ttu-id="0b80c-145">Tuttavia, il pacchetto tensorflow-directml funziona in un ambiente Python 3,5, 3,6 o 3,7.</span><span class="sxs-lookup"><span data-stu-id="0b80c-145">However, the tensorflow-directml package works in a Python 3.5, 3.6 or 3.7 environment.</span></span> 

```
conda create --name directml python=3.6 

conda activate directml 
```

### <a name="install-the-tensorflow-with-directml-package"></a><span data-ttu-id="0b80c-146">Installare il pacchetto Tensorflow con DirectML</span><span class="sxs-lookup"><span data-stu-id="0b80c-146">Install the Tensorflow with DirectML package</span></span> 

<span data-ttu-id="0b80c-147">Installare il pacchetto di TensorFlow con un back-end DirectML tramite PIP eseguendo il comando seguente.</span><span class="sxs-lookup"><span data-stu-id="0b80c-147">Install the package of TensorFlow with a DirectML backend through pip by running the following command.</span></span>

> [!NOTE]
> <span data-ttu-id="0b80c-148">Il pacchetto tensorflow-directml supporta solo TensorFlow 1,15.</span><span class="sxs-lookup"><span data-stu-id="0b80c-148">The tensorflow-directml package only supports TensorFlow 1.15.</span></span> 

```
pip install tensorflow-directml
```

<span data-ttu-id="0b80c-149">Dopo aver installato il pacchetto tensorflow-directml, è possibile verificare che venga eseguito correttamente aggiungendo due tensori.</span><span class="sxs-lookup"><span data-stu-id="0b80c-149">Once you’ve installed the tensorflow-directml package, you can verify that it runs correctly by adding two tensors.</span></span> <span data-ttu-id="0b80c-150">Copiare le righe seguenti in una sessione interattiva di Python.</span><span class="sxs-lookup"><span data-stu-id="0b80c-150">Copy the following lines into an interactive Python session.</span></span> 

```
import tensorflow.compat.v1 as tf 

tf.enable_eager_execution(tf.ConfigProto(log_device_placement=True)) 

print(tf.add([1.0, 2.0], [3.0, 4.0])) 
```

<span data-ttu-id="0b80c-151">Verrà visualizzato un output simile al seguente, con l'operatore Add inserito sul dispositivo DML.</span><span class="sxs-lookup"><span data-stu-id="0b80c-151">You should see output similar to the following, with the add operator placed on the DML device.</span></span> 

```
2020-06-15 11:27:18.235973: I tensorflow/core/common_runtime/dml/dml_device_factory.cc:45] DirectML device enumeration: found 1 compatible adapters. 

2020-06-15 11:27:18.240065: I tensorflow/core/common_runtime/dml/dml_device_factory.cc:32] DirectML: creating device on adapter 0 (AMD Radeon VII) 

2020-06-15 11:27:18.323949: I tensorflow/stream_executor/platform/default/dso_loader.cc:60] Successfully opened dynamic library libdirectml.so.ba106a7c621ea741d21598708ee581c11918380 

2020-06-15 11:27:18.337830: I tensorflow/core/common_runtime/eager/execute.cc:571] Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0 

tf.Tensor([4. 6.], shape=(2,), dtype=float32) 
```

## <a name="tensorflow-with-directml-samples-and-feedback"></a><span data-ttu-id="0b80c-152">Tensorflow con DirectML esempi e commenti e suggerimenti</span><span class="sxs-lookup"><span data-stu-id="0b80c-152">Tensorflow with DirectML samples and feedback</span></span> 

<span data-ttu-id="0b80c-153">A questo punto si è pronti per iniziare a scoprire di più su ML training.</span><span class="sxs-lookup"><span data-stu-id="0b80c-153">Now you’re ready to start learning more about ML training.</span></span> <span data-ttu-id="0b80c-154">Vedere le [esercitazioni di TensorFlow](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) o gli [esempi](https://github.com/microsoft/DirectML).</span><span class="sxs-lookup"><span data-stu-id="0b80c-154">Check out the [TensorFlow tutorials](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) or [our samples](https://github.com/microsoft/DirectML).</span></span> <span data-ttu-id="0b80c-155">Questo contenuto è stato usato come convalida per questo pacchetto di anteprima iniziale di TensorFlow con DirectML.</span><span class="sxs-lookup"><span data-stu-id="0b80c-155">We used this content as validation for this initial preview package of TensorFlow with DirectML.</span></span> 

<span data-ttu-id="0b80c-156">Se si verificano problemi o si inviano commenti e suggerimenti sul pacchetto TensorFlow con DirectML, [connettersi al team](https://github.com/microsoft/DirectML/issues).</span><span class="sxs-lookup"><span data-stu-id="0b80c-156">If you run into issues or have feedback on the TensorFlow with DirectML package, please [connect with our team here](https://github.com/microsoft/DirectML/issues).</span></span>
