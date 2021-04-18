---
title: Abilitare NVIDIA CUDA in WSL 2
description: Abilitare l'anteprima di NVIDIA CUDA nel sottosistema Windows per Linux
ms.topic: article
ms.date: 06/17/2020
ms.openlocfilehash: ea5b460d4b4c71417f8ac9969f58bcebf6d10af9
ms.sourcegitcommit: 85acfd5afdcd30c81e3d2b375e813957f9830e9f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/03/2020
ms.locfileid: "106300580"
---
# <a name="enable-nvidia-cuda-in-wsl-2"></a><span data-ttu-id="7e0c6-103">Abilitare NVIDIA CUDA in WSL 2</span><span class="sxs-lookup"><span data-stu-id="7e0c6-103">Enable NVIDIA CUDA in WSL 2</span></span>

<span data-ttu-id="7e0c6-104">Windows Insider SDK supporta l'esecuzione di strumenti di Machine Learning, librerie e Framework diffusi che usano NVIDIA CUDA per l'accelerazione hardware GPU all'interno di un'istanza di WSL 2.</span><span class="sxs-lookup"><span data-stu-id="7e0c6-104">The Windows Insider SDK supports running existing ML tools, libraries, and popular frameworks that use NVIDIA CUDA for GPU hardware acceleration inside a WSL 2 instance.</span></span> <span data-ttu-id="7e0c6-105">Sono inclusi PyTorch e TensorFlow, oltre a tutti i supporti Docker e NVIDIA container Toolkit disponibili in un ambiente Linux nativo.</span><span class="sxs-lookup"><span data-stu-id="7e0c6-105">This includes PyTorch and TensorFlow as well as all the Docker and NVIDIA Container Toolkit support available in a native Linux environment.</span></span> 

> [!NOTE]
> <span data-ttu-id="7e0c6-106">Le funzionalità seguenti sono disponibili nelle versioni provvisorie di Windows 10 e sono soggette a modifiche.</span><span class="sxs-lookup"><span data-stu-id="7e0c6-106">The following features are available in prerelease versions of Windows 10, and are subject to change.</span></span>

## <a name="install-the-latest-windows-insider-dev-channel-build"></a><span data-ttu-id="7e0c6-107">Installare la versione più recente di Windows Insider dev Channel Build</span><span class="sxs-lookup"><span data-stu-id="7e0c6-107">Install the latest Windows Insider Dev Channel build</span></span> 

<span data-ttu-id="7e0c6-108">Per usare questa versione di anteprima, è necessario [registrarsi al programma Windows Insider](https://insider.windows.com/getting-started/#register).</span><span class="sxs-lookup"><span data-stu-id="7e0c6-108">To use this preview, you'll need to [register for the Windows Insider Program](https://insider.windows.com/getting-started/#register).</span></span> <span data-ttu-id="7e0c6-109">Al termine, seguire [questi instuctions](https://insider.windows.com/getting-started/#install) per installare la build più recente di insider.</span><span class="sxs-lookup"><span data-stu-id="7e0c6-109">Once you do, follow [these instuctions](https://insider.windows.com/getting-started/#install) to install the latest Insider build.</span></span> <span data-ttu-id="7e0c6-110">Quando si scelgono le impostazioni, assicurarsi di selezionare il [canale dev](/windows-insider/flight-hub/#active-development-builds-of-windows-10).</span><span class="sxs-lookup"><span data-stu-id="7e0c6-110">When choosing your settings, ensure you're selecting the [Dev Channel](/windows-insider/flight-hub/#active-development-builds-of-windows-10).</span></span> 

<span data-ttu-id="7e0c6-111">Per questa anteprima è necessario compilare 20150 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="7e0c6-111">For this preview, you need Build 20150 or higher.</span></span> <span data-ttu-id="7e0c6-112">È possibile controllare il numero di versione della build eseguendo `winver` tramite il comando **Run** (tasto logo Windows + R).</span><span class="sxs-lookup"><span data-stu-id="7e0c6-112">You can check your build version number by running `winver` via the **Run** command (Windows logo key + R).</span></span>

## <a name="install-the-preview-gpu-driver"></a><span data-ttu-id="7e0c6-113">Installare il driver della GPU di anteprima</span><span class="sxs-lookup"><span data-stu-id="7e0c6-113">Install the preview GPU driver</span></span> 

<span data-ttu-id="7e0c6-114">Scaricare e installare il [driver NVIDIA CUDA-enabled per WSL](https://developer.nvidia.com/cuda/wsl) da usare con i flussi di lavoro CUDA ml esistenti.</span><span class="sxs-lookup"><span data-stu-id="7e0c6-114">Download and install the [NVIDIA CUDA-enabled driver for WSL](https://developer.nvidia.com/cuda/wsl) to use with your existing CUDA ML workflows.</span></span> 

## <a name="set-up-wsl-2-for-the-preview"></a><span data-ttu-id="7e0c6-115">Configurare WSL 2 per l'anteprima</span><span class="sxs-lookup"><span data-stu-id="7e0c6-115">Set up WSL 2 for the preview</span></span> 

<span data-ttu-id="7e0c6-116">Dopo aver installato il driver precedente, assicurarsi di [abilitare WSL 2](/windows/wsl/install-win10) e [installare una distribuzione basata su glibc](/windows/wsl/install-win10#install-your-linux-distribution-of-choice) (ad esempio Ubuntu o Debian).</span><span class="sxs-lookup"><span data-stu-id="7e0c6-116">Once you've installed the above driver, ensure you [enable WSL 2](/windows/wsl/install-win10) and [install a glibc-based distribution](/windows/wsl/install-win10#install-your-linux-distribution-of-choice) (such as Ubuntu or Debian).</span></span> <span data-ttu-id="7e0c6-117">Assicurarsi di avere il kernel più recente selezionando **Controlla aggiornamenti** nella sezione **Windows Update** dell'app Impostazioni.</span><span class="sxs-lookup"><span data-stu-id="7e0c6-117">Ensure you have the latest kernel by selecting **Check for updates** in the **Windows Update** section of the Settings app.</span></span> 

> [!NOTE]
> <span data-ttu-id="7e0c6-118">Assicurarsi **di ricevere gli aggiornamenti per altri prodotti Microsoft quando si aggiorna Windows** abilitato.</span><span class="sxs-lookup"><span data-stu-id="7e0c6-118">Ensure you have **Receive updates for other Microsoft products when you update Windows** enabled.</span></span> <span data-ttu-id="7e0c6-119">È possibile trovarlo in **Opzioni avanzate** all'interno della sezione **Windows Update** dell'app Impostazioni.</span><span class="sxs-lookup"><span data-stu-id="7e0c6-119">You can find it in **Advanced options** within the **Windows Update** section of the Settings app.</span></span> 

<span data-ttu-id="7e0c6-120">Per questa anteprima è necessaria una versione del kernel di 4.19.121 o superiore.</span><span class="sxs-lookup"><span data-stu-id="7e0c6-120">For this preview, you need a kernel version of 4.19.121 or higher.</span></span> <span data-ttu-id="7e0c6-121">È possibile controllare il numero di versione eseguendo il comando seguente in PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7e0c6-121">You can check the version number by running the following command in PowerShell.</span></span> 

```powershell
wsl cat /proc/version
```

<span data-ttu-id="7e0c6-122">A questo punto è possibile iniziare a usare i flussi di lavoro di esistente Linux tramite [NVIDIA Docker](https://github.com/NVIDIA/nvidia-docker)oppure installando [PyTorch](https://pytorch.org/get-started/locally/) o [TensorFlow](https://www.tensorflow.org/install/gpu) all'interno di WSL 2.</span><span class="sxs-lookup"><span data-stu-id="7e0c6-122">Now you can start using your exisiting Linux workflows through [NVIDIA Docker](https://github.com/NVIDIA/nvidia-docker), or by installing [PyTorch](https://pytorch.org/get-started/locally/) or [TensorFlow](https://www.tensorflow.org/install/gpu) inside WSL 2.</span></span> <span data-ttu-id="7e0c6-123">Altre informazioni sulla configurazione vengono acquisite nel [manuale dell'utente di NVIDIA CUDA on WSL](https://docs.nvidia.com/cuda/wsl-user-guide/index.html).</span><span class="sxs-lookup"><span data-stu-id="7e0c6-123">More information on getting set up is captured in [NVIDIA's CUDA on WSL User Guide](https://docs.nvidia.com/cuda/wsl-user-guide/index.html).</span></span>

<span data-ttu-id="7e0c6-124">Condividi il feedback sul supporto di NVIDIA tramite il [Forum della community per CUDA in WSL](https://forums.developer.nvidia.com/c/accelerated-computing/cuda/cuda-on-windows-subsystem-for-linux-wsl-2/303).</span><span class="sxs-lookup"><span data-stu-id="7e0c6-124">Share feedback on NVIDIA's support via their [Community forum for CUDA on WSL](https://forums.developer.nvidia.com/c/accelerated-computing/cuda/cuda-on-windows-subsystem-for-linux-wsl-2/303).</span></span>
