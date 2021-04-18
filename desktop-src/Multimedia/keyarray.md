---
title: Matrice di matrici (mmsystem. h)
description: Key ARRAY specifica un tipo usato per definire una matrice di chiavi.
ms.assetid: af1a1d2f-4558-4374-93ab-5a705fc879ca
keywords:
- MIDIPATCHSIZE DI MATRICI
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6e45e46417fb3b6653ecae605aa60f775c1d654
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301700"
---
# <a name="keyarray"></a><span data-ttu-id="c65de-104">Matrice di matrici</span><span class="sxs-lookup"><span data-stu-id="c65de-104">KEYARRAY</span></span>

<span data-ttu-id="c65de-105">Key ARRAY specifica un tipo usato per definire una matrice di chiavi.</span><span class="sxs-lookup"><span data-stu-id="c65de-105">KEYARRAY specifies a type used to define an array of keys.</span></span>


```C++
typedef WORD KEYARRAY[MIDIPATCHSIZE];
```



<dl> <dt>

<span data-ttu-id="c65de-106">**MIDIPATCHSIZE di matrici \[\]**</span><span class="sxs-lookup"><span data-stu-id="c65de-106">**KEYARRAY\[MIDIPATCHSIZE\]**</span></span>
</dt> <dd>

<span data-ttu-id="c65de-107">Ogni elemento nella matrice corrisponde a una patch di percussione basata su chiave con ognuno dei 16 bit che rappresenta uno dei 16 canali MIDI.</span><span class="sxs-lookup"><span data-stu-id="c65de-107">Each element in the array corresponds to a key-based percussion patch with each of the 16 bits representing one of the 16 MIDI channels.</span></span> <span data-ttu-id="c65de-108">Per ognuno dei canali che usano tale patch particolare sono impostati bit.</span><span class="sxs-lookup"><span data-stu-id="c65de-108">Bits are set for each of the channels that use that particular patch.</span></span> <span data-ttu-id="c65de-109">Se, ad esempio, la patch di percussione per il numero di chiave 60 viene usata dai canali MIDI fisici 9 e 15, l'elemento 60 della matrice deve essere impostato su 0x8200.</span><span class="sxs-lookup"><span data-stu-id="c65de-109">For example, if the percussion patch for key number 60 is used by physical MIDI channels 9 and 15, element 60 of the array should be set to 0x8200.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c65de-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c65de-110">Requirements</span></span>



| <span data-ttu-id="c65de-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="c65de-111">Requirement</span></span> | <span data-ttu-id="c65de-112">Valore</span><span class="sxs-lookup"><span data-stu-id="c65de-112">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c65de-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c65de-113">Minimum supported client</span></span><br/> | <span data-ttu-id="c65de-114">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c65de-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c65de-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c65de-115">Minimum supported server</span></span><br/> | <span data-ttu-id="c65de-116">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c65de-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c65de-117">Versione</span><span class="sxs-lookup"><span data-stu-id="c65de-117">Version</span></span><br/>                  | <span data-ttu-id="c65de-118">MIDI (Musical Instrument Digital Interface), tipi MIDI</span><span class="sxs-lookup"><span data-stu-id="c65de-118">Musical Instrument Digital Interface (MIDI), MIDI Types</span></span><br/>                                        |
| <span data-ttu-id="c65de-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c65de-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="c65de-120"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c65de-120"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c65de-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c65de-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c65de-122">Tipi MIDI</span><span class="sxs-lookup"><span data-stu-id="c65de-122">MIDI Types</span></span>](midi-event-types.md)
</dt> </dl>

 

 





