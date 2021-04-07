---
description: 'Versione utilizzabile del metodo IMFWorkQueueServices:: EndRegisterPlatformWorkQueueWithMMCSS.'
ms.assetid: cb15129e-a3ad-4351-a7d6-dd4b883437bd
title: RemoteEndRegisterPlatformWorkQueueWithMMCSS (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 673281a8ed4e4c4174ecd2d874e7032776ea44c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749199"
---
# <a name="remoteendregisterplatformworkqueuewithmmcss"></a>RemoteEndRegisterPlatformWorkQueueWithMMCSS

Versione utilizzabile del metodo [**IMFWorkQueueServices:: EndRegisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregisterplatformworkqueuewithmmcss) .

``` syntax
[call_as(EndRegisterPlatformWorkQueueWithMMCSS)]
HRESULT RemoteEndRegisterPlatformWorkQueueWithMMCSS(
    IUnknown *pResult,
    DWORD *pdwTaskId
);
```

## <a name="remarks"></a>Commenti

Le applicazioni non possono chiamare direttamente questo metodo e gli oggetti non implementano questo metodo. Il metodo non viene visualizzato in vtable per l'interfaccia. Se [**EndRegisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregisterplatformworkqueuewithmmcss) viene chiamato tra i limiti del processo, la Media Foundation DLL di proxy/stub converte la chiamata in una chiamata al metodo remoto e quindi la converte nuovamente.

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

 

 




