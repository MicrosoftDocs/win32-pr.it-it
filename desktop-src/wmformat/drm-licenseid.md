---
title: DRM_LicenseID
description: La proprietà LicenseID DRM contiene una stringa recuperata dalla licenza associata al file attualmente aperto che identifica in \_ modo univoco la licenza.
ms.assetid: d5967f5b-99b6-41ea-8494-ac4a7331bbfe
keywords:
- DRM_LicenseID windows Media Format
topic_type:
- apiref
api_name:
- DRM_LicenseID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9dea32903de18dd1bde8f132b8acf993d3eba2deb0d45c814f0572ce8591ca3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930951"
---
# <a name="drm_licenseid"></a>ID licenza \_ DRM

La **proprietà \_ LicenseID DRM** contiene una stringa recuperata dalla licenza associata al file attualmente aperto che identifica in modo univoco la licenza.

## <a name="global-constant"></a>Costante globale

g \_ wszWMDRM \_ LicenseID

## <a name="data-type"></a>Tipo di dati

**STRINGA DI \_ TIPO \_ WMT**

## <a name="remarks"></a>Commenti

Questo attributo è presente solo con contenuto DRM versione 7. Può essere impostato usando [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) e può essere recuperato con [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).

L'ID licenza viene archiviato in una licenza, non in un file ASF. Ogni singola licenza ha un ID univoco assegnato dal generatore di licenze al momento della creazione della licenza. Ad esempio, se si ottengono due licenze per lo stesso contenuto, ognuna avrà un attributo LicenseID diverso. In genere, le applicazioni non devono recuperare questo valore.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




