---
title: TS_ATTRID (Textstor.h)
description: Il tipo di dati \_ TS ATTRID viene usato per identificare un attributo di testo.
ms.assetid: 5e375609-3d3c-4c12-ae05-dcaa70779162
keywords:
- TS_ATTRID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e1c40d56f1f8ff3deb59d0dd7664a197a672ade7b2d53beebd8e35ba5de7c0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117950337"
---
# <a name="ts_attrid"></a>TS \_ ATTRID

Il **tipo di dati \_ TS ATTRID** viene usato per identificare un attributo di testo.


```C++
typedef GUID TS_ATTRID;
```



## <a name="remarks"></a>Commenti

Un elenco di GUID predefiniti per TS \_ ATTRID si trova in tsattrs.h.

I GUID TSATTRID Text VerticalWriting e \_ TSATTRID Text Orientation sono utili per le applicazioni in modo che corrispondano al testo di \_ \_ input da \_ correggere. È possibile creare ALTRI GUID definiti dall'utente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[ app desktop app \| UWP\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 App desktop UWP per le app \[ desktop di 2000 \| Server\]<br/>                             |
| Componente ridistribuibile<br/>          | TSF 1.0 in Windows 2000 Professional<br/>                                         |
| Intestazione<br/>                   | <dl> <dt>Textstor.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Textstor.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITextStoreACP::FindNextAttrTransition**](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-findnextattrtransition)
</dt> <dt>

[**ITextStoreACP::RequestAttrsAtPosition**](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrsatposition)
</dt> <dt>

[**ITextStoreACP::RequestAttrsTransitioningAtPosition**](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrstransitioningatposition)
</dt> <dt>

[**ITextStoreACP::RequestSupportedAttrs**](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestsupportedattrs)
</dt> <dt>

[**ITextStoreACPSink::OnAttrsChange**](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onattrschange)
</dt> <dt>

[**ITextStoreAnchor::FindNextAttrTransition**](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition)
</dt> <dt>

[**ITextStoreAnchor::RequestAttrsAtPosition**](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrsatposition)
</dt> <dt>

[**ITextStoreAnchor::RequestAttrsTransitioningAtPosition**](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrstransitioningatposition)
</dt> <dt>

[**ITextStoreAnchor::RequestSupportedAttrs**](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestsupportedattrs)
</dt> <dt>

[**ITextStoreAnchorSink::OnAttrsChange**](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onattrschange)
</dt> <dt>

[**TS \_ ATTRVAL**](/windows/desktop/api/Textstor/ns-textstor-ts_attrval)
</dt> </dl>

 

 





