---
title: Nomi dei dispositivi
description: Nomi dei dispositivi
ms.assetid: 0ba06439-cc33-43e1-a094-09bcc5e2f6b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e516f7f8eed338067dc373f8509f46598e198c71
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471766"
---
# <a name="device-names"></a><span data-ttu-id="30e1a-103">Nomi dei dispositivi</span><span class="sxs-lookup"><span data-stu-id="30e1a-103">Device Names</span></span>

<span data-ttu-id="30e1a-104">Per ogni tipo di dispositivo potrebbero essere presenti diversi driver MCI che condividono il set di comandi ma operano su formati di dati diversi.</span><span class="sxs-lookup"><span data-stu-id="30e1a-104">For each device type, there might be several MCI drivers that share the command set but operate on different data formats.</span></span> <span data-ttu-id="30e1a-105">Per identificare in modo univoco un driver MCI, MCI USA *i nomi di dispositivo*.</span><span class="sxs-lookup"><span data-stu-id="30e1a-105">To uniquely identify an MCI driver, MCI uses *device names*.</span></span>

<span data-ttu-id="30e1a-106">I nomi dei dispositivi sono identificati \[ nella \] sezione MCI del file SYSTEM.INI o nella parte appropriata del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="30e1a-106">Device names are identified either in the \[mci\] section of the SYSTEM.INI file or in the appropriate part of the registry.</span></span> <span data-ttu-id="30e1a-107">Queste informazioni identificano tutti i driver MCI per Windows.</span><span class="sxs-lookup"><span data-stu-id="30e1a-107">This information identifies all MCI drivers to Windows.</span></span> <span data-ttu-id="30e1a-108">Le voci nella \[ sezione MCI \] usano il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="30e1a-108">The entries in the \[mci\] section use the following form:</span></span>

<span data-ttu-id="30e1a-109">*\_ nome dispositivo*  =  *driver \_ filename. Extension*</span><span class="sxs-lookup"><span data-stu-id="30e1a-109">*device\_name* = *driver\_filename.extension*</span></span>

<span data-ttu-id="30e1a-110">Nell'esempio seguente viene illustrata \[ una \] sezione MCI tipica da SYSTEM.INI:</span><span class="sxs-lookup"><span data-stu-id="30e1a-110">The following example shows a typical \[mci\] section from SYSTEM.INI:</span></span>


```C++
[mci]
cdaudio=mcicda.drv 
sequencer=mciseq.drv 
waveaudio=mciwave.drv 
avivideo=mciavi.drv
```



<span data-ttu-id="30e1a-111">Se un driver MCI viene installato usando un nome di dispositivo già esistente in SYSTEM.INI o nel registro di sistema, il sistema aggiunge un numero intero al nome del dispositivo del nuovo driver, creando un nome univoco per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="30e1a-111">If an MCI driver is installed using a device name that already exists in SYSTEM.INI or the registry, the system appends an integer to the device name of the new driver, creating a unique device name.</span></span> <span data-ttu-id="30e1a-112">Nell'esempio precedente, a un driver aggiuntivo installato con il nome del dispositivo "CDAudio" viene assegnato il nome del dispositivo "cdaudio1".</span><span class="sxs-lookup"><span data-stu-id="30e1a-112">In the preceding example, an additional driver installed using the "cdaudio" device name would be assigned the device name "cdaudio1".</span></span>

 

 




