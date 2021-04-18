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
# <a name="wmdm_format_capability-structure"></a>Struttura delle funzionalità del \_ formato WMDM \_

La struttura della **\_ \_ funzionalità del formato WMDM** descrive le funzionalità di un dispositivo per un particolare formato. Questa struttura contiene un set di configurazioni di proprietà in una matrice di strutture **WMDM \_ prop \_ config** . Ogni configurazione di proprietà rappresenta un set di valori di proprietà compatibili tra tutte le proprietà supportate per un determinato formato. L'applicazione può ottenere questa struttura chiamando il metodo **IWMDMDevice3:: GetFormatCapability** e passando il codice del formato. Per un elenco di codici di formato, vedere [**WMDM \_ FORMATCODE**](wmdm-formatcode.md).

## <a name="syntax"></a>Sintassi


```C++
typedef struct _WMDM_FORMAT_CAPABILITY {
  UINT              nPropConfig;
  WMDM_PROP_CONFIG  *pConfigs;
} WMDM_FORMAT_CAPABILITY;
```



## <a name="members"></a>Members

<dl> <dt>

**nPropConfig**
</dt> <dd>

Numero di configurazioni di proprietà nella matrice **pConfigs** .

</dd> <dt>

**pConfigs**
</dt> <dd>

Puntatore a una matrice di strutture [**WMDM \_ prop \_ config**](wmdm-prop-config.md) . La dimensione della matrice è uguale al valore di **nPropConfig**.

</dd> </dl>

## <a name="remarks"></a>Commenti

La struttura della **\_ \_ funzionalità del formato WMDM** fornisce un meccanismo flessibile per esprimere le funzionalità del dispositivo per un particolare formato.

Se il contenuto deve essere sottoposto a rendering dal dispositivo (ad esempio, un file audio da riprodurre dal dispositivo), le proprietà del contenuto devono corrispondere a una delle configurazioni di proprietà restituite da [**IWMDMDevice3:: GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) nella struttura della **\_ \_ funzionalità di formato WMDM** . Ad esempio, per un file audio, la velocità in bit e la frequenza di campionamento devono soddisfare una delle configurazioni di proprietà restituite.

Il chiamante è responsabile della liberazione della memoria allocata per questa struttura. La funzione seguente illustra come cancellare una struttura **di \_ \_ funzionalità del formato WMDM** .


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



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[**\_ \_ \_ \_ form valori validi dell'enumerazione \_ WMDM**](wmdm-enum-prop-valid-values-form.md)
</dt> <dt>

[**\_configurazione della prop WMDM \_**](wmdm-prop-config.md)
</dt> <dt>

[**WMDM \_ prop \_ DESC**](wmdm-prop-desc.md)
</dt> <dt>

[**\_ \_ enumerazione valori Prop \_ WMDM**](wmdm-prop-values-enum.md)
</dt> <dt>

[**WMDM \_ \_ intervallo valori \_ prop**](wmdm-prop-values-range.md)
</dt> <dt>

[**Strutture**](structures.md)
</dt> </dl>

 

 





