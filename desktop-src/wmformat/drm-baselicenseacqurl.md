---
title: DRM_BaseLicenseAcqURL
description: L' \_ attributo BaseLicenseAcqURL di DRM contiene un URL di base parziale a cui un'applicazione del lettore deve passare per ottenere una licenza per il contenuto.
ms.assetid: 9acaac44-81b2-467c-9510-023fbb47dd04
keywords:
- DRM_BaseLicenseAcqURL formato Windows Media
topic_type:
- apiref
api_name:
- DRM_BaseLicenseAcqURL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 128a65eb51d9051243dd439e208207aaf98d5caf
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104117355"
---
# <a name="drm_baselicenseacqurl"></a>\_BASELICENSEACQURL DRM

L' **attributo \_ BaseLicenseAcqURL di DRM** contiene un URL di base parziale a cui un'applicazione del lettore deve passare per ottenere una licenza per il contenuto.

## <a name="global-constant"></a>Costante globale

g \_ wszWMDRM \_ BaseLicenseAcqURL

## <a name="data-type"></a>Tipo di dati

**\_stringa di tipo WMT \_**

## <a name="remarks"></a>Commenti

Si tratta di una proprietà di lettura/scrittura facoltativa impostata e recuperata tramite [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty). Viene fornito per consentire ai sistemi di distribuzione delle licenze di usare percorsi relativi nelle proprietà dell'URL di acquisizione delle licenze.

Dopo aver impostato questa proprietà, tutti gli URL di acquisizione delle licenze parziali nelle intestazioni di contenuto avranno l'URL di base aggiunto all'inizio dell'URL parziale per formare un URL completo per l'applicazione del lettore a cui passare. La chiamata di **IWMDRMReader:: GetDRMProperty** per **DRM \_ BaseLicenseAcqURL** funzionerà solo nella stessa sessione in cui è stata impostata. La proprietà non è archiviata nell'intestazione del contenuto; è dinamico e solo l'URL relativo viene archiviato nel contenuto.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà DRM**](drm-properties.md)
</dt> </dl>

 

 




