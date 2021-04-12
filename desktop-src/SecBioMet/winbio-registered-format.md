---
title: Struttura WINBIO_REGISTERED_FORMAT ( \_ tipi WINBIO. h)
description: Specifica un formato dati registrato come coppia proprietario/formato.
ms.assetid: a178840e-81cc-4dd3-9d80-a181fa7fa888
keywords:
- Struttura di WINBIO_REGISTERED_FORMAT Windows Biometric Framework API
- API Windows Biometric Framework puntatore alla struttura PWINBIO_REGISTERED_FORMAT
topic_type:
- apiref
api_name:
- WINBIO_REGISTERED_FORMAT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f45293fe95627c7dfad4c9c51eb7fa74ad1738c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517806"
---
# <a name="winbio_registered_format-structure"></a><span data-ttu-id="7113c-105">\_Struttura del \_ formato registrato WINBIO</span><span class="sxs-lookup"><span data-stu-id="7113c-105">WINBIO\_REGISTERED\_FORMAT structure</span></span>

<span data-ttu-id="7113c-106">La struttura del **\_ \_ formato registrato WINBIO** specifica un formato dati registrato come coppia proprietario/formato.</span><span class="sxs-lookup"><span data-stu-id="7113c-106">The **WINBIO\_REGISTERED\_FORMAT** structure specifies a registered data format as an owner/format pair.</span></span>

## <a name="syntax"></a><span data-ttu-id="7113c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7113c-107">Syntax</span></span>


```C++
typedef struct _WINBIO_REGISTERED_FORMAT {
  USHORT Owner;
  USHORT Type;
} WINBIO_REGISTERED_FORMAT, *PWINBIO_REGISTERED_FORMAT;
```



## <a name="members"></a><span data-ttu-id="7113c-108">Members</span><span class="sxs-lookup"><span data-stu-id="7113c-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="7113c-109">**Proprietario**</span><span class="sxs-lookup"><span data-stu-id="7113c-109">**Owner**</span></span>
</dt> <dd>

<span data-ttu-id="7113c-110">Valore proprietario assegnato a IBROLI (International Biometric Industry Association).</span><span class="sxs-lookup"><span data-stu-id="7113c-110">An IBIA (International Biometric Industry Association) assigned owner value.</span></span>

</dd> <dt>

<span data-ttu-id="7113c-111">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7113c-111">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="7113c-112">Formato assegnato dal proprietario.</span><span class="sxs-lookup"><span data-stu-id="7113c-112">An owner assigned format.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7113c-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="7113c-113">Remarks</span></span>

<span data-ttu-id="7113c-114">Poiché Windows supporta attualmente solo i lettori di impronte digitali, nella struttura del **\_ \_ formato registrato WINBIO** devono essere usati i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="7113c-114">Because Windows currently supports only fingerprint readers, the following values should be used in the **WINBIO\_REGISTERED\_FORMAT** structure.</span></span>



| <span data-ttu-id="7113c-115">Costante</span><span class="sxs-lookup"><span data-stu-id="7113c-115">Constant</span></span>                                    | <span data-ttu-id="7113c-116">Significato</span><span class="sxs-lookup"><span data-stu-id="7113c-116">Meaning</span></span>                                                                                                               |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7113c-117">\_Proprietario del \_ formato ANSI 381 \_ \_ di WINBIO</span><span class="sxs-lookup"><span data-stu-id="7113c-117">WINBIO\_ANSI\_381\_FORMAT\_OWNER</span></span><br/> | <span data-ttu-id="7113c-118">InterNational Committee for Information Technology Standards (INCIs) Technical Committee M1 (biometria).</span><span class="sxs-lookup"><span data-stu-id="7113c-118">InterNational Committee for Information Technology Standards (INCITS) technical committee M1 (biometrics).</span></span><br/> |
| <span data-ttu-id="7113c-119">\_Tipo di \_ formato ANSI 381 \_ \_ di WINBIO</span><span class="sxs-lookup"><span data-stu-id="7113c-119">WINBIO\_ANSI\_381\_FORMAT\_TYPE</span></span><br/>  | <span data-ttu-id="7113c-120">ANSI INCIs 381 formato di interscambio dati basato su immagine Finger.</span><span class="sxs-lookup"><span data-stu-id="7113c-120">ANSI INCITS 381 finger image based data interchange format.</span></span><br/>                                                |



 

## <a name="requirements"></a><span data-ttu-id="7113c-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7113c-121">Requirements</span></span>



| <span data-ttu-id="7113c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="7113c-122">Requirement</span></span> | <span data-ttu-id="7113c-123">Valore</span><span class="sxs-lookup"><span data-stu-id="7113c-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7113c-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7113c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7113c-125">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="7113c-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="7113c-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7113c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7113c-127">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="7113c-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="7113c-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7113c-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="7113c-129"><dt>\_Tipi WinBio. h (includere WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7113c-129"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7113c-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7113c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7113c-131">Strutture delle applicazioni client</span><span class="sxs-lookup"><span data-stu-id="7113c-131">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="7113c-132">**\_Costanti di \_ formato ANSI 381 di WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="7113c-132">**WINBIO\_ANSI\_381\_FORMAT Constants**</span></span>](winbio-ansi-381-format-constants.md)
</dt> <dt>

[<span data-ttu-id="7113c-133">**WINBIO \_ BDB \_ ANSI \_ 381 \_ intestazione**</span><span class="sxs-lookup"><span data-stu-id="7113c-133">**WINBIO\_BDB\_ANSI\_381\_HEADER**</span></span>](winbio-bdb-ansi-381-header.md)
</dt> <dt>

[<span data-ttu-id="7113c-134">**\_intestazione WINBIO bir \_**</span><span class="sxs-lookup"><span data-stu-id="7113c-134">**WINBIO\_BIR\_HEADER**</span></span>](winbio-bir-header.md)
</dt> </dl>

 

 





