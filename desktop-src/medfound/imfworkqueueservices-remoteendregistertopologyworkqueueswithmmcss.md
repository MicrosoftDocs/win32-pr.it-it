---
description: Versione remota del metodo IMFWorkQueueServices::EndRegisterTopologyWorkQueuesWithMMCSS.
ms.assetid: 94dce412-6a72-4ddf-86a3-5176ee1eb6d2
title: RemoteEndRegisterTopologyWorkQueuesWithMMCSS (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a82861da29a5cae3cc9275e7a45372363280df7a7d2026bc4dfa4e2e1147a76c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114301"
---
# <a name="remoteendregistertopologyworkqueueswithmmcss"></a>RemoteEndRegisterTopologyWorkQueuesWithMMCSS

Versione remota del metodo [**IMFWorkQueueServices::EndRegisterTopologyWorkQueuesWithMMCSS.**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregistertopologyworkqueueswithmmcss)

``` syntax
[call_as(EndRegisterTopologyWorkQueuesWithMMCSS)]
HRESULT RemoteEndRegisterTopologyWorkQueuesWithMMCSS(
    IUnknown *pResult
);
```

## <a name="remarks"></a>Commenti

Le applicazioni non possono chiamare direttamente questo metodo e gli oggetti non implementano questo metodo. Il metodo non viene visualizzato nella tabella vtable per l'interfaccia . Se [**EndRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregistertopologyworkqueueswithmmcss) viene chiamato oltre i limiti del processo, la DLL proxy/stub di Media Foundation converte la chiamata in una chiamata al metodo remoto e quindi la converte nuovamente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Mfobjects.h (includere Mfidl.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Mfuuid.lib</dt> </dl>                    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMFWorkQueueServices**](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




