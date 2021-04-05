---
title: Supporto per USB 3,0
description: Supporto per USB 3,0
ms.assetid: AACE4B57-A03F-40C7-AFDD-514D29F24521
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c2f6fa342efa5e7b4fd95287a2061482fa0cbb9
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "103730759"
---
# <a name="support-for-usb-30"></a><span data-ttu-id="e0912-103">Supporto per USB 3,0</span><span class="sxs-lookup"><span data-stu-id="e0912-103">Support for USB 3.0</span></span>

## <a name="platforms"></a><span data-ttu-id="e0912-104">Piattaforme</span><span class="sxs-lookup"><span data-stu-id="e0912-104">Platforms</span></span>

<span data-ttu-id="e0912-105">**Client** -Windows 8</span><span class="sxs-lookup"><span data-stu-id="e0912-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="e0912-106">**Server** : Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e0912-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="e0912-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e0912-107">Description</span></span>

<span data-ttu-id="e0912-108">In Windows 8 e Windows Server 2012 è stato aggiunto il supporto per USB 3,0.</span><span class="sxs-lookup"><span data-stu-id="e0912-108">In Windows 8 and Windows Server 2012, we added support for USB 3.0.</span></span> <span data-ttu-id="e0912-109">Questa operazione è stata eseguita aggiungendo un nuovo stack software per potenziare il controller host USB 3,0, denominato XHC (eXtensible Host Controller).</span><span class="sxs-lookup"><span data-stu-id="e0912-109">We did this by adding a new software stack to power the USB 3.0 host controller, called an eXtensible Host Controller (XHC).</span></span> <span data-ttu-id="e0912-110">Sono stati mantenuti la parità di interfaccia, il livello livello IRQL, il contesto del chiamante, lo stato di errore, la frequenza dei tentativi e così via.</span><span class="sxs-lookup"><span data-stu-id="e0912-110">We maintained interface parity, IRQL level, caller context, error status, retry frequency, and so on.</span></span> <span data-ttu-id="e0912-111">Non dovrebbe esserci alcuna differenza quando si interagisce con un dispositivo connesso tramite USB 2,0 rispetto a USB 3,0.</span><span class="sxs-lookup"><span data-stu-id="e0912-111">There should be no difference for you when interacting with a device connected over USB 2.0 versus USB 3.0.</span></span>

<span data-ttu-id="e0912-112">Tuttavia, se si sta scrivendo un driver per un nuovo dispositivo USB 3,0, è possibile optare per le nuove funzionalità USB 3,0.</span><span class="sxs-lookup"><span data-stu-id="e0912-112">However, if you are writing a driver for a new, USB 3.0 device, definitely opt for new USB 3.0 capabilities.</span></span>

## <a name="manifestation"></a><span data-ttu-id="e0912-113">Manifestazione</span><span class="sxs-lookup"><span data-stu-id="e0912-113">Manifestation</span></span>

<span data-ttu-id="e0912-114">I trasferimenti di dispositivi sono più veloci e la potenza viene consumata da un PC tramite dispositivi USB complessivi.</span><span class="sxs-lookup"><span data-stu-id="e0912-114">Device transfers are faster and less power is consumed from a PC by USB devices overall.</span></span> <span data-ttu-id="e0912-115">Sussiste il rischio che i dispositivi USB esistenti non funzionino correttamente quando si è connessi a una porta USB 3,0.</span><span class="sxs-lookup"><span data-stu-id="e0912-115">There is a risk that existing USB devices may not function correctly when connected to a USB 3.0 port.</span></span> <span data-ttu-id="e0912-116">Questo problema non si verifica e non è previsto, ma poiché il software che alimenta USB 3,0 è nuovo, si tratta di un rischio.</span><span class="sxs-lookup"><span data-stu-id="e0912-116">This should not happen, and is not expected, but, because the software that powers USB 3.0 is new, it is a risk.</span></span>

 

 




