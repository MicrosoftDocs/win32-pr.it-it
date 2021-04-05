---
title: PATCHARRAY (mmsystem. h)
description: PATCHARRAY è un tipo usato per definire una matrice di patch MIDI.
ms.assetid: f48ee0d2-224a-4530-ac28-ae63160316cc
keywords:
- PATCHARRAY MIDIPATCHSIZE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e07af0e878fc0d2fc79d6d17aafd48fbd991fb39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874625"
---
# <a name="patcharray"></a><span data-ttu-id="7fbb0-104">PATCHARRAY</span><span class="sxs-lookup"><span data-stu-id="7fbb0-104">PATCHARRAY</span></span>

<span data-ttu-id="7fbb0-105">PATCHARRAY è un tipo usato per definire una matrice di patch MIDI.</span><span class="sxs-lookup"><span data-stu-id="7fbb0-105">PATCHARRAY is a type used to define an array of MIDI patches.</span></span>


```C++
typedef WORD PATCHARRAY[MIDIPATCHSIZE];
```



<dl> <dt>

<span data-ttu-id="7fbb0-106">**\[MIDIPATCHSIZE PATCHARRAY\]**</span><span class="sxs-lookup"><span data-stu-id="7fbb0-106">**PATCHARRAY\[MIDIPATCHSIZE\]**</span></span>
</dt> <dd>

<span data-ttu-id="7fbb0-107">Ogni elemento nella matrice corrisponde a una patch con ognuno dei 16 bit che rappresenta uno dei 16 canali MIDI.</span><span class="sxs-lookup"><span data-stu-id="7fbb0-107">Each element in the array corresponds to a patch with each of the 16 bits representing one of the 16 MIDI channels.</span></span> <span data-ttu-id="7fbb0-108">Per ognuno dei canali che usano tale patch particolare sono impostati bit.</span><span class="sxs-lookup"><span data-stu-id="7fbb0-108">Bits are set for each of the channels that use that particular patch.</span></span> <span data-ttu-id="7fbb0-109">Se, ad esempio, il numero di patch 0 viene usato dai canali MIDI fisici 0 e 8, l'elemento 0 della matrice deve essere impostato su 0x0101.</span><span class="sxs-lookup"><span data-stu-id="7fbb0-109">For example, if patch number 0 is used by physical MIDI channels 0 and 8, element 0 of the array should be set to 0x0101.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7fbb0-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7fbb0-110">Requirements</span></span>



| <span data-ttu-id="7fbb0-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fbb0-111">Requirement</span></span> | <span data-ttu-id="7fbb0-112">Valore</span><span class="sxs-lookup"><span data-stu-id="7fbb0-112">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fbb0-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7fbb0-113">Minimum supported client</span></span><br/> | <span data-ttu-id="7fbb0-114">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7fbb0-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="7fbb0-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7fbb0-115">Minimum supported server</span></span><br/> | <span data-ttu-id="7fbb0-116">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7fbb0-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="7fbb0-117">Versione</span><span class="sxs-lookup"><span data-stu-id="7fbb0-117">Version</span></span><br/>                  | <span data-ttu-id="7fbb0-118">MIDI (Musical Instrument Digital Interface), tipi MIDI</span><span class="sxs-lookup"><span data-stu-id="7fbb0-118">Musical Instrument Digital Interface (MIDI), MIDI Types</span></span><br/>                                        |
| <span data-ttu-id="7fbb0-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7fbb0-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="7fbb0-120"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7fbb0-120"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fbb0-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7fbb0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fbb0-122">Tipi MIDI</span><span class="sxs-lookup"><span data-stu-id="7fbb0-122">MIDI Types</span></span>](midi-event-types.md)
</dt> </dl>

 

 





