---
title: attributo ncadg_ipx
description: La \_ parola chiave ncadg IPX identifica IPX come famiglia di protocolli per l'endpoint. Questa famiglia di protocolli è obsoleta e non deve essere utilizzata nelle nuove applicazioni.
ms.assetid: 6b136eb9-4e18-43ff-993b-a2ad005273f1
keywords:
- attributo ncadg_ipx MIDL
topic_type:
- apiref
api_name:
- ncadg_ipx
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fa206902ae80e5218e1d5249da8a8fb1b9dfc04
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725378"
---
# <a name="ncadg_ipx-attribute"></a>\_attributo IPX ncadg

La parola chiave **ncadg \_ IPX** identifica IPX come famiglia di protocolli per l'endpoint. Questa famiglia di protocolli è obsoleta e non deve essere utilizzata nelle nuove applicazioni.

``` syntax
endpoint("ncadg_ipx:link-address[port-name]")
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*Indirizzo collegamento* 
</dt> <dd>

Specifica il server host. Può trattarsi di una stringa di caratteri (il nome del server) o di un numero esadecimale di 20 cifre costituito dall'indirizzo di rete del server host (8 cifre) concatenato con l'indirizzo del nodo (12 cifre). Per istruzioni su come ottenere l'indirizzo di rete e l'indirizzo del nodo, vedere la sezione Osservazioni. Una stringa **null** specifica il computer locale.

</dd> <dt>

*nome porta* 
</dt> <dd>

Specifica un numero a 16 bit facoltativo che rappresenta l'indirizzo del socket. I valori possono variare da 1 a 65535. Quando non viene specificato alcun valore, il servizio di mapping degli endpoint seleziona un valore valido per il *nome di porta* .

</dd> </dl>

## <a name="remarks"></a>Commenti

Si applicano le restrizioni seguenti ai protocolli di datagramma, **ncadg \_ IPX** e [**ncadg \_ IP \_ UDP**](ncadg-ip-udp.md):

-   Non supportano i callback. Tutte le funzioni che utilizzano l'attributo di **\[** [**callback**](callback.md) **\]** avranno esito negativo.
-   Non supportano l'uso del costruttore del tipo di [**pipe**](pipe.md) .

Quando si utilizza il trasporto **\_ IPX ncadg** , il nome del server è esattamente uguale al nome del server Windows a 32 bit. Tuttavia, poiché i nomi vengono distribuiti usando i protocolli Novell, devono essere conformi alle convenzioni di denominazione Novell. Se il nome di un server non è un nome Novell valido, i server non saranno in grado di creare endpoint con il trasporto **\_ IPX ncadg** . Di seguito è riportato un elenco parziale di caratteri non consentiti nei nomi dei server Novell:

" \* + . / : ; < = >? \[ \] \\ \|

Il **trasporto \_ IPX ncadg** è supportato dalla versione di NWLink fornita con MS client 3,0.

per le applicazioni client Windows a 16 bit che usano il trasporto **\_ IPX ncadg** è necessario che il file Nwipxspx.dll sia installato per l'esecuzione nel sottosistema WOW. Per ottenere questo file, contattare Novell.

Per ottenere gli indirizzi di rete e di nodo, usare l'utilità **ComCheck** di Novell o l'API **IPXGetInternetAddress** definita da Novell. In Windows è inoltre possibile ottenere questi indirizzi con il comando di **configurazione Ipxroute** .

La sintassi della stringa della porta di trasporto TCP/IP, come tutte le stringhe di porta, viene definita indipendentemente dalla specifica IDL. Il compilatore esegue alcune verifiche della sintassi, ma non garantisce che la specifica dell'endpoint sia corretta. È possibile che alcuni errori vengano segnalati in fase di esecuzione anziché in fase di compilazione.

> [!Note]  
> Questa famiglia di protocolli non è supportata in Windows XP.

 

## <a name="examples"></a>Esempi

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncadg_ipx:[1000]") 
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

[**\_SPX ncacn**](ncacn-spx.md)
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

[**\_UDP IP \_ ncadg**](ncadg-ip-udp.md)
</dt> <dt>

[Associazione stringa](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 