---
title: attributo ncacn_spx
description: La \_ parola chiave SPX ncacn identifica SPX come la famiglia di protocolli per l'endpoint. Questa famiglia di protocolli è obsoleta e non deve essere utilizzata nelle nuove applicazioni.
ms.assetid: 45e93e25-e84d-4242-80b0-c4b61e80f716
keywords:
- attributo ncacn_spx MIDL
topic_type:
- apiref
api_name:
- ncacn_spx
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09d27cc746df906ff6b1a3290e41d860c76dc362
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299766"
---
# <a name="ncacn_spx-attribute"></a>ncacn \_ attributo SPX

La parola chiave **\_ SPX ncacn** identifica SPX come la famiglia di protocolli per l'endpoint. Questa famiglia di protocolli è obsoleta e non deve essere utilizzata nelle nuove applicazioni.

``` syntax
endpoint("ncacn_spx:link-address[port-name]")
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*Indirizzo collegamento* 
</dt> <dd>

Specifica il server host. Può trattarsi di una stringa di caratteri (il nome del server) o di un numero esadecimale di 20 cifre costituito dall'indirizzo di rete del server host (8 cifre) concatenato con l'indirizzo del nodo (12 cifre). Per istruzioni su come ottenere l'indirizzo di rete e l'indirizzo del nodo, vedere la sezione Osservazioni. Una stringa **null** specifica il computer locale.

</dd> <dt>

*nome porta* 
</dt> <dd>

Specifica un numero a 16 bit facoltativo che rappresenta l'indirizzo del socket. I valori possono variare da 1 a 65.535. Quando non viene specificato alcun valore, il servizio di mapping degli endpoint seleziona un valore valido per il *nome di porta* .

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando si usa il **trasporto \_ SPX ncacn** , il nome del server corrisponde esattamente al nome di Windows a 32 bit. Tuttavia, poiché i nomi vengono distribuiti usando i protocolli Novell, devono essere conformi alle convenzioni di denominazione Novell. Se il nome di un server non è un nome Novell valido, i server non saranno in grado di creare endpoint con il trasporto **\_ SPX ncacn** . Di seguito è riportato un elenco parziale di caratteri non consentiti nei nomi dei server Novell:

" \* + . / : ; < = >? \[ \] \\ \|

Il **trasporto \_ SPX ncacn** non è supportato dalla versione di NWLink fornita con MS client 3,0.

per le applicazioni client Windows a 16 bit che usano il trasporto **ncacn \_ SPX** è necessario che il file Nwipxspx.dll sia installato per l'esecuzione nel sottosistema WOW. Per ottenere questo file, contattare Novell.

> [!Note]  
> Per ottenere gli indirizzi di rete e di nodo, usare l'utilità **ComCheck** di Novell o l'API **IPXGetInternetAddress** definita da Novell. In Windows è inoltre possibile ottenere questi indirizzi con il comando di **configurazione Ipxroute** .

 

La sintassi della stringa della porta di trasporto SPX, come tutte le stringhe di porta, viene definita indipendentemente dalla specifica IDL. Il compilatore esegue alcune verifiche della sintassi, ma non garantisce che la specifica dell'endpoint sia corretta. È possibile che alcuni errori vengano segnalati in fase di esecuzione anziché in fase di compilazione.

## <a name="examples"></a>Esempi

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_spx:[1000]") 
] 
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**endpoint**](endpoint.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**ncacn \_ in \_ DSP**](ncacn-at-dsp.md)
</dt> <dt>

[**ncacn \_ DNET \_ NSP**](ncacn-dnet-nsp.md)
</dt> <dt>

[**\_TCP IP \_ ncacn**](ncacn-ip-tcp.md)
</dt> <dt>

[**ncacn \_ NB \_ IPX**](ncacn-nb-ipx.md)
</dt> <dt>

[**ncacn \_ NB \_ NB**](ncacn-nb-nb.md)
</dt> <dt>

[**ncacn \_ NB \_ TCP**](ncacn-nb-tcp.md)
</dt> <dt>

[**\_NP ncacn**](ncacn-np.md)
</dt> <dt>

[**ncacn \_ le reti virtuali \_ spp**](ncacn-vns-spp.md)
</dt> <dt>

[**ncalrpc**](ncalrpc.md)
</dt> <dt>

[**ncadg \_ IPX**](ncadg-ipx.md)
</dt> <dt>

[**\_UDP IP \_ ncadg**](ncadg-ip-udp.md)
</dt> <dt>

[Associazione stringa](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 