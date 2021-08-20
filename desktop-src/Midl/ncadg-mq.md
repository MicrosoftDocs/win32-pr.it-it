---
title: ncadg_mq attributo
description: La parola chiave \_ mq ncadg identifica Microsoft Message Queuing Services (MSMQ) come protocollo di trasporto per l'endpoint. Questo protocollo è obsoleto e non deve essere usato nelle nuove applicazioni.
ms.assetid: 7472fc47-c1f0-4578-8aef-b655505e0563
keywords:
- ncadg_mq attributo MIDL
topic_type:
- apiref
api_name:
- ncadg_mq
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0164211a267760a533d8d164a76387dbbcfba8a0aad8e4ac6ecaf20ed770708a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067021"
---
# <a name="ncadg_mq-attribute"></a>Attributo ncadg \_ mq

La **parola chiave \_ mq ncadg** identifica Microsoft Message Queuing Services (MSMQ) come protocollo di trasporto per l'endpoint. Questo protocollo è obsoleto e non deve essere usato nelle nuove applicazioni.

``` syntax
endpoint("ncadg_mq:server-name")
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*nome-server* 
</dt> <dd>

Specifica il nome del server, o host, computer. Il nome è una stringa di caratteri e può essere un nome di dominio completo.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per usare il protocollo di trasporto **ncadg \_ mq,** i componenti MSMQ devono essere installati completamente e i sistemi client e server devono essere raggiungibili tramite i protocolli MQ.

Il **protocollo \_ mq ncadg** non supporta endpoint dinamici o [**chiamate broadcast.**](broadcast.md) Come per altri protocolli di datagramma, **ncadg \_ mq** non supporta i callback. Le funzioni che usano l'attributo [**di callback**](callback.md) avranno esito negativo.

> [!Note]  
> Questa famiglia di protocolli non è supportata in Windows XP.

 

## <a name="examples"></a>Esempio

La sintassi del protocollo message-queue viene definita indipendentemente dalla specifica IDL. Il compilatore MIDL esegue alcuni controlli della sintassi, ma non garantisce che la specifica dell'endpoint sia corretta. Alcuni errori possono essere segnalati in fase di esecuzione anziché durante la compilazione.

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncadg_mq:rainier") 
]
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Trasmissione**](broadcast.md)
</dt> <dt>

[**callback**](callback.md)
</dt> <dt>

[**Endpoint**](endpoint.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Messaggio**](message.md)
</dt> <dt>

[Accodamento messaggi RPC](/windows/desktop/Rpc/rpc-message-queuing)
</dt> <dt>

[Associazione di stringhe](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 