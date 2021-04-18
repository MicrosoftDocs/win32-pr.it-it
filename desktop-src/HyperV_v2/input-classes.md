---
description: I dispositivi di input utente sono rappresentati da queste classi. Una macchina virtuale ha sempre un'istanza di ogni classe associata.
ms.assetid: FFCA890D-6102-47BB-B499-4B9D77D75E9B
title: Classi di input
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2955cadfb00dcc39fed490a9c706b12bb1a8993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309508"
---
# <a name="input-classes"></a><span data-ttu-id="cef59-104">Classi di input</span><span class="sxs-lookup"><span data-stu-id="cef59-104">Input classes</span></span>

<span data-ttu-id="cef59-105">I dispositivi di input utente sono rappresentati da queste classi.</span><span class="sxs-lookup"><span data-stu-id="cef59-105">The user input devices are represented by these classes.</span></span> <span data-ttu-id="cef59-106">Una macchina virtuale ha sempre un'istanza di ogni classe associata.</span><span class="sxs-lookup"><span data-stu-id="cef59-106">A virtual machine always has one instance of each class associated with it.</span></span> <span data-ttu-id="cef59-107">Questi dispositivi non possono essere aggiunti o rimossi dalla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="cef59-107">These devices may not be added or removed from the virtual machine.</span></span> <span data-ttu-id="cef59-108">Pertanto, non sono presenti istanze del pool di risorse per i dispositivi della tastiera o del mouse.</span><span class="sxs-lookup"><span data-stu-id="cef59-108">Therefore, there are no resource pool instances for keyboard or mouse devices.</span></span>

<span data-ttu-id="cef59-109">I dispositivi della tastiera e del mouse sono collegati alla macchina virtuale tramite l'associazione [**\_ SystemDevice di MSVM**](msvm-systemdevice.md) .</span><span class="sxs-lookup"><span data-stu-id="cef59-109">The keyboard and mouse devices are linked to the virtual machine through the [**Msvm\_SystemDevice**](msvm-systemdevice.md) association.</span></span> <span data-ttu-id="cef59-110">Una macchina virtuale contiene un dispositivo mouse PS2 e un mouse sintetico.</span><span class="sxs-lookup"><span data-stu-id="cef59-110">A virtual machine contains both a PS2 and a synthetic mouse device.</span></span> <span data-ttu-id="cef59-111">Solo un dispositivo di puntamento è attivo alla volta.</span><span class="sxs-lookup"><span data-stu-id="cef59-111">Only one pointing device is active at a time.</span></span>

<span data-ttu-id="cef59-112">Di seguito sono riportate le classi WMI di virtualizzazione correlate all'input.</span><span class="sxs-lookup"><span data-stu-id="cef59-112">The following are virtualization WMI classes related to input.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="cef59-113">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="cef59-113">In this section</span></span>



| <span data-ttu-id="cef59-114">Argomento</span><span class="sxs-lookup"><span data-stu-id="cef59-114">Topic</span></span>                                                          | <span data-ttu-id="cef59-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cef59-115">Description</span></span>                                     |
|----------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="cef59-116">**\_Tastiera MSVM**</span><span class="sxs-lookup"><span data-stu-id="cef59-116">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)<br/>             | <span data-ttu-id="cef59-117">Rappresenta un dispositivo da tastiera.</span><span class="sxs-lookup"><span data-stu-id="cef59-117">Represents a keyboard device.</span></span><br/>        |
| [<span data-ttu-id="cef59-118">**\_Ps2Mouse MSVM**</span><span class="sxs-lookup"><span data-stu-id="cef59-118">**Msvm\_Ps2Mouse**</span></span>](msvm-ps2mouse.md)<br/>             | <span data-ttu-id="cef59-119">Rappresenta un dispositivo mouse PS2.</span><span class="sxs-lookup"><span data-stu-id="cef59-119">Represents a PS2 mouse device.</span></span><br/>       |
| [<span data-ttu-id="cef59-120">**\_SyntheticMouse MSVM**</span><span class="sxs-lookup"><span data-stu-id="cef59-120">**Msvm\_SyntheticMouse**</span></span>](msvm-syntheticmouse.md)<br/> | <span data-ttu-id="cef59-121">Rappresenta un dispositivo mouse sintetico.</span><span class="sxs-lookup"><span data-stu-id="cef59-121">Represents a synthetic mouse device.</span></span><br/> |



 

 

 




