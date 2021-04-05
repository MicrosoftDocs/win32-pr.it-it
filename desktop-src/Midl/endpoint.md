---
title: attributo endpoint
description: L'attributo \ endpoint \ specifica una porta o porte note (endpoint di comunicazione) sui quali i server dell'interfaccia restano in ascolto delle chiamate.
ms.assetid: b88c5a97-b726-43de-b5b6-649cda60c320
keywords:
- attributo dell'endpoint MIDL
topic_type:
- apiref
api_name:
- endpoint
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4383df496a791859f7249766f0dbb59266d28e93
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872362"
---
# <a name="endpoint-attribute"></a>attributo endpoint

L'attributo **\[ endpoint \]** specifica una porta o porte note (endpoint di comunicazione) sui quali i server dell'interfaccia restano in ascolto delle chiamate.

``` syntax
endpoint("protocol-sequence:[endpoint-port]" [ , ...] )
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*sequenza di protocolli* 
</dt> <dd>

Specifica una stringa di caratteri che rappresenta una combinazione valida di un protocollo RPC (ad esempio "ncacn"), un protocollo di trasporto (ad esempio "TCP") e un protocollo di rete (ad esempio "IP"). Per un elenco di sequenze di protocollo valide, vedere [costanti di sequenza del protocollo](/windows/desktop/Rpc/protocol-sequence-constants).

</dd> <dt>

*Porta endpoint* 
</dt> <dd>

Specifica una stringa che rappresenta la designazione dell'endpoint per la famiglia di protocolli specificata. La sintassi della stringa di porta è specifica per ogni sequenza di protocollo.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'attributo **\[ endpoint \]** specifica una famiglia di trasporto, ad esempio il protocollo orientato alla connessione TCP/IP, un protocollo NetBIOS orientato alla connessione o il protocollo orientato alla connessione named pipe. L'utilizzo dell'attributo **\[ endpoint \]** è coerente con altri metodi per l'aggiunta di un endpoint e non fornisce servizi aggiuntivi o speciali per l'endpoint. fornisce semplicemente un collegamento per chiamare l'API.

> [!Note]  
> Specifica di un endpoint in. La definizione dell'interfaccia IDL non limita l'accesso all'interfaccia all'endpoint specificato. Aggiunta di un endpoint a. La definizione dell'interfaccia IDL consente la chiamata dell'interfaccia tramite qualsiasi endpoint in tale processo e consente l'utilizzo dell'endpoint per chiamare altre interfacce nel processo.

 

Il valore della *sequenza di protocollo* determina i valori validi per la *porta dell'endpoint*. Il compilatore MIDL controlla solo la sintassi generale per la voce di *Porta endpoint* . Gli errori di specifica della porta vengono segnalati dalle librerie di Runtime. Per informazioni sui valori consentiti per ogni sequenza di protocollo, vedere [costanti di sequenza del protocollo](/windows/desktop/Rpc/protocol-sequence-constants).

Le sequenze di protocollo seguenti specificate da DCE non sono supportate dal compilatore MIDL fornito con Microsoft RPC: **ncacn \_ OSI \_ DNA** e **ncadg \_ DDS**.

Assicurarsi di racchiudere tra virgolette la barra rovesciata negli endpoint. Questo errore si verifica in genere quando l'endpoint è un named pipe.

Le informazioni sull'endpoint specificate nel file IDL vengono utilizzate dalle funzioni di runtime RPC [**RpcServerUseProtseqIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqif) e [**RpcServerUseAllProtseqsIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqsif).

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

 

 