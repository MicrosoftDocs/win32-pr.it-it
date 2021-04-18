---
title: Struttura WMDM_PROP_VALUES_ENUM
description: La \_ \_ struttura enum dei valori di WMDM Prop \_ contiene un set enumerato di valori validi per una particolare proprietà in una particolare configurazione di proprietà.
ms.assetid: 8094f3c0-a7ed-4e63-8503-aaac3fd9c012
keywords:
- Struttura di WMDM_PROP_VALUES_ENUM Windows Media Gestione dispositivi
topic_type:
- apiref
api_name:
- WMDM_PROP_VALUES_ENUM
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1c70088d57189dd36d360bc8910a15717d964ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325273"
---
# <a name="wmdm_prop_values_enum-structure"></a><span data-ttu-id="97e76-104">\_ \_ Struttura enum dei valori di WMDM Prop \_</span><span class="sxs-lookup"><span data-stu-id="97e76-104">WMDM\_PROP\_VALUES\_ENUM structure</span></span>

<span data-ttu-id="97e76-105">La **struttura \_ \_ \_ enum dei valori di WMDM prop** contiene un set enumerato di valori validi per una particolare proprietà in una particolare configurazione di proprietà.</span><span class="sxs-lookup"><span data-stu-id="97e76-105">The **WMDM\_PROP\_VALUES\_ENUM** structure contains an enumerated set of valid values for a particular property in a particular property configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="97e76-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="97e76-106">Syntax</span></span>


```C++
typedef struct _WMDM_PROP_VALUES_ENUM {
  UINT        cEnumValues;
  PROPVARIANT *pValues;
} WMDM_PROP_VALUES_ENUM;
```



## <a name="members"></a><span data-ttu-id="97e76-107">Members</span><span class="sxs-lookup"><span data-stu-id="97e76-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="97e76-108">**cEnumValues**</span><span class="sxs-lookup"><span data-stu-id="97e76-108">**cEnumValues**</span></span>
</dt> <dd>

<span data-ttu-id="97e76-109">Conteggio dei valori enumerati.</span><span class="sxs-lookup"><span data-stu-id="97e76-109">Count of enumerated values.</span></span>

</dd> <dt>

<span data-ttu-id="97e76-110">**pValues**</span><span class="sxs-lookup"><span data-stu-id="97e76-110">**pValues**</span></span>
</dt> <dd>

<span data-ttu-id="97e76-111">Puntatore a una matrice di valori.</span><span class="sxs-lookup"><span data-stu-id="97e76-111">Pointer to an array of values.</span></span> <span data-ttu-id="97e76-112">La dimensione della matrice è uguale al valore di **cEnumValues**.</span><span class="sxs-lookup"><span data-stu-id="97e76-112">The size of the array is equal to the value of **cEnumValues**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="97e76-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="97e76-113">Remarks</span></span>

<span data-ttu-id="97e76-114">Questa struttura viene utilizzata nella struttura **WMDM di \_ prop \_ desc** per descrivere un set enumerato di valori validi.</span><span class="sxs-lookup"><span data-stu-id="97e76-114">This structure is used in the **WMDM\_PROP\_DESC** structure to describe an enumerated set of valid values.</span></span> <span data-ttu-id="97e76-115">Un set enumerato di valori validi è applicabile quando WMDM \_ enum \_ prop \_ valid \_ Values \_ enum è selezionato nell'enumerazione **WMDM \_ enum \_ prop \_ valid \_ Values \_ form** Enumeration.</span><span class="sxs-lookup"><span data-stu-id="97e76-115">An enumerated set of valid values is applicable when WMDM\_ENUM\_PROP\_VALID\_VALUES\_ENUM is selected from the **WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM** enumeration.</span></span>

<span data-ttu-id="97e76-116">Il chiamante è necessario per liberare la memoria utilizzata da **pvalues**.</span><span class="sxs-lookup"><span data-stu-id="97e76-116">The caller is required to free the memory used by **pValues**.</span></span> <span data-ttu-id="97e76-117">Per un esempio di come eseguire questa operazione, vedere [**\_ \_ funzionalità di formato WMDM**](wmdm-format-capability.md).</span><span class="sxs-lookup"><span data-stu-id="97e76-117">For an example of how to do this, see [**WMDM\_FORMAT\_CAPABILITY**](wmdm-format-capability.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="97e76-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="97e76-118">Requirements</span></span>



| <span data-ttu-id="97e76-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="97e76-119">Requirement</span></span> | <span data-ttu-id="97e76-120">Valore</span><span class="sxs-lookup"><span data-stu-id="97e76-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="97e76-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="97e76-121">Header</span></span><br/> | <dl> <span data-ttu-id="97e76-122"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="97e76-122"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97e76-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="97e76-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97e76-124">**IWMDMDevice3::GetFormatCapability**</span><span class="sxs-lookup"><span data-stu-id="97e76-124">**IWMDMDevice3::GetFormatCapability**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[<span data-ttu-id="97e76-125">**\_ \_ \_ \_ form valori validi dell'enumerazione \_ WMDM**</span><span class="sxs-lookup"><span data-stu-id="97e76-125">**WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM**</span></span>](wmdm-enum-prop-valid-values-form.md)
</dt> <dt>

[<span data-ttu-id="97e76-126">**\_funzionalità di formato WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="97e76-126">**WMDM\_FORMAT\_CAPABILITY**</span></span>](wmdm-format-capability.md)
</dt> <dt>

[<span data-ttu-id="97e76-127">**\_configurazione della prop WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="97e76-127">**WMDM\_PROP\_CONFIG**</span></span>](wmdm-prop-config.md)
</dt> <dt>

[<span data-ttu-id="97e76-128">**WMDM \_ prop \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="97e76-128">**WMDM\_PROP\_DESC**</span></span>](wmdm-prop-desc.md)
</dt> <dt>

[<span data-ttu-id="97e76-129">**WMDM \_ \_ intervallo valori \_ prop**</span><span class="sxs-lookup"><span data-stu-id="97e76-129">**WMDM\_PROP\_VALUES\_RANGE**</span></span>](wmdm-prop-values-range.md)
</dt> <dt>

[<span data-ttu-id="97e76-130">**Strutture**</span><span class="sxs-lookup"><span data-stu-id="97e76-130">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





