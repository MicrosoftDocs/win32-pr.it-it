---
title: Struttura WMDM_PROP_VALUES_RANGE
description: La \_ struttura dell'intervallo WMDM Prop \_ Values \_ descrive un intervallo di valori validi per una particolare proprietà in una particolare configurazione della proprietà.
ms.assetid: fb823a66-cc9c-4632-a4f0-03c7255c3ccb
keywords:
- Struttura di WMDM_PROP_VALUES_RANGE Windows Media Gestione dispositivi
topic_type:
- apiref
api_name:
- WMDM_PROP_VALUES_RANGE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ba82a1067db97e93fff2845e69e89f978548b73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325272"
---
# <a name="wmdm_prop_values_range-structure"></a><span data-ttu-id="76c6d-104">\_Struttura dell' \_ intervallo di valori della prop WMDM \_</span><span class="sxs-lookup"><span data-stu-id="76c6d-104">WMDM\_PROP\_VALUES\_RANGE structure</span></span>

<span data-ttu-id="76c6d-105">La struttura dell' **\_ \_ \_ intervallo WMDM prop values** descrive un intervallo di valori validi per una particolare proprietà in una particolare configurazione della proprietà.</span><span class="sxs-lookup"><span data-stu-id="76c6d-105">The **WMDM\_PROP\_VALUES\_RANGE** structure describes a range of valid values for a particular property in a particular property configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="76c6d-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="76c6d-106">Syntax</span></span>


```C++
typedef struct _WMDM_PROP_VALUES_RANGE {
  PROPVARIANT rangeMin;
  PROPVARIANT rangeMax;
  PROPVARIANT rangeStep;
} WMDM_PROP_VALUES_RANGE;
```



## <a name="members"></a><span data-ttu-id="76c6d-107">Members</span><span class="sxs-lookup"><span data-stu-id="76c6d-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="76c6d-108">**rangeMin**</span><span class="sxs-lookup"><span data-stu-id="76c6d-108">**rangeMin**</span></span>
</dt> <dd>

<span data-ttu-id="76c6d-109">Valore minimo nell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="76c6d-109">Minimum value in the range.</span></span>

</dd> <dt>

<span data-ttu-id="76c6d-110">**rangeMax**</span><span class="sxs-lookup"><span data-stu-id="76c6d-110">**rangeMax**</span></span>
</dt> <dd>

<span data-ttu-id="76c6d-111">Valore massimo nell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="76c6d-111">Maximum value in the range.</span></span>

</dd> <dt>

<span data-ttu-id="76c6d-112">**rangeStep**</span><span class="sxs-lookup"><span data-stu-id="76c6d-112">**rangeStep**</span></span>
</dt> <dd>

<span data-ttu-id="76c6d-113">Dimensioni del passaggio in cui i valori validi vengono incrementati dal valore minimo al valore massimo.</span><span class="sxs-lookup"><span data-stu-id="76c6d-113">The step size in which valid values increment from the minimum value to the maximum value.</span></span> <span data-ttu-id="76c6d-114">Questo consente di specificare valori discreti consentiti in un intervallo.</span><span class="sxs-lookup"><span data-stu-id="76c6d-114">This permits specifying discrete permissible values in a range.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="76c6d-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="76c6d-115">Remarks</span></span>

<span data-ttu-id="76c6d-116">Questa struttura viene utilizzata nella struttura [**WMDM di \_ prop \_ desc**](wmdm-prop-desc.md) per descrivere un intervallo di valori validi.</span><span class="sxs-lookup"><span data-stu-id="76c6d-116">This structure is used in the [**WMDM\_PROP\_DESC**](wmdm-prop-desc.md) structure to describe a range of valid values.</span></span> <span data-ttu-id="76c6d-117">Un intervallo di valori validi è applicabile quando WMDM \_ enum \_ prop \_ valid \_ Values \_ enum è selezionato dall'enumerazione [**WMDM \_ enum \_ prop \_ valid \_ Values \_ form**](wmdm-enum-prop-valid-values-form.md) Enumeration.</span><span class="sxs-lookup"><span data-stu-id="76c6d-117">A range of valid values is applicable when WMDM\_ENUM\_PROP\_VALID\_VALUES\_ENUM is selected from the [**WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM**](wmdm-enum-prop-valid-values-form.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="76c6d-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="76c6d-118">Requirements</span></span>



| <span data-ttu-id="76c6d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="76c6d-119">Requirement</span></span> | <span data-ttu-id="76c6d-120">Valore</span><span class="sxs-lookup"><span data-stu-id="76c6d-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="76c6d-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="76c6d-121">Header</span></span><br/> | <dl> <span data-ttu-id="76c6d-122"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="76c6d-122"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76c6d-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="76c6d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76c6d-124">**IWMDMDevice3::GetFormatCapability**</span><span class="sxs-lookup"><span data-stu-id="76c6d-124">**IWMDMDevice3::GetFormatCapability**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[<span data-ttu-id="76c6d-125">**\_ \_ \_ \_ form valori validi dell'enumerazione \_ WMDM**</span><span class="sxs-lookup"><span data-stu-id="76c6d-125">**WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM**</span></span>](wmdm-enum-prop-valid-values-form.md)
</dt> <dt>

[<span data-ttu-id="76c6d-126">**\_funzionalità di formato WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="76c6d-126">**WMDM\_FORMAT\_CAPABILITY**</span></span>](wmdm-format-capability.md)
</dt> <dt>

[<span data-ttu-id="76c6d-127">**\_configurazione della prop WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="76c6d-127">**WMDM\_PROP\_CONFIG**</span></span>](wmdm-prop-config.md)
</dt> <dt>

[<span data-ttu-id="76c6d-128">**WMDM \_ prop \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="76c6d-128">**WMDM\_PROP\_DESC**</span></span>](wmdm-prop-desc.md)
</dt> <dt>

[<span data-ttu-id="76c6d-129">**\_ \_ enumerazione valori Prop \_ WMDM**</span><span class="sxs-lookup"><span data-stu-id="76c6d-129">**WMDM\_PROP\_VALUES\_ENUM**</span></span>](wmdm-prop-values-enum.md)
</dt> <dt>

[<span data-ttu-id="76c6d-130">**Strutture**</span><span class="sxs-lookup"><span data-stu-id="76c6d-130">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





