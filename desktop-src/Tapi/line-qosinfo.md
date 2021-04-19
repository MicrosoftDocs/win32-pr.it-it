---
description: Il messaggio QOSINFO della riga TSPI \_ fa sì che TAPI generi un evento QoS. Per ulteriori informazioni, vedere ITQOSEvent.
ms.assetid: b2844d12-c524-42ab-aeb9-8daf4e07a436
title: Messaggio LINE_QOSINFO (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d35ff19601ab6acd9a3d8e8aebf1e59b06a4f17e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328910"
---
# <a name="line_qosinfo-message"></a>\_Messaggio linea QOSINFO

Il messaggio **\_ QOSINFO della riga** TSPI fa sì che TAPI generi un evento QoS. Per ulteriori informazioni, vedere [**ITQOSEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itqosevent) .


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

RIGA del valore \_ QOSINFO.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Membro dell'enumeratore [**di \_ eventi QoS**](/windows/win32/api/tapi3if/ne-tapi3if-qos_event) che identifica il tipo di evento.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Costante del [tipo di supporto](./tapiprotocol--constants.md) che identifica il supporto della chiamata associata a questo evento.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Non utilizzato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,2<br/>                                                      |
| Intestazione<br/>       | <dl> <dt>TSPI. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_evento QoS**](/windows/win32/api/tapi3if/ne-tapi3if-qos_event)
</dt> <dt>

[**ITQOSEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itqosevent)
</dt> </dl>

 

