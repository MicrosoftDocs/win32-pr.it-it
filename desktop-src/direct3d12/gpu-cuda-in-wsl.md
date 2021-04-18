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
# <a name="enable-nvidia-cuda-in-wsl-2"></a>Abilitare NVIDIA CUDA in WSL 2

Windows Insider SDK supporta l'esecuzione di strumenti di Machine Learning, librerie e Framework diffusi che usano NVIDIA CUDA per l'accelerazione hardware GPU all'interno di un'istanza di WSL 2. Sono inclusi PyTorch e TensorFlow, oltre a tutti i supporti Docker e NVIDIA container Toolkit disponibili in un ambiente Linux nativo. 

> [!NOTE]
> Le funzionalità seguenti sono disponibili nelle versioni provvisorie di Windows 10 e sono soggette a modifiche.

## <a name="install-the-latest-windows-insider-dev-channel-build"></a>Installare la versione più recente di Windows Insider dev Channel Build 

Per usare questa versione di anteprima, è necessario [registrarsi al programma Windows Insider](https://insider.windows.com/getting-started/#register). Al termine, seguire [questi instuctions](https://insider.windows.com/getting-started/#install) per installare la build più recente di insider. Quando si scelgono le impostazioni, assicurarsi di selezionare il [canale dev](/windows-insider/flight-hub/#active-development-builds-of-windows-10). 

Per questa anteprima è necessario compilare 20150 o versione successiva. È possibile controllare il numero di versione della build eseguendo `winver` tramite il comando **Run** (tasto logo Windows + R).

## <a name="install-the-preview-gpu-driver"></a>Installare il driver della GPU di anteprima 

Scaricare e installare il [driver NVIDIA CUDA-enabled per WSL](https://developer.nvidia.com/cuda/wsl) da usare con i flussi di lavoro CUDA ml esistenti. 

## <a name="set-up-wsl-2-for-the-preview"></a>Configurare WSL 2 per l'anteprima 

Dopo aver installato il driver precedente, assicurarsi di [abilitare WSL 2](/windows/wsl/install-win10) e [installare una distribuzione basata su glibc](/windows/wsl/install-win10#install-your-linux-distribution-of-choice) (ad esempio Ubuntu o Debian). Assicurarsi di avere il kernel più recente selezionando **Controlla aggiornamenti** nella sezione **Windows Update** dell'app Impostazioni. 

> [!NOTE]
> Assicurarsi **di ricevere gli aggiornamenti per altri prodotti Microsoft quando si aggiorna Windows** abilitato. È possibile trovarlo in **Opzioni avanzate** all'interno della sezione **Windows Update** dell'app Impostazioni. 

Per questa anteprima è necessaria una versione del kernel di 4.19.121 o superiore. È possibile controllare il numero di versione eseguendo il comando seguente in PowerShell. 

```powershell
wsl cat /proc/version
```

A questo punto è possibile iniziare a usare i flussi di lavoro di esistente Linux tramite [NVIDIA Docker](https://github.com/NVIDIA/nvidia-docker)oppure installando [PyTorch](https://pytorch.org/get-started/locally/) o [TensorFlow](https://www.tensorflow.org/install/gpu) all'interno di WSL 2. Altre informazioni sulla configurazione vengono acquisite nel [manuale dell'utente di NVIDIA CUDA on WSL](https://docs.nvidia.com/cuda/wsl-user-guide/index.html).

Condividi il feedback sul supporto di NVIDIA tramite il [Forum della community per CUDA in WSL](https://forums.developer.nvidia.com/c/accelerated-computing/cuda/cuda-on-windows-subsystem-for-linux-wsl-2/303).
