---
title: DRM_LicenseID
description: La \_ Proprietà DRM LicenseID contiene una stringa recuperata dalla licenza associata al file attualmente aperto che identifica in modo univoco la licenza.
ms.assetid: d5967f5b-99b6-41ea-8494-ac4a7331bbfe
keywords:
- DRM_LicenseID formato Windows Media
topic_type:
- apiref
api_name:
- DRM_LicenseID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8d9174e364e186056e63375b8ed322875dfb868
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104336425"
---
# <a name="drm_licenseid"></a>\_LICENSEID DRM

La proprietà **DRM \_ LicenseID** contiene una stringa recuperata dalla licenza associata al file attualmente aperto che identifica in modo univoco la licenza.

## <a name="global-constant"></a>Costante globale

g \_ wszWMDRM \_ LicenseID

## <a name="data-type"></a>Tipo di dati

**\_stringa di tipo WMT \_**

## <a name="remarks"></a>Commenti

Questo attributo è presente solo con contenuto DRM versione 7. Può essere impostato usando [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) e può essere recuperato con [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).

L'ID licenza viene archiviato in una licenza, non in un file ASF. Ogni singola licenza dispone di un ID univoco assegnato dal generatore di licenze al momento della creazione della licenza. Se ad esempio si ottengono due licenze per lo stesso contenuto, ciascuna di esse avrà un attributo LicenseID diverso. In genere, le applicazioni non devono recuperare questo valore.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




