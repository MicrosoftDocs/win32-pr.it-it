---
title: Struttura WINBIO_BIR_DATA ( \_ tipi WINBIO. h)
description: Specifica la dimensione, in byte, e l'offset di un blocco di informazioni biometriche.
ms.assetid: 2f73eb1f-f1a1-4831-a8f7-eec28aa51645
keywords:
- Struttura di WINBIO_BIR_DATA Windows Biometric Framework API
topic_type:
- apiref
api_name:
- WINBIO_BIR_DATA
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41ebf7b157c5bd806442cdc120350a89ce646f9e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400593"
---
# <a name="winbio_bir_data-structure"></a><span data-ttu-id="dc051-104">\_ \_ Struttura dei dati WINBIO Bir</span><span class="sxs-lookup"><span data-stu-id="dc051-104">WINBIO\_BIR\_DATA structure</span></span>

<span data-ttu-id="dc051-105">La **struttura \_ \_ dei dati WINBIO bir** specifica la dimensione, in byte, e l'offset di un blocco di informazioni biometriche.</span><span class="sxs-lookup"><span data-stu-id="dc051-105">The **WINBIO\_BIR\_DATA** structure specifies the size, in bytes, and the offset of a block of biometric information.</span></span> <span data-ttu-id="dc051-106">Questa struttura viene usata dalla struttura [**WINBIO \_ Bir**](winbio-bir.md) per specificare dove si trovano le varie parti di un record di informazioni biometriche.</span><span class="sxs-lookup"><span data-stu-id="dc051-106">This structure is used by the [**WINBIO\_BIR**](winbio-bir.md) structure to specify where the various parts of a biometric information record are located.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc051-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dc051-107">Syntax</span></span>


```C++
typedef struct _WINBIO_BIR_DATA {
  ULONG Size;
  ULONG Offset;
} WINBIO_BIR_DATA;
```



## <a name="members"></a><span data-ttu-id="dc051-108">Members</span><span class="sxs-lookup"><span data-stu-id="dc051-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="dc051-109">**Dimensioni**</span><span class="sxs-lookup"><span data-stu-id="dc051-109">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="dc051-110">Dimensioni, in byte, delle informazioni biometriche.</span><span class="sxs-lookup"><span data-stu-id="dc051-110">Size, in bytes, of the biometric information.</span></span>

</dd> <dt>

<span data-ttu-id="dc051-111">**Offset**</span><span class="sxs-lookup"><span data-stu-id="dc051-111">**Offset**</span></span>
</dt> <dd>

<span data-ttu-id="dc051-112">Offset, in byte dall'inizio della struttura [**WINBIO \_ Bir**](winbio-bir.md) , delle informazioni biometriche.</span><span class="sxs-lookup"><span data-stu-id="dc051-112">Offset, in bytes from the beginning of the [**WINBIO\_BIR**](winbio-bir.md) structure, of the biometric information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dc051-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="dc051-113">Remarks</span></span>

<span data-ttu-id="dc051-114">L'uso degli offset anziché dei puntatori consente una semplice serializzazione di BIR e per una conversione meno complessa tra gli ambienti 32 e 64 bit o tra l'utente e la modalità kernel.</span><span class="sxs-lookup"><span data-stu-id="dc051-114">The use of offsets rather than pointers allows for easy serialization of the BIR and for less complicated translation between 32 and 64-bit environments or between user and kernel mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc051-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dc051-115">Requirements</span></span>



| <span data-ttu-id="dc051-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc051-116">Requirement</span></span> | <span data-ttu-id="dc051-117">Valore</span><span class="sxs-lookup"><span data-stu-id="dc051-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc051-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dc051-118">Minimum supported client</span></span><br/> | <span data-ttu-id="dc051-119">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="dc051-119">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="dc051-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dc051-120">Minimum supported server</span></span><br/> | <span data-ttu-id="dc051-121">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="dc051-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="dc051-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dc051-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc051-123"><dt>\_Tipi WinBio. h (includere WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dc051-123"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc051-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dc051-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc051-125">Strutture delle applicazioni client</span><span class="sxs-lookup"><span data-stu-id="dc051-125">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="dc051-126">**WINBIO \_ Bir**</span><span class="sxs-lookup"><span data-stu-id="dc051-126">**WINBIO\_BIR**</span></span>](winbio-bir.md)
</dt> <dt>

[<span data-ttu-id="dc051-127">**\_intestazione WINBIO bir \_**</span><span class="sxs-lookup"><span data-stu-id="dc051-127">**WINBIO\_BIR\_HEADER**</span></span>](winbio-bir-header.md)
</dt> </dl>

 

 





