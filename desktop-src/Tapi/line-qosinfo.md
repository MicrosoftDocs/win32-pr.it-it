---
description: Il messaggio QOSINFO TSPI LINE causa la generazione di un evento QOS da parte di \_ TAPI. Per altre informazioni, vedere ITQOSEvent.
ms.assetid: b2844d12-c524-42ab-aeb9-8daf4e07a436
title: LINE_QOSINFO messaggio (Tspi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f0e6273eb31447f0e0c9543dfa191a25869fa08f05be8a5c639ceb101deff47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873321"
---
# <a name="line_qosinfo-message"></a>Messaggio \_ LINE QOSINFO

Il messaggio **\_ QOSINFO TSPI LINE** causa la generazione di un evento QOS da parte di TAPI. Per [**altre informazioni, vedere ITQOSEvent.**](/windows/win32/api/tapi3if/nn-tapi3if-itqosevent)


```C++
        
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*htLine* 
</dt> <dd>

Handle TAPI per la riga.

</dd> <dt>

*htCall* 
</dt> <dd>

Handle TAPI per la chiamata.

</dd> <dt>

*dwMsg* 
</dt> <dd>

Valore LINE \_ QOSINFO.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Membro dell'enumeratore [**\_ QOS EVENT**](/windows/win32/api/tapi3if/ne-tapi3if-qos_event) che identifica il tipo di evento.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Costante [del tipo di](./tapiprotocol--constants.md) supporto che identifica il supporto della chiamata associata a questo evento.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Non utilizzato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.2<br/>                                                      |
| Intestazione<br/>       | <dl> <dt>Tspi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EVENTO \_ QOS**](/windows/win32/api/tapi3if/ne-tapi3if-qos_event)
</dt> <dt>

[**ITQOSEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itqosevent)
</dt> </dl>

 

