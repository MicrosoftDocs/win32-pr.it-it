---
title: TS_ATTRID (Textstor. h)
description: Il \_ tipo di dati ATTRID di Servizi terminal viene usato per identificare un attributo di testo.
ms.assetid: 5e375609-3d3c-4c12-ae05-dcaa70779162
keywords:
- TS_ATTRID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ea3823a95c123fe9942f69a2a133fd94a8567a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739783"
---
# <a name="ts_attrid"></a>ATTRID di Servizi terminal \_

Il tipo di dati **\_ ATTRID di Servizi terminal** viene usato per identificare un attributo di testo.


```C++
typedef GUID TS_ATTRID;
```



## <a name="remarks"></a>Commenti

Un elenco di GUID predefiniti per ATTRID di Servizi terminal \_ è in tsattrs. h.

I GUID TSATTRID \_ Text \_ VERTICALWRITING e TSATTRID \_ Text \_ Orientation sono utili per le applicazioni che devono corrispondere al testo di input da correggere. È possibile creare GUID aggiuntivi definiti dall'utente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App UWP di Windows 2000 Professional \[ desktop apps \|\]<br/>                       |
| Server minimo supportato<br/> | App desktop di Windows 2000 Server \[ \| UWP\]<br/>                             |
| Componente ridistribuibile<br/>          | TSF 1,0 su Windows 2000 Professional<br/>                                         |
| Intestazione<br/>                   | <dl> <dt>Textstor. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Textstor. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITextStoreACP:: FindNextAttrTransition**](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-findnextattrtransition)
</dt> <dt>

[**ITextStoreACP:: RequestAttrsAtPosition**](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrsatposition)
</dt> <dt>

[**ITextStoreACP:: RequestAttrsTransitioningAtPosition**](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrstransitioningatposition)
</dt> <dt>

[**ITextStoreACP:: RequestSupportedAttrs**](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestsupportedattrs)
</dt> <dt>

[**ITextStoreACPSink:: OnAttrsChange**](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onattrschange)
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

[**ATTRVAL di Servizi terminal \_**](/windows/desktop/api/Textstor/ns-textstor-ts_attrval)
</dt> </dl>

 

 





