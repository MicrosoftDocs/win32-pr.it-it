---
title: Struttura WMDM_FORMAT_CAPABILITY
description: La \_ struttura della \_ funzionalità del formato WMDM descrive le funzionalità di un dispositivo per un particolare formato.
ms.assetid: 9672173D-B11E-4DCB-BCAE-38B94FCC8B99
keywords:
- Struttura di WMDM_FORMAT_CAPABILITY Windows Media Gestione dispositivi
topic_type:
- apiref
api_name:
- WMDM_FORMAT_CAPABILITY
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14f8dbdd81aff63a819624cdb1c778cb9bec712b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325010"
---
# <a name="wmdm_format_capability-structure"></a><span data-ttu-id="cee8e-104">Struttura delle funzionalità del \_ formato WMDM \_</span><span class="sxs-lookup"><span data-stu-id="cee8e-104">WMDM\_FORMAT\_CAPABILITY structure</span></span>

<span data-ttu-id="cee8e-105">La struttura della **\_ \_ funzionalità del formato WMDM** descrive le funzionalità di un dispositivo per un particolare formato.</span><span class="sxs-lookup"><span data-stu-id="cee8e-105">The **WMDM\_FORMAT\_CAPABILITY** structure describes the capabilities of a device for a particular format.</span></span> <span data-ttu-id="cee8e-106">Questa struttura contiene un set di configurazioni di proprietà in una matrice di strutture **WMDM \_ prop \_ config** .</span><span class="sxs-lookup"><span data-stu-id="cee8e-106">This structure contains a set of property configurations in an array of **WMDM\_PROP\_CONFIG** structures.</span></span> <span data-ttu-id="cee8e-107">Ogni configurazione di proprietà rappresenta un set di valori di proprietà compatibili tra tutte le proprietà supportate per un determinato formato.</span><span class="sxs-lookup"><span data-stu-id="cee8e-107">Each property configuration represents a set of compatible property values across all the properties supported for a given format.</span></span> <span data-ttu-id="cee8e-108">L'applicazione può ottenere questa struttura chiamando il metodo **IWMDMDevice3:: GetFormatCapability** e passando il codice del formato.</span><span class="sxs-lookup"><span data-stu-id="cee8e-108">The application can get this structure by calling the **IWMDMDevice3::GetFormatCapability** method and passing in the format code.</span></span> <span data-ttu-id="cee8e-109">Per un elenco di codici di formato, vedere [**WMDM \_ FORMATCODE**](wmdm-formatcode.md).</span><span class="sxs-lookup"><span data-stu-id="cee8e-109">For a list of format codes, see [**WMDM\_FORMATCODE**](wmdm-formatcode.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="cee8e-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cee8e-110">Syntax</span></span>


```C++
typedef struct _WMDM_FORMAT_CAPABILITY {
  UINT              nPropConfig;
  WMDM_PROP_CONFIG  *pConfigs;
} WMDM_FORMAT_CAPABILITY;
```



## <a name="members"></a><span data-ttu-id="cee8e-111">Members</span><span class="sxs-lookup"><span data-stu-id="cee8e-111">Members</span></span>

<dl> <dt>

<span data-ttu-id="cee8e-112">**nPropConfig**</span><span class="sxs-lookup"><span data-stu-id="cee8e-112">**nPropConfig**</span></span>
</dt> <dd>

<span data-ttu-id="cee8e-113">Numero di configurazioni di proprietà nella matrice **pConfigs** .</span><span class="sxs-lookup"><span data-stu-id="cee8e-113">Number of property configurations in the **pConfigs** array.</span></span>

</dd> <dt>

<span data-ttu-id="cee8e-114">**pConfigs**</span><span class="sxs-lookup"><span data-stu-id="cee8e-114">**pConfigs**</span></span>
</dt> <dd>

<span data-ttu-id="cee8e-115">Puntatore a una matrice di strutture [**WMDM \_ prop \_ config**](wmdm-prop-config.md) .</span><span class="sxs-lookup"><span data-stu-id="cee8e-115">Pointer to an array of [**WMDM\_PROP\_CONFIG**](wmdm-prop-config.md) structures.</span></span> <span data-ttu-id="cee8e-116">La dimensione della matrice è uguale al valore di **nPropConfig**.</span><span class="sxs-lookup"><span data-stu-id="cee8e-116">The size of array is equal to the value of **nPropConfig**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cee8e-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="cee8e-117">Remarks</span></span>

<span data-ttu-id="cee8e-118">La struttura della **\_ \_ funzionalità del formato WMDM** fornisce un meccanismo flessibile per esprimere le funzionalità del dispositivo per un particolare formato.</span><span class="sxs-lookup"><span data-stu-id="cee8e-118">The **WMDM\_FORMAT\_CAPABILITY** structure provides a flexible mechanism to express the capabilities of the device for a particular format.</span></span>

<span data-ttu-id="cee8e-119">Se il contenuto deve essere sottoposto a rendering dal dispositivo (ad esempio, un file audio da riprodurre dal dispositivo), le proprietà del contenuto devono corrispondere a una delle configurazioni di proprietà restituite da [**IWMDMDevice3:: GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) nella struttura della **\_ \_ funzionalità di formato WMDM** .</span><span class="sxs-lookup"><span data-stu-id="cee8e-119">If the content is meant to be rendered by the device (for example, an audio file to be played by the device), the properties of the content must match one of the property configurations returned by [**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) in the **WMDM\_FORMAT\_CAPABILITY** structure.</span></span> <span data-ttu-id="cee8e-120">Ad esempio, per un file audio, la velocità in bit e la frequenza di campionamento devono soddisfare una delle configurazioni di proprietà restituite.</span><span class="sxs-lookup"><span data-stu-id="cee8e-120">For example, for an audio file, the bit rate and sample rate must satisfy one of the property configurations returned.</span></span>

<span data-ttu-id="cee8e-121">Il chiamante è responsabile della liberazione della memoria allocata per questa struttura.</span><span class="sxs-lookup"><span data-stu-id="cee8e-121">The caller is responsible for freeing the memory allocated for this structure.</span></span> <span data-ttu-id="cee8e-122">La funzione seguente illustra come cancellare una struttura **di \_ \_ funzionalità del formato WMDM** .</span><span class="sxs-lookup"><span data-stu-id="cee8e-122">The following function demonstrates how to clear a **WMDM\_FORMAT\_CAPABILITY** structure.</span></span>


```C++
void FreeFormatCapability(WMDM_FORMAT_CAPABILITY formatCap)
{
    // Loop through all configurations.
    for (UINT i=0; i < formatCap.nPropConfig; i++) 
    {
        // Loop through all descriptions of a configuration and delete
        // the values particular to that description type.
        for (UINT j=0; j < formatCap.pConfigs[i].nPropDesc; j++) 
        {
            switch (formatCap.pConfigs[i].pPropDesc[j].ValidValuesForm)
            {
                case WMDM_ENUM_PROP_VALID_VALUES_ENUM:
                    for (UINT k=0; k < formatCap.pConfigs[i].pPropDesc[j].ValidValues.EnumeratedValidValues.cEnumValues; k++)
                    {
                        PropVariantClear (&(formatCap.pConfigs[i].pPropDesc[j].ValidValues.EnumeratedValidValues.pValues[k]));
                    }
                    CoTaskMemFree(formatCap.pConfigs[i].pPropDesc[j].ValidValues.EnumeratedValidValues.pValues);
                    break;
                case WMDM_ENUM_PROP_VALID_VALUES_RANGE:
                    PropVariantClear (&(formatCap.pConfigs[i].pPropDesc[j].ValidValues.ValidValuesRange.rangeMin));
                    PropVariantClear (&(formatCap.pConfigs[i].pPropDesc[j].ValidValues.ValidValuesRange.rangeMax));
                    PropVariantClear (&(formatCap.pConfigs[i].pPropDesc[j].ValidValues.ValidValuesRange.rangeStep));
                    break;
                case WMDM_ENUM_PROP_VALID_VALUES_ANY:
                    // No dynamically allocated memory for this value.
                default:
                    break;
            }

            // Free the memory for the description name.
            CoTaskMemFree(formatCap.pConfigs[i].pPropDesc[j].pwszPropName);
        }
        // Free the memory holding the array of description items for this configuration.
        CoTaskMemFree(formatCap.pConfigs[i].pPropDesc);
    }

    // Free the memory pointing to the array of configurations.
    CoTaskMemFree(formatCap.pConfigs);
    formatCap.nPropConfig = 0;
}
```



## <a name="requirements"></a><span data-ttu-id="cee8e-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cee8e-123">Requirements</span></span>



| <span data-ttu-id="cee8e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="cee8e-124">Requirement</span></span> | <span data-ttu-id="cee8e-125">Valore</span><span class="sxs-lookup"><span data-stu-id="cee8e-125">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="cee8e-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cee8e-126">Header</span></span><br/> | <dl> <span data-ttu-id="cee8e-127"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cee8e-127"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cee8e-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cee8e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cee8e-129">**IWMDMDevice3::GetFormatCapability**</span><span class="sxs-lookup"><span data-stu-id="cee8e-129">**IWMDMDevice3::GetFormatCapability**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[<span data-ttu-id="cee8e-130">**\_ \_ \_ \_ form valori validi dell'enumerazione \_ WMDM**</span><span class="sxs-lookup"><span data-stu-id="cee8e-130">**WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM**</span></span>](wmdm-enum-prop-valid-values-form.md)
</dt> <dt>

[<span data-ttu-id="cee8e-131">**\_configurazione della prop WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="cee8e-131">**WMDM\_PROP\_CONFIG**</span></span>](wmdm-prop-config.md)
</dt> <dt>

[<span data-ttu-id="cee8e-132">**WMDM \_ prop \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="cee8e-132">**WMDM\_PROP\_DESC**</span></span>](wmdm-prop-desc.md)
</dt> <dt>

[<span data-ttu-id="cee8e-133">**\_ \_ enumerazione valori Prop \_ WMDM**</span><span class="sxs-lookup"><span data-stu-id="cee8e-133">**WMDM\_PROP\_VALUES\_ENUM**</span></span>](wmdm-prop-values-enum.md)
</dt> <dt>

[<span data-ttu-id="cee8e-134">**WMDM \_ \_ intervallo valori \_ prop**</span><span class="sxs-lookup"><span data-stu-id="cee8e-134">**WMDM\_PROP\_VALUES\_RANGE**</span></span>](wmdm-prop-values-range.md)
</dt> <dt>

[<span data-ttu-id="cee8e-135">**Strutture**</span><span class="sxs-lookup"><span data-stu-id="cee8e-135">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





