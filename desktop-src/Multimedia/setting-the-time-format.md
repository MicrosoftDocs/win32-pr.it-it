---
title: Impostazione del formato dell'ora
description: Impostazione del formato dell'ora
ms.assetid: c670d47e-30fc-4637-b468-b6a415605dca
keywords:
- MCI_SET messaggio di comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6bc48faa36fea49b0aba749476c998572ebf400
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872414"
---
# <a name="setting-the-time-format"></a><span data-ttu-id="c6a0a-104">Impostazione del formato dell'ora</span><span class="sxs-lookup"><span data-stu-id="c6a0a-104">Setting the Time Format</span></span>

<span data-ttu-id="c6a0a-105">Usare il messaggio del comando [**\_ set di MCI**](mci-set.md) insieme alla struttura [**\_ set \_ parametri di MCI**](mci-set-parms.md) per impostare il formato dell'ora per un dispositivo aperto.</span><span class="sxs-lookup"><span data-stu-id="c6a0a-105">Use the [**MCI\_SET**](mci-set.md) command message along with the [**MCI\_SET\_PARMS**](mci-set-parms.md) structure to set the time format for an open device.</span></span> <span data-ttu-id="c6a0a-106">Impostare il membro **dwTimeFormat** su una delle seguenti costanti.</span><span class="sxs-lookup"><span data-stu-id="c6a0a-106">Set the **dwTimeFormat** member to one of the following constants.</span></span>



| <span data-ttu-id="c6a0a-107">Costante</span><span class="sxs-lookup"><span data-stu-id="c6a0a-107">Constant</span></span>                   | <span data-ttu-id="c6a0a-108">Formato ora</span><span class="sxs-lookup"><span data-stu-id="c6a0a-108">Time format</span></span>                                          |
|----------------------------|------------------------------------------------------|
| <span data-ttu-id="c6a0a-109">\_byte in formato MCI \_</span><span class="sxs-lookup"><span data-stu-id="c6a0a-109">MCI\_FORMAT\_BYTES</span></span>         | <span data-ttu-id="c6a0a-110">Byte (nei file in formato PCM con modulazione del codice Pulse \[ \] )</span><span class="sxs-lookup"><span data-stu-id="c6a0a-110">Bytes (in pulse code modulated \[PCM\] format files)</span></span> |
| <span data-ttu-id="c6a0a-111">\_ \_ millisecondi formato MCI</span><span class="sxs-lookup"><span data-stu-id="c6a0a-111">MCI\_FORMAT\_MILLISECONDS</span></span>  | <span data-ttu-id="c6a0a-112">Millisecondi</span><span class="sxs-lookup"><span data-stu-id="c6a0a-112">Milliseconds</span></span>                                         |
| <span data-ttu-id="c6a0a-113">\_MSF formato \_ MCI</span><span class="sxs-lookup"><span data-stu-id="c6a0a-113">MCI\_FORMAT\_MSF</span></span>           | <span data-ttu-id="c6a0a-114">Minuto/secondo/frame</span><span class="sxs-lookup"><span data-stu-id="c6a0a-114">Minute/second/frame</span></span>                                  |
| <span data-ttu-id="c6a0a-115">\_esempi di formato MCI \_</span><span class="sxs-lookup"><span data-stu-id="c6a0a-115">MCI\_FORMAT\_SAMPLES</span></span>       | <span data-ttu-id="c6a0a-116">Esempi</span><span class="sxs-lookup"><span data-stu-id="c6a0a-116">Samples</span></span>                                              |
| <span data-ttu-id="c6a0a-117">\_Formato MCI \_ \_ 24</span><span class="sxs-lookup"><span data-stu-id="c6a0a-117">MCI\_FORMAT\_SMPTE\_24</span></span>     | <span data-ttu-id="c6a0a-118">SMPTE, 24 frame</span><span class="sxs-lookup"><span data-stu-id="c6a0a-118">SMPTE, 24 frame</span></span>                                      |
| <span data-ttu-id="c6a0a-119">\_Formato MCI \_ \_ 25</span><span class="sxs-lookup"><span data-stu-id="c6a0a-119">MCI\_FORMAT\_SMPTE\_25</span></span>     | <span data-ttu-id="c6a0a-120">SMPTE, 25 frame</span><span class="sxs-lookup"><span data-stu-id="c6a0a-120">SMPTE, 25 frame</span></span>                                      |
| <span data-ttu-id="c6a0a-121">\_Formato MCI \_ \_ 30</span><span class="sxs-lookup"><span data-stu-id="c6a0a-121">MCI\_FORMAT\_SMPTE\_30</span></span>     | <span data-ttu-id="c6a0a-122">SMPTE, 30 frame</span><span class="sxs-lookup"><span data-stu-id="c6a0a-122">SMPTE, 30 frame</span></span>                                      |
| <span data-ttu-id="c6a0a-123">\_Formato MCI \_ \_ 30DROP</span><span class="sxs-lookup"><span data-stu-id="c6a0a-123">MCI\_FORMAT\_SMPTE\_30DROP</span></span> | <span data-ttu-id="c6a0a-124">SMPTE, 30 frame drop</span><span class="sxs-lookup"><span data-stu-id="c6a0a-124">SMPTE, 30 frame drop</span></span>                                 |
| <span data-ttu-id="c6a0a-125">\_formato MCI \_ TMSF</span><span class="sxs-lookup"><span data-stu-id="c6a0a-125">MCI\_FORMAT\_TMSF</span></span>          | <span data-ttu-id="c6a0a-126">Traccia/minuto/secondo/frame</span><span class="sxs-lookup"><span data-stu-id="c6a0a-126">Track/minute/second/frame</span></span>                            |
| <span data-ttu-id="c6a0a-127">\_ \_ formato SONGPTR MCI \_ Seq</span><span class="sxs-lookup"><span data-stu-id="c6a0a-127">MCI\_SEQ\_FORMAT\_SONGPTR</span></span>  | <span data-ttu-id="c6a0a-128">Puntatore al brano MIDI</span><span class="sxs-lookup"><span data-stu-id="c6a0a-128">MIDI song pointer</span></span>                                    |



 

<span data-ttu-id="c6a0a-129">Nell'esempio seguente il formato dell'ora viene impostato su millisecondi sul dispositivo specificato dalla variabile wDeviceID usando la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="c6a0a-129">The following example sets the time format to milliseconds on the device specified by the wDeviceID variable using the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function.</span></span>


```C++
UINT wDeviceID; 
MCI_SET_PARMS mciSetParms; 

// Set time format to milliseconds. 

mciSetParms.dwTimeFormat = MCI_FORMAT_MILLISECONDS; 
if( mciSendCommand(wDeviceID, MCI_SET, MCI_SET_TIME_FORMAT, 
                  (DWORD) &mciSetParms)) 
{
    // Error, unable to set time format. 
    return FALSE; 
}
else 
{
    // Time format set successfully. 
    return TRUE; 
}
```



 

 