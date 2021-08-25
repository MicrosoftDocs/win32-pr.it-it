---
description: Imposta l'ID chiave per l'esempio.
ms.assetid: 75339350-05AA-486E-9C28-11070C0DA61D
title: MFSampleExtension_Content_KeyID attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38498665dddaed0cd38082246f61f0f86c9b1b7a1e8cec7d19d476c860fe8d6d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848171"
---
# <a name="mfsampleextension_content_keyid-attribute"></a>Attributo Content \_ KeyID MFSampleExtension \_

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
| Client minimo supportato<br/> | \[Windows 8.1 app desktop \| app UWP\]<br/>                                |
| Server minimo supportato<br/> | Windows Server 2012 App \[ UWP per app desktop \| R2\]<br/>                     |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Esempio IMF**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[MFSampleExtension \_ Encryption \_ SubSampleMappingSplit](mfsampleextension-encryption-subsamplemappingsplit.md)
</dt> </dl>

 

 




