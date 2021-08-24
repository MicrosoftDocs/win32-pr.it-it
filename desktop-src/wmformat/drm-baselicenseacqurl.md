---
title: DRM_BaseLicenseAcqURL
description: L'attributo BaseLicenseAcqURL DRM contiene un URL di base parziale a cui un'applicazione lettore deve passare per ottenere una \_ licenza per il contenuto.
ms.assetid: 9acaac44-81b2-467c-9510-023fbb47dd04
keywords:
- DRM_BaseLicenseAcqURL windows Media Format
topic_type:
- apiref
api_name:
- DRM_BaseLicenseAcqURL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77827068ee8a491cd732b28e5b8d60e1868ec66c04c72156f08358dd7d3751d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119659001"
---
# <a name="drm_baselicenseacqurl"></a>DRM \_ BaseLicenseAcqURL

**L'attributo \_ BaseLicenseAcqURL DRM** contiene un URL di base parziale a cui un'applicazione lettore deve passare per ottenere una licenza per il contenuto.

## <a name="global-constant"></a>Costante globale

g \_ wszWMDRM \_ BaseLicenseAcqURL

## <a name="data-type"></a>Tipo di dati

**STRINGA DI \_ TIPO \_ WMT**

## <a name="remarks"></a>Commenti

Si tratta di una proprietà di lettura/scrittura facoltativa che viene impostata e recuperata tramite [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty). Viene fornito per consentire ai sistemi di distribuzione delle licenze di usare percorsi relativi nelle proprietà dell'URL di acquisizione delle licenze.

Dopo aver impostato questa proprietà, a tutti gli URL di acquisizione delle licenze parziali nelle intestazioni del contenuto verrà aggiunto l'URL di base all'inizio dell'URL parziale per formare un URL completo a cui l'applicazione lettore può passare. La **chiamata a IWMDRMReader::GetDRMProperty** per **\_ DRM BaseLicenseAcqURL** funzionerà solo nella stessa sessione impostata. La proprietà non viene archiviata nell'intestazione del contenuto. è dinamico e solo l'URL relativo viene archiviato nel contenuto.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà DRM**](drm-properties.md)
</dt> </dl>

 

 




