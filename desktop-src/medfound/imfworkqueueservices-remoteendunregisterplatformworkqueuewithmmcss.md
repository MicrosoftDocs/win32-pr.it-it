---
description: 'Versione utilizzabile del metodo IMFWorkQueueServices:: EndUnregisterPlatformWorkQueueWithMMCSS.'
ms.assetid: 92eef511-0af0-4146-ac81-7dfa4a649016
title: RemoteEndUnregisterPlatformWorkQueueWithMMCSS (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a03f8cdc1bfdded539c8143c3fa50c6bafb54de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884674"
---
# <a name="remoteendunregisterplatformworkqueuewithmmcss"></a>RemoteEndUnregisterPlatformWorkQueueWithMMCSS

Versione utilizzabile del metodo [**IMFWorkQueueServices:: EndUnregisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregisterplatformworkqueuewithmmcss) .

``` syntax
[call_as(EndUnregisterPlatformWorkQueueWithMMCSS)]
HRESULT RemoteEndUnregisterPlatformWorkQueueWithMMCSS(
    IUnknown *pResult
);
```

## <a name="remarks"></a>Commenti

Le applicazioni non possono chiamare direttamente questo metodo e gli oggetti non implementano questo metodo. Il metodo non viene visualizzato in vtable per l'interfaccia. Se [**EndUnregisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregisterplatformworkqueuewithmmcss) viene chiamato tra i limiti del processo, la Media Foundation DLL di proxy/stub converte la chiamata in una chiamata al metodo remoto e quindi la converte nuovamente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Mfobjects. h (include Mfidl. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Mfuuid. lib</dt> </dl>                    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMFWorkQueueServices**](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




