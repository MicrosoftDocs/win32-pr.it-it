---
description: Imposta l'ID chiave per l'esempio.
ms.assetid: 75339350-05AA-486E-9C28-11070C0DA61D
title: Attributo MFSampleExtension_Content_KeyID (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b40d698dbb2d64e9744027b3cd8a3bb2dceec226
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310244"
---
# <a name="mfsampleextension_content_keyid-attribute"></a>MFSampleExtension \_ Content \_ keyId-attributo

Imposta l'ID chiave per l'esempio.

## <a name="data-type"></a>Tipo di dati

**GUID**

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come impostare l'ID chiave per l'esempio.


```C++
// m_spSample is a IMFSample
// guidKID is a GUID

m_spSample->SetGUID( MFSampleExtension_Content_KeyID, guidKID );
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App \[ desktop di Windows 8.1 app \| UWP\]<br/>                                |
| Server minimo supportato<br/> | App desktop di Windows Server 2012 R2 \[ \| UWP\]<br/>                     |
| Intestazione<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[\_SubSampleMappingSplit di crittografia MFSampleExtension \_](mfsampleextension-encryption-subsamplemappingsplit.md)
</dt> </dl>

 

 




