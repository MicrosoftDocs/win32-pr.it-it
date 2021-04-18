---
description: 'Versione utilizzabile del metodo IMFMediaTypeHandler:: GetCurrentMediaType.'
ms.assetid: f7f69adb-2a4a-47a9-bb92-ad9d005b962f
title: RemoteGetCurrentMediaType (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc168198e8402d83538c046967d1d851ae2532b1
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320482"
---
# <a name="remotegetcurrentmediatype"></a>RemoteGetCurrentMediaType

Versione utilizzabile del metodo [**IMFMediaTypeHandler:: GetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype) .

``` syntax
[call_as(GetCurrentMediaType)]
HRESULT RemoteGetCurrentMediaType(
    BYTE **ppbData,
    DWORD *pcbData
);
```

## <a name="remarks"></a>Commenti

Le applicazioni non possono chiamare direttamente questo metodo e gli oggetti non implementano questo metodo. Il metodo non viene visualizzato in vtable per l'interfaccia. Se [**GetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype) viene chiamato tra i limiti del processo, la Media Foundation DLL di proxy/stub converte la chiamata in una chiamata al metodo remoto e quindi la converte nuovamente.

Questa interfaccia è disponibile nelle piattaforme seguenti se sono installati i componenti ridistribuibili di Windows Media Format 11 SDK:

-   Windows XP con Service Pack 2 (SP2) e versioni successive.
-   Windows XP Media Center Edition 2005 con KB900325 (Windows XP Media Center Edition 2005) e KB925766 (aggiornamento cumulativo ottobre 2006 per Windows XP Media Center Edition) installato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows Vista app \[ \| UWP\]<br/>                                                    |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2008 \|\]<br/>                                              |
| Intestazione<br/>                   | <dl> <dt>Mfobjects. h (include Mfidl. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Mfuuid. lib</dt> </dl>                    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler)
</dt> </dl>

 

 




