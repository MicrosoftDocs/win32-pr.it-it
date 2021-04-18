---
title: Enumerazione WMDM_ENUM_PROP_VALID_VALUES_FORM
description: Il \_ \_ \_ tipo di enumerazione del modulo WMDM enum prop valid \_ Values \_ descrive le possibili forme di valori validi per una proprietà.
ms.assetid: 49d174b4-c8a3-4c16-ad21-4b66dcf8088f
keywords:
- Enumerazione WMDM_ENUM_PROP_VALID_VALUES_FORM Windows Media Gestione dispositivi
topic_type:
- apiref
api_name:
- WMDM_ENUM_PROP_VALID_VALUES_FORM
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d7db971f359a9cead2aae6083a934086d42c481
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324587"
---
# <a name="wmdm_enum_prop_valid_values_form-enumeration"></a><span data-ttu-id="36712-104">\_ \_ \_ \_ \_ Enumerazione form valori validi dell'enumerazione WMDM</span><span class="sxs-lookup"><span data-stu-id="36712-104">WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM enumeration</span></span>

<span data-ttu-id="36712-105">Il tipo di enumerazione del **\_ modulo WMDM enum \_ prop \_ valid \_ Values \_** descrive le possibili forme di valori validi per una proprietà.</span><span class="sxs-lookup"><span data-stu-id="36712-105">The **WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM** enumeration type describes possible forms of valid values for a property.</span></span>

## <a name="syntax"></a><span data-ttu-id="36712-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="36712-106">Syntax</span></span>


```C++
typedef enum _WMDM_ENUM_PROP_VALID_VALUES_FORM { 
  WMDM_ENUM_PROP_VALID_VALUES_ANY,
  WMDM_ENUM_PROP_VALID_VALUES_RANGE,
  WMDM_ENUM_PROP_VALID_VALUES_ENUM
} WMDM_ENUM_PROP_VALID_VALUES_FORM;
```



## <a name="constants"></a><span data-ttu-id="36712-107">Costanti</span><span class="sxs-lookup"><span data-stu-id="36712-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="36712-108"><span id="WMDM_ENUM_PROP_VALID_VALUES_ANY"></span><span id="wmdm_enum_prop_valid_values_any"></span>**WMDM \_ enum \_ prop \_ \_ valori validi \_ any**</span><span class="sxs-lookup"><span data-stu-id="36712-108"><span id="WMDM_ENUM_PROP_VALID_VALUES_ANY"></span><span id="wmdm_enum_prop_valid_values_any"></span>**WMDM\_ENUM\_PROP\_VALID\_VALUES\_ANY**</span></span>
</dt> <dd>

<span data-ttu-id="36712-109">Tutti i valori sono validi.</span><span class="sxs-lookup"><span data-stu-id="36712-109">All values are valid.</span></span>

</dd> <dt>

<span data-ttu-id="36712-110"><span id="WMDM_ENUM_PROP_VALID_VALUES_RANGE"></span><span id="wmdm_enum_prop_valid_values_range"></span>**WMDM \_ enum \_ prop \_ \_ valori validi \_ intervallo**</span><span class="sxs-lookup"><span data-stu-id="36712-110"><span id="WMDM_ENUM_PROP_VALID_VALUES_RANGE"></span><span id="wmdm_enum_prop_valid_values_range"></span>**WMDM\_ENUM\_PROP\_VALID\_VALUES\_RANGE**</span></span>
</dt> <dd>

<span data-ttu-id="36712-111">I valori validi sono espressi come un intervallo.</span><span class="sxs-lookup"><span data-stu-id="36712-111">Valid values are expressed as a range.</span></span> <span data-ttu-id="36712-112">Per informazioni dettagliate, vedere la struttura [**WMDM \_ prop \_ Values \_ Range**](wmdm-prop-values-range.md) .</span><span class="sxs-lookup"><span data-stu-id="36712-112">For detailed information, see the [**WMDM\_PROP\_VALUES\_RANGE**](wmdm-prop-values-range.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="36712-113"><span id="WMDM_ENUM_PROP_VALID_VALUES_ENUM"></span><span id="wmdm_enum_prop_valid_values_enum"></span>**\_enumerazione WMDM enum \_ prop \_ valid \_ Values \_**</span><span class="sxs-lookup"><span data-stu-id="36712-113"><span id="WMDM_ENUM_PROP_VALID_VALUES_ENUM"></span><span id="wmdm_enum_prop_valid_values_enum"></span>**WMDM\_ENUM\_PROP\_VALID\_VALUES\_ENUM**</span></span>
</dt> <dd>

<span data-ttu-id="36712-114">I valori validi sono un set enumerato.</span><span class="sxs-lookup"><span data-stu-id="36712-114">Valid values are an enumerated set.</span></span> <span data-ttu-id="36712-115">Per informazioni dettagliate, vedere la struttura di [**\_ \_ \_ enumerazione WMDM prop values**](wmdm-prop-values-enum.md) .</span><span class="sxs-lookup"><span data-stu-id="36712-115">For detailed information, see the [**WMDM\_PROP\_VALUES\_ENUM**](wmdm-prop-values-enum.md) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="36712-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="36712-116">Remarks</span></span>

<span data-ttu-id="36712-117">Questa enumerazione viene usata nella struttura [**WMDM \_ prop \_ desc**](wmdm-prop-desc.md) per specificare il formato dei valori validi per una proprietà.</span><span class="sxs-lookup"><span data-stu-id="36712-117">This enumeration is used in the [**WMDM\_PROP\_DESC**](wmdm-prop-desc.md) structure to specify the form of valid values for a property.</span></span>

## <a name="requirements"></a><span data-ttu-id="36712-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="36712-118">Requirements</span></span>



| <span data-ttu-id="36712-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="36712-119">Requirement</span></span> | <span data-ttu-id="36712-120">Valore</span><span class="sxs-lookup"><span data-stu-id="36712-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="36712-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="36712-121">Header</span></span><br/> | <dl> <span data-ttu-id="36712-122"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="36712-122"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36712-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="36712-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36712-124">**Tipi di enumerazione**</span><span class="sxs-lookup"><span data-stu-id="36712-124">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> <dt>

[<span data-ttu-id="36712-125">**IWMDMDevice3::GetFormatCapability**</span><span class="sxs-lookup"><span data-stu-id="36712-125">**IWMDMDevice3::GetFormatCapability**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[<span data-ttu-id="36712-126">**\_funzionalità di formato WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="36712-126">**WMDM\_FORMAT\_CAPABILITY**</span></span>](wmdm-format-capability.md)
</dt> <dt>

[<span data-ttu-id="36712-127">**\_configurazione della prop WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="36712-127">**WMDM\_PROP\_CONFIG**</span></span>](wmdm-prop-config.md)
</dt> <dt>

[<span data-ttu-id="36712-128">**WMDM \_ prop \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="36712-128">**WMDM\_PROP\_DESC**</span></span>](wmdm-prop-desc.md)
</dt> <dt>

[<span data-ttu-id="36712-129">**\_ \_ enumerazione valori Prop \_ WMDM**</span><span class="sxs-lookup"><span data-stu-id="36712-129">**WMDM\_PROP\_VALUES\_ENUM**</span></span>](wmdm-prop-values-enum.md)
</dt> <dt>

[<span data-ttu-id="36712-130">**WMDM \_ \_ intervallo valori \_ prop**</span><span class="sxs-lookup"><span data-stu-id="36712-130">**WMDM\_PROP\_VALUES\_RANGE**</span></span>](wmdm-prop-values-range.md)
</dt> </dl>

 

 





