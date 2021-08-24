---
title: Attributo endpoint
description: L'attributo \endpoint\ specifica una porta o porte note (endpoint di comunicazione) su cui i server dell'interfaccia sono in ascolto delle chiamate.
ms.assetid: b88c5a97-b726-43de-b5b6-649cda60c320
keywords:
- Attributo endpoint MIDL
topic_type:
- apiref
api_name:
- endpoint
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dea4951a407f09c1407c6e897938460d780e0429e888210e7e1ade392b5e94af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119383181"
---
# <a name="endpoint-attribute"></a>Attributo endpoint

**\[ L'attributo \]** endpoint specifica una o più porte note (endpoint di comunicazione) su cui i server dell'interfaccia sono in ascolto delle chiamate.

``` syntax
endpoint("protocol-sequence:[endpoint-port]" [ , ...] )
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*protocol-sequence* 
</dt> <dd>

Specifica una stringa di caratteri che rappresenta una combinazione valida di un protocollo RPC (ad esempio "ncacn"), un protocollo di trasporto (ad esempio "tcp") e un protocollo di rete (ad esempio "ip"). Per un elenco di sequenze di protocollo valide, vedere [Costanti della sequenza di protocollo.](/windows/desktop/Rpc/protocol-sequence-constants)

</dd> <dt>

*endpoint-port* 
</dt> <dd>

Specifica una stringa che rappresenta la designazione dell'endpoint per la famiglia di protocolli specificata. La sintassi della stringa di porta è specifica di ogni sequenza di protocollo.

</dd> </dl>

## <a name="remarks"></a>Commenti

**\[ L'attributo \]** endpoint specifica una famiglia di trasporti, ad esempio il protocollo orientato alla connessione TCP/IP, un protocollo orientato alla connessione NetBIOS o il protocollo orientato alla connessione named pipe. L'uso dell'attributo **\[ endpoint \]** è coerente con altri metodi per l'aggiunta di un endpoint e non fornisce servizi aggiuntivi o speciali per l'endpoint, ma fornisce semplicemente un collegamento per chiamare l'API.

> [!Note]  
> Specifica di un endpoint in . La definizione dell'interfaccia IDL non limita l'accesso all'interfaccia all'endpoint specificato. Aggiunta di un endpoint a . La definizione dell'interfaccia IDL consente di chiamare l'interfaccia tramite qualsiasi endpoint del processo e consente di usare l'endpoint per chiamare altre interfacce in tale processo.

 

Il *valore della sequenza di* protocollo determina i valori validi per *endpoint-port.* Il compilatore MIDL controlla solo la sintassi generale per la *voce endpoint-port.* Gli errori di specifica della porta vengono segnalati dalle librerie di runtime. Per informazioni sui valori consentiti per ogni sequenza di protocollo, vedere Costanti della [sequenza di protocollo.](/windows/desktop/Rpc/protocol-sequence-constants)

Le sequenze di protocollo seguenti specificate da DCE non sono supportate dal compilatore MIDL fornito con Microsoft RPC: **ncacn \_ osi \_ dna** e **ncadg \_ dds**.

Assicurarsi di virgolette corrette per i caratteri barra rovesciata negli endpoint. Questo errore si verifica in genere quando l'endpoint è un named pipe.

Le informazioni sull'endpoint specificate nel file IDL vengono usate dalle funzioni di run-time RPC [**RpcServerUseProtseqIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqif) e [**RpcServerUseAllProtseqsIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqsif).

## <a name="examples"></a>Esempi

``` syntax
endpoint("ncacn_np:[\\pipe\\rainier]") 

endpoint("ncacn_ip_tcp:[1044]", "ncacn_np:[\\pipe\\shasta]")
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**RpcServerUseAllProtseqsIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqsif)
</dt> <dt>

[**RpcServerUseProtseqIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqif)
</dt> </dl>

 

 