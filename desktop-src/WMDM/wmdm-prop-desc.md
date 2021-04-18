---
title: Struttura WMDM_PROP_DESC
description: La \_ struttura WMDM Prop \_ desc descrive i valori validi di una proprietà in una particolare configurazione della proprietà.
ms.assetid: e4766e1e-6c1b-4a2d-ad2e-c07035ca2be2
keywords:
- Struttura di WMDM_PROP_DESC Windows Media Gestione dispositivi
topic_type:
- apiref
api_name:
- WMDM_PROP_DESC
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98f6ea406a3d48d0ed65098d66721fcadbb98411
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331899"
---
# <a name="wmdm_prop_desc-structure"></a><span data-ttu-id="41334-104">\_Struttura WMDM Prop \_ DESC</span><span class="sxs-lookup"><span data-stu-id="41334-104">WMDM\_PROP\_DESC structure</span></span>

<span data-ttu-id="41334-105">La struttura **WMDM \_ prop \_ desc** descrive i valori validi di una proprietà in una particolare configurazione della proprietà.</span><span class="sxs-lookup"><span data-stu-id="41334-105">The **WMDM\_PROP\_DESC** structure describes valid values of a property in a particular property configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="41334-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="41334-106">Syntax</span></span>


```C++
typedef struct _WMDM_PROP_DESC {
  LPWSTR                           pwszPropName;
  WMDM_ENUM_PROP_VALID_VALUES_FORM ValidValuesForm;
  union  {
    WMDM_PROP_VALUES_RANGE ValidValuesRange;
    WMDM_PROP_VALUES_ENUM  EnumeratedValidValues;
  } ValidValues;
} WMDM_PROP_DESC;
```



## <a name="members"></a><span data-ttu-id="41334-107">Members</span><span class="sxs-lookup"><span data-stu-id="41334-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="41334-108">**pwszPropName**</span><span class="sxs-lookup"><span data-stu-id="41334-108">**pwszPropName**</span></span>
</dt> <dd>

<span data-ttu-id="41334-109">Nome della proprietà.</span><span class="sxs-lookup"><span data-stu-id="41334-109">Name of the property.</span></span> <span data-ttu-id="41334-110">L'applicazione deve liberare questa memoria quando viene eseguita utilizzandola.</span><span class="sxs-lookup"><span data-stu-id="41334-110">The application must free this memory when it is done using it.</span></span>

</dd> <dt>

<span data-ttu-id="41334-111">**ValidValuesForm**</span><span class="sxs-lookup"><span data-stu-id="41334-111">**ValidValuesForm**</span></span>
</dt> <dd>

<span data-ttu-id="41334-112">Valore di enumerazione del [**\_ modulo WMDM enum \_ prop \_ \_ valori \_ validi**](wmdm-enum-prop-valid-values-form.md) che descrive il tipo di valori, ad esempio un intervallo o un elenco.</span><span class="sxs-lookup"><span data-stu-id="41334-112">An [**WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM**](wmdm-enum-prop-valid-values-form.md) enumeration value describing the type of values, such as a range or list.</span></span> <span data-ttu-id="41334-113">Il valore di questa enumerazione determina quale variabile membro viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="41334-113">The value of this enumeration determines which member variable is used.</span></span>

</dd> <dt>

<span data-ttu-id="41334-114">**ValidValues**</span><span class="sxs-lookup"><span data-stu-id="41334-114">**ValidValues**</span></span>
</dt> <dd>

<span data-ttu-id="41334-115">Include i valori validi della proprietà in una configurazione di proprietà specifica.</span><span class="sxs-lookup"><span data-stu-id="41334-115">Holds the valid values of the property in a particular property configuration.</span></span> <span data-ttu-id="41334-116">Questo membro include uno dei tre elementi seguenti: il valore di enumerazione WMDM \_ enum \_ prop \_ valid \_ Values \_ any, il membro **ValidValuesRange** o il membro **EnumeratedValidValues**.</span><span class="sxs-lookup"><span data-stu-id="41334-116">This member holds one of three items: the enumeration value WMDM\_ENUM\_PROP\_VALID\_VALUES\_ANY; the member **ValidValuesRange**; or the member **EnumeratedValidValues**.</span></span> <span data-ttu-id="41334-117">Il valore o il membro è indicato da **ValidValuesForm**.</span><span class="sxs-lookup"><span data-stu-id="41334-117">The value or member is indicated by **ValidValuesForm**.</span></span>

<dl> <dt>

<span data-ttu-id="41334-118">**ValidValuesRange**</span><span class="sxs-lookup"><span data-stu-id="41334-118">**ValidValuesRange**</span></span>
</dt> <dd>

<span data-ttu-id="41334-119">Una struttura [**WMDM dell' \_ \_ \_ intervallo di valori prop**](wmdm-prop-values-range.md) contenente un intervallo di valori validi.</span><span class="sxs-lookup"><span data-stu-id="41334-119">A [**WMDM\_PROP\_VALUES\_RANGE**](wmdm-prop-values-range.md) structure containing a range of valid values.</span></span> <span data-ttu-id="41334-120">Questa operazione è presente solo quando **ValidValuesForm** è impostato su WMDM \_ enum \_ prop \_ valid \_ Values \_ Range.</span><span class="sxs-lookup"><span data-stu-id="41334-120">This is present only when **ValidValuesForm** is set to WMDM\_ENUM\_PROP\_VALID\_VALUES\_RANGE.</span></span> <span data-ttu-id="41334-121">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="41334-121">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="41334-122">**EnumeratedValidValues**</span><span class="sxs-lookup"><span data-stu-id="41334-122">**EnumeratedValidValues**</span></span>
</dt> <dd>

<span data-ttu-id="41334-123">Una struttura di [**\_ \_ \_ enumerazione di valori prop WMDM**](wmdm-prop-values-enum.md) contenente un set enumerato di valori validi.</span><span class="sxs-lookup"><span data-stu-id="41334-123">A [**WMDM\_PROP\_VALUES\_ENUM**](wmdm-prop-values-enum.md) structure containing an enumerated set of valid values.</span></span> <span data-ttu-id="41334-124">Questa operazione è presente solo quando **ValidValuesForm** è impostato su WMDM \_ enum \_ prop \_ valid \_ Values \_ enum.</span><span class="sxs-lookup"><span data-stu-id="41334-124">This is present only when **ValidValuesForm** is set to WMDM\_ENUM\_PROP\_VALID\_VALUES\_ENUM.</span></span> <span data-ttu-id="41334-125">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="41334-125">See Remarks.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="41334-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="41334-126">Remarks</span></span>

<span data-ttu-id="41334-127">La struttura **WMDM \_ prop \_ desc** contiene una descrizione della proprietà costituita da un nome di proprietà e dai relativi valori validi in una particolare configurazione.</span><span class="sxs-lookup"><span data-stu-id="41334-127">The **WMDM\_PROP\_DESC** structure contains a property description that consists of a property name and its valid values in a particular configuration.</span></span>

<span data-ttu-id="41334-128">Il chiamante è necessario per liberare la memoria usata da **ValidValuesRange** o **EnumeratedValues**.</span><span class="sxs-lookup"><span data-stu-id="41334-128">The caller is required to free the memory used by **ValidValuesRange** or **EnumeratedValues**.</span></span> <span data-ttu-id="41334-129">Per un esempio di come eseguire questa operazione, vedere [**\_ \_ funzionalità di formato WMDM**](wmdm-format-capability.md).</span><span class="sxs-lookup"><span data-stu-id="41334-129">For an example of how to do this, see [**WMDM\_FORMAT\_CAPABILITY**](wmdm-format-capability.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="41334-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="41334-130">Requirements</span></span>



| <span data-ttu-id="41334-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="41334-131">Requirement</span></span> | <span data-ttu-id="41334-132">Valore</span><span class="sxs-lookup"><span data-stu-id="41334-132">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="41334-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="41334-133">Header</span></span><br/> | <dl> <span data-ttu-id="41334-134"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="41334-134"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41334-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="41334-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41334-136">**IWMDMDevice3::GetFormatCapability**</span><span class="sxs-lookup"><span data-stu-id="41334-136">**IWMDMDevice3::GetFormatCapability**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[<span data-ttu-id="41334-137">**\_ \_ \_ \_ form valori validi dell'enumerazione \_ WMDM**</span><span class="sxs-lookup"><span data-stu-id="41334-137">**WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM**</span></span>](wmdm-enum-prop-valid-values-form.md)
</dt> <dt>

[<span data-ttu-id="41334-138">**\_funzionalità di formato WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="41334-138">**WMDM\_FORMAT\_CAPABILITY**</span></span>](wmdm-format-capability.md)
</dt> <dt>

[<span data-ttu-id="41334-139">**\_configurazione della prop WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="41334-139">**WMDM\_PROP\_CONFIG**</span></span>](wmdm-prop-config.md)
</dt> <dt>

[<span data-ttu-id="41334-140">**\_ \_ enumerazione valori Prop \_ WMDM**</span><span class="sxs-lookup"><span data-stu-id="41334-140">**WMDM\_PROP\_VALUES\_ENUM**</span></span>](wmdm-prop-values-enum.md)
</dt> <dt>

[<span data-ttu-id="41334-141">**WMDM \_ \_ intervallo valori \_ prop**</span><span class="sxs-lookup"><span data-stu-id="41334-141">**WMDM\_PROP\_VALUES\_RANGE**</span></span>](wmdm-prop-values-range.md)
</dt> <dt>

[<span data-ttu-id="41334-142">**Strutture**</span><span class="sxs-lookup"><span data-stu-id="41334-142">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





