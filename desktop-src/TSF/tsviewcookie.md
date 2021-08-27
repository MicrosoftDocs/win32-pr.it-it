---
title: TsViewCookie (Textstor.h)
description: Il tipo di dati TsViewCookie identifica una visualizzazione di contesto.
ms.assetid: e649b799-d0d6-4f2d-b9f1-28070eea9b16
keywords:
- TsViewCookie
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1266f1835015583a31c2dce1d3b2da6131611ef90ba7a0dd76cae58bc3fce2f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118873566"
---
# <a name="tsviewcookie"></a>TsViewCookie

Il **tipo di dati TsViewCookie** identifica una visualizzazione di contesto.


```C++
typedef DWORD TsViewCookie;
```



## <a name="remarks"></a>Commenti

Un'applicazione deve fornire un **valore TsViewCookie** univoco per ogni visualizzazione creata.

Il gestore TSF ottiene questo valore dall'applicazione chiamando [ITextStoreACP::GetActiveView](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getactiveview) o [ITextStoreAnchor::GetActiveView](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getactiveview). Il gestore TSF usa questo valore per identificare la visualizzazione quando chiama vari metodi [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) o [ITextStoreAnchor.](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor)

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

[**ITextStoreACP**](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp)
</dt> <dt>

[**ITextStoreACP::GetActiveView**](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getactiveview)
</dt> <dt>

[**ITextStoreAnchor::GetActiveView**](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getactiveview)
</dt> </dl>

 

 





