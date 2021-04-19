---
description: La \_ struttura della mappa PID contiene identifica il contenuto di un ID pacchetto del flusso di trasporto MPEG-2.
ms.assetid: c247ec75-483d-4587-a82f-07bbf6d277b4
title: Struttura PID_MAP (Bdatypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PID_MAP
api_type:
- HeaderDef
api_location:
- bdatypes.h
ms.openlocfilehash: 98b238c61ccfcfb93e4ddcc0a051d9084228f604
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332184"
---
# <a name="pid_map-structure"></a><span data-ttu-id="457ab-103">\_Struttura mappa PID</span><span class="sxs-lookup"><span data-stu-id="457ab-103">PID\_MAP structure</span></span>

<span data-ttu-id="457ab-104">La `PID_MAP` struttura contiene identifica il contenuto di un ID pacchetto del flusso di trasporto MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="457ab-104">The `PID_MAP` structure contains identifies the contents of an MPEG-2 transport stream packet ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="457ab-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="457ab-105">Syntax</span></span>


```C++
typedef struct {
  ULONG                ulPID;
  MEDIA_SAMPLE_CONTENT MediaSampleContent;
} PID_MAP;
```



## <a name="members"></a><span data-ttu-id="457ab-106">Members</span><span class="sxs-lookup"><span data-stu-id="457ab-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="457ab-107">**ulPID**</span><span class="sxs-lookup"><span data-stu-id="457ab-107">**ulPID**</span></span>
</dt> <dd>

<span data-ttu-id="457ab-108">Specifica l'ID pacchetto (PID)</span><span class="sxs-lookup"><span data-stu-id="457ab-108">Specifies the packet ID (PID)</span></span>

</dd> <dt>

<span data-ttu-id="457ab-109">**MediaSampleContent**</span><span class="sxs-lookup"><span data-stu-id="457ab-109">**MediaSampleContent**</span></span>
</dt> <dd>

<span data-ttu-id="457ab-110">Specifica il contenuto del payload del pacchetto, come tipo di enumerazione del [**\_ \_ contenuto di esempio multimediale**](media-sample-content.md) .</span><span class="sxs-lookup"><span data-stu-id="457ab-110">Specifies the contents of the packet payload, as a [**MEDIA\_SAMPLE\_CONTENT**](media-sample-content.md) enumeration type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="457ab-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="457ab-111">Requirements</span></span>



| <span data-ttu-id="457ab-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="457ab-112">Requirement</span></span> | <span data-ttu-id="457ab-113">Valore</span><span class="sxs-lookup"><span data-stu-id="457ab-113">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="457ab-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="457ab-114">Header</span></span><br/> | <dl> <span data-ttu-id="457ab-115"><dt>Bdatypes. h (include Bdaiface. h)</dt></span><span class="sxs-lookup"><span data-stu-id="457ab-115"><dt>Bdatypes.h (include Bdaiface.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="457ab-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="457ab-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="457ab-117">Strutture DirectShow</span><span class="sxs-lookup"><span data-stu-id="457ab-117">DirectShow Structures</span></span>](directshow-structures.md)
</dt> <dt>

[<span data-ttu-id="457ab-118">**Interfaccia IEnumPIDMap**</span><span class="sxs-lookup"><span data-stu-id="457ab-118">**IEnumPIDMap Interface**</span></span>](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-ienumpidmap)
</dt> </dl>

 

 




