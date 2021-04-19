---
title: Struttura WMDM_PROP_CONFIG
description: La \_ \_ struttura di configurazione di WMDM prop descrive un set di valori di proprietà compatibili tra tutte le proprietà supportate dal dispositivo per un particolare formato. Questa struttura contiene un numero di descrizioni delle proprietà in una matrice di \_ strutture WMDM Prop \_ desc.
ms.assetid: cf116861-e31d-4561-b262-e271888afc24
keywords:
- Struttura di WMDM_PROP_CONFIG Windows Media Gestione dispositivi
topic_type:
- apiref
api_name:
- WMDM_PROP_CONFIG
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b19314b2f012d25fa2d97b44b9dc7524f9e3355
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324225"
---
# <a name="wmdm_prop_config-structure"></a><span data-ttu-id="11e43-105">Struttura di configurazione di WMDM \_ prop \_</span><span class="sxs-lookup"><span data-stu-id="11e43-105">WMDM\_PROP\_CONFIG structure</span></span>

<span data-ttu-id="11e43-106">La struttura di **\_ \_ configurazione di WMDM prop** descrive un set di valori di proprietà compatibili tra tutte le proprietà supportate dal dispositivo per un particolare formato.</span><span class="sxs-lookup"><span data-stu-id="11e43-106">The **WMDM\_PROP\_CONFIG** structure describes a set of compatible property values across all the properties supported by the device for a particular format.</span></span> <span data-ttu-id="11e43-107">Questa struttura contiene un numero di descrizioni delle proprietà in una matrice di strutture [**WMDM \_ prop \_ desc**](wmdm-prop-desc.md) .</span><span class="sxs-lookup"><span data-stu-id="11e43-107">This structure contains a number of property descriptions in an array of [**WMDM\_PROP\_DESC**](wmdm-prop-desc.md) structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="11e43-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="11e43-108">Syntax</span></span>


```C++
typedef struct _WMDM_PROP_CONFIG {
  UINT           nPreference;
  UINT           nPropDesc;
  WMDM_PROP_DESC *pPropDesc;
} WMDM_PROP_CONFIG;
```



## <a name="members"></a><span data-ttu-id="11e43-109">Members</span><span class="sxs-lookup"><span data-stu-id="11e43-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="11e43-110">**nPreference**</span><span class="sxs-lookup"><span data-stu-id="11e43-110">**nPreference**</span></span>
</dt> <dd>

<span data-ttu-id="11e43-111">Livello di preferenza del dispositivo per questa configurazione.</span><span class="sxs-lookup"><span data-stu-id="11e43-111">Device's level of preference for this configuration.</span></span> <span data-ttu-id="11e43-112">Il valore più basso indica la configurazione più preferita.</span><span class="sxs-lookup"><span data-stu-id="11e43-112">The lowest value indicates the most preferred configuration.</span></span>

</dd> <dt>

<span data-ttu-id="11e43-113">**nPropDesc**</span><span class="sxs-lookup"><span data-stu-id="11e43-113">**nPropDesc**</span></span>
</dt> <dd>

<span data-ttu-id="11e43-114">Numero di descrizioni delle proprietà contenute in questa configurazione.</span><span class="sxs-lookup"><span data-stu-id="11e43-114">Number of property descriptions contained in this configuration.</span></span> <span data-ttu-id="11e43-115">È disponibile una singola descrizione della proprietà per ogni proprietà supportata per il formato specificato.</span><span class="sxs-lookup"><span data-stu-id="11e43-115">There is a single property description for each property supported for the specified format.</span></span>

</dd> <dt>

<span data-ttu-id="11e43-116">**pPropDesc**</span><span class="sxs-lookup"><span data-stu-id="11e43-116">**pPropDesc**</span></span>
</dt> <dd>

<span data-ttu-id="11e43-117">Puntatore a una matrice di strutture [**WMDM \_ prop \_ desc**](wmdm-prop-desc.md) contenenti descrizioni di proprietà.</span><span class="sxs-lookup"><span data-stu-id="11e43-117">Pointer to an array of [**WMDM\_PROP\_DESC**](wmdm-prop-desc.md) structures containing property descriptions.</span></span> <span data-ttu-id="11e43-118">La dimensione della matrice è uguale al valore di **nPropDesc**.</span><span class="sxs-lookup"><span data-stu-id="11e43-118">The size of the array is equal to the value of **nPropDesc**.</span></span> <span data-ttu-id="11e43-119">Al termine di questa operazione, l'applicazione deve liberare la memoria.</span><span class="sxs-lookup"><span data-stu-id="11e43-119">The application must free this memory when finished with it.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="11e43-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="11e43-120">Remarks</span></span>

<span data-ttu-id="11e43-121">La struttura di [**\_ \_ funzionalità del formato WMDM**](wmdm-format-capability.md) restituita da [**IWMDMDevice3:: GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) per un particolare formato è costituita da una serie di configurazioni di proprietà.</span><span class="sxs-lookup"><span data-stu-id="11e43-121">The [**WMDM\_FORMAT\_CAPABILITY**](wmdm-format-capability.md) structure returned by [**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) for a particular format consists of a number of property configurations.</span></span> <span data-ttu-id="11e43-122">**WMDM \_ Le strutture di \_ configurazione prop** descrivono tali configurazioni.</span><span class="sxs-lookup"><span data-stu-id="11e43-122">**WMDM\_PROP\_CONFIG** structures describe those configurations.</span></span>

<span data-ttu-id="11e43-123">Una configurazione di proprietà descrive i valori per tutte le proprietà supportate per un determinato formato.</span><span class="sxs-lookup"><span data-stu-id="11e43-123">A property configuration describes values for all the properties supported for a given format.</span></span> <span data-ttu-id="11e43-124">I valori di proprietà diverse in una singola configurazione sono compatibili tra loro.</span><span class="sxs-lookup"><span data-stu-id="11e43-124">The values of different properties in a single configuration are compatible with each other.</span></span> <span data-ttu-id="11e43-125">Ad esempio, per un file audio, una configurazione includerà i valori validi della frequenza di campionamento e i valori validi della velocità in bit in modo che tutte le combinazioni di queste frequenze di campionamento e di bit possano essere riprodotte nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="11e43-125">For example, for an audio file, a configuration will include valid values of sample rate and valid values of the bit rate such that all combinations of these sample and bit rates can be played on the device.</span></span>

<span data-ttu-id="11e43-126">Il chiamante è necessario per liberare la memoria utilizzata da **pPropDesc**.</span><span class="sxs-lookup"><span data-stu-id="11e43-126">The caller is required to free the memory used by **pPropDesc**.</span></span> <span data-ttu-id="11e43-127">Per un esempio di come eseguire questa operazione, vedere [**\_ \_ funzionalità di formato WMDM**](wmdm-format-capability.md).</span><span class="sxs-lookup"><span data-stu-id="11e43-127">For an example of how to do this, see [**WMDM\_FORMAT\_CAPABILITY**](wmdm-format-capability.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="11e43-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="11e43-128">Requirements</span></span>



| <span data-ttu-id="11e43-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="11e43-129">Requirement</span></span> | <span data-ttu-id="11e43-130">Valore</span><span class="sxs-lookup"><span data-stu-id="11e43-130">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="11e43-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="11e43-131">Header</span></span><br/> | <dl> <span data-ttu-id="11e43-132"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="11e43-132"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11e43-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="11e43-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11e43-134">**IWMDMDevice3::GetFormatCapability**</span><span class="sxs-lookup"><span data-stu-id="11e43-134">**IWMDMDevice3::GetFormatCapability**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[<span data-ttu-id="11e43-135">**\_ \_ \_ \_ form valori validi dell'enumerazione \_ WMDM**</span><span class="sxs-lookup"><span data-stu-id="11e43-135">**WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM**</span></span>](wmdm-enum-prop-valid-values-form.md)
</dt> <dt>

[<span data-ttu-id="11e43-136">**\_funzionalità di formato WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="11e43-136">**WMDM\_FORMAT\_CAPABILITY**</span></span>](wmdm-format-capability.md)
</dt> <dt>

[<span data-ttu-id="11e43-137">**WMDM \_ prop \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="11e43-137">**WMDM\_PROP\_DESC**</span></span>](wmdm-prop-desc.md)
</dt> <dt>

[<span data-ttu-id="11e43-138">**\_ \_ enumerazione valori Prop \_ WMDM**</span><span class="sxs-lookup"><span data-stu-id="11e43-138">**WMDM\_PROP\_VALUES\_ENUM**</span></span>](wmdm-prop-values-enum.md)
</dt> <dt>

[<span data-ttu-id="11e43-139">**WMDM \_ \_ intervallo valori \_ prop**</span><span class="sxs-lookup"><span data-stu-id="11e43-139">**WMDM\_PROP\_VALUES\_RANGE**</span></span>](wmdm-prop-values-range.md)
</dt> <dt>

[<span data-ttu-id="11e43-140">**Strutture**</span><span class="sxs-lookup"><span data-stu-id="11e43-140">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





