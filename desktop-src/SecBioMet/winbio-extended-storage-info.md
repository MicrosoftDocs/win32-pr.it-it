---
title: Struttura WINBIO_EXTENDED_STORAGE_INFO ( \_ tipi WINBIO. h)
description: Contiene informazioni sulle funzionalità e i requisiti di registrazione dell'adattatore di archiviazione per un'unità biometrica.
ms.assetid: 7A648610-E947-4967-A9AF-C8A9C0B81D92
keywords:
- Struttura di WINBIO_EXTENDED_STORAGE_INFO Windows Biometric Framework API
- API Windows Biometric Framework puntatore alla struttura PWINBIO_EXTENDED_STORAGE_INFO
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_STORAGE_INFO
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ac2559717a2040cfb617e85e0a51495be1b5987
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963865"
---
# <a name="winbio_extended_storage_info-structure"></a><span data-ttu-id="83061-105">\_Struttura delle \_ informazioni di archiviazione estesa WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="83061-105">WINBIO\_EXTENDED\_STORAGE\_INFO structure</span></span>

<span data-ttu-id="83061-106">Contiene informazioni sulle funzionalità e i requisiti di registrazione dell'adattatore di archiviazione per un'unità biometrica.</span><span class="sxs-lookup"><span data-stu-id="83061-106">Contains information about the capabilities and enrollment requirements of the storage adapter for a biometric unit.</span></span>

## <a name="syntax"></a><span data-ttu-id="83061-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="83061-107">Syntax</span></span>


```C++
typedef struct _WINBIO_EXTENDED_STORAGE_INFO {
  WINBIO_CAPABILITIES   GenericStorageCapabilities;
  WINBIO_BIOMETRIC_TYPE Factor;
  union {
    ULONG32 Null;
    struct {
      WINBIO_CAPABILITIES Capabilities;
    } FacialFeatures;
    struct {
      WINBIO_CAPABILITIES Capabilities;
    } Fingerprint;
    struct {
      WINBIO_CAPABILITIES Capabilities;
    } Iris;
    struct {
      WINBIO_CAPABILITIES Capabilities;
    } Voice;
  } Specific;
} WINBIO_EXTENDED_STORAGE_INFO, *PWINBIO_EXTENDED_STORAGE_INFO;
```



## <a name="members"></a><span data-ttu-id="83061-108">Members</span><span class="sxs-lookup"><span data-stu-id="83061-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="83061-109">**GenericStorageCapabilities**</span><span class="sxs-lookup"><span data-stu-id="83061-109">**GenericStorageCapabilities**</span></span>
</dt> <dd>

<span data-ttu-id="83061-110">Funzionalità generiche del componente di archiviazione connesso a un'unità biometrica specifica.</span><span class="sxs-lookup"><span data-stu-id="83061-110">The generic capabilities of the storage component that is connected to a specific biometric unit.</span></span>

</dd> <dt>

<span data-ttu-id="83061-111">**Fattore**</span><span class="sxs-lookup"><span data-stu-id="83061-111">**Factor**</span></span>
</dt> <dd>

<span data-ttu-id="83061-112">Tipo di unità biometrica per la quale questa struttura contiene informazioni sulle funzionalità e i requisiti di registrazione dell'adattatore di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="83061-112">The type of biometric unit for which this structure contains information about capabilities and enrollment requirements of the storage adapter.</span></span> <span data-ttu-id="83061-113">Se, ad esempio, il valore del membro **Factor** è **WINBIO \_ , \_** la struttura delle **\_ informazioni di \_ archiviazione \_ estesa WINBIO** si applica a un lettore di impronte digitali e contiene le informazioni rilevanti nella struttura **specifico. Fingerprint** .</span><span class="sxs-lookup"><span data-stu-id="83061-113">For example, if the value of the **Factor** member is **WINBIO\_TYPE\_FINGERPRINT**, the **WINBIO\_EXTENDED\_STORAGE\_INFO** structure applies to a fingerprint reader and contains the relevant information in the **Specifc.Fingerprint** structure.</span></span>

</dd> <dt>

<span data-ttu-id="83061-114">**Specifica**</span><span class="sxs-lookup"><span data-stu-id="83061-114">**Specific**</span></span>
</dt> <dd>

<span data-ttu-id="83061-115">Informazioni sulle funzionalità e i requisiti di registrazione dell'adattatore di archiviazione per un'unità biometrica correlata a un fattore biometrico specifico.</span><span class="sxs-lookup"><span data-stu-id="83061-115">Information about the capabilities and enrollment requirements of the storage adapter for a biometric unit related to a specific biometric factor.</span></span>

<dl> <dt>

<span data-ttu-id="83061-116">**Null**</span><span class="sxs-lookup"><span data-stu-id="83061-116">**Null**</span></span>
</dt> <dd>

<span data-ttu-id="83061-117">Riservato.</span><span class="sxs-lookup"><span data-stu-id="83061-117">Reserved.</span></span> <span data-ttu-id="83061-118">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="83061-118">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="83061-119">**FacialFeatures**</span><span class="sxs-lookup"><span data-stu-id="83061-119">**FacialFeatures**</span></span>
</dt> <dd>

<span data-ttu-id="83061-120">Informazioni sulle funzionalità e i requisiti di registrazione dell'adattatore di archiviazione per un'unità biometrica correlata alle funzionalità facciali.</span><span class="sxs-lookup"><span data-stu-id="83061-120">Information about the capabilities and enrollment requirements of the storage adapter for a biometric unit related to facial features.</span></span>

<dl> <dt>

<span data-ttu-id="83061-121">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="83061-121">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="83061-122">Funzionalità di riconoscimento facciali del componente di archiviazione connesso a un'unità biometrica specifica.</span><span class="sxs-lookup"><span data-stu-id="83061-122">The facial recognition capabilities of the storage component that is connected to a specific biometric unit.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="83061-123">**Impronta digitale**</span><span class="sxs-lookup"><span data-stu-id="83061-123">**Fingerprint**</span></span>
</dt> <dd>

<span data-ttu-id="83061-124">Informazioni sulle funzionalità e i requisiti di registrazione dell'adattatore di archiviazione per un'unità biometrica relativa ai modelli di impronta digitale.</span><span class="sxs-lookup"><span data-stu-id="83061-124">Information about the capabilities and enrollment requirements of the storage adapter for a biometric unit related to fingerprint patterns.</span></span>

<dl> <dt>

<span data-ttu-id="83061-125">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="83061-125">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="83061-126">Funzionalità di riconoscimento delle impronte digitali del componente di archiviazione connesso a un'unità biometrica specifica</span><span class="sxs-lookup"><span data-stu-id="83061-126">The fingerprint recognition capabilities of the storage component that is connected to a specific biometric unit</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="83061-127">**Iris**</span><span class="sxs-lookup"><span data-stu-id="83061-127">**Iris**</span></span>
</dt> <dd>

<span data-ttu-id="83061-128">Informazioni sulle funzionalità e i requisiti di registrazione dell'adattatore di archiviazione per un'unità biometrica relativa ai modelli Iris.</span><span class="sxs-lookup"><span data-stu-id="83061-128">Information about the capabilities and enrollment requirements of the storage adapter for a biometric unit related to iris patterns.</span></span>

<dl> <dt>

<span data-ttu-id="83061-129">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="83061-129">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="83061-130">Funzionalità di riconoscimento Iris del componente di archiviazione connesso a un'unità biometrica specifica</span><span class="sxs-lookup"><span data-stu-id="83061-130">The iris recognition capabilities of the storage component that is connected to a specific biometric unit</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="83061-131">**Chiamata vocale**</span><span class="sxs-lookup"><span data-stu-id="83061-131">**Voice**</span></span>
</dt> <dd>

<span data-ttu-id="83061-132">Informazioni sulle funzionalità e i requisiti di registrazione dell'adattatore di archiviazione per un'unità biometrica relativa ai modelli vocali.</span><span class="sxs-lookup"><span data-stu-id="83061-132">Information about the capabilities and enrollment requirements of the storage adapter for a biometric unit related to voice patterns.</span></span>

<dl> <dt>

<span data-ttu-id="83061-133">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="83061-133">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="83061-134">Funzionalità di riconoscimento vocale del componente di archiviazione connesso a un'unità biometrica specifica</span><span class="sxs-lookup"><span data-stu-id="83061-134">The voice recognition capabilities of the storage component that is connected to a specific biometric unit</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="83061-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="83061-135">Requirements</span></span>



| <span data-ttu-id="83061-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="83061-136">Requirement</span></span> | <span data-ttu-id="83061-137">Valore</span><span class="sxs-lookup"><span data-stu-id="83061-137">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83061-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83061-138">Minimum supported client</span></span><br/> | <span data-ttu-id="83061-139">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="83061-139">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="83061-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83061-140">Minimum supported server</span></span><br/> | <span data-ttu-id="83061-141">\[Solo app desktop Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="83061-141">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="83061-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="83061-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="83061-143"><dt>WinBio \_ types. h (includere WinBio. h per le applicazioni client o WinBio \_ Adapters. h per gli adapter)</dt></span><span class="sxs-lookup"><span data-stu-id="83061-143"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83061-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="83061-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83061-145">**\_ \_ Costanti di tipo biometrico WINBIO**</span><span class="sxs-lookup"><span data-stu-id="83061-145">**WINBIO\_BIOMETRIC\_TYPE Constants**</span></span>](winbio-biometric-type-constants.md)
</dt> <dt>

[<span data-ttu-id="83061-146">**\_Costanti della funzionalità WINBIO**</span><span class="sxs-lookup"><span data-stu-id="83061-146">**WINBIO\_CAPABILITY Constants**</span></span>](winbio-capability-constants.md)
</dt> </dl>

 

 





