---
title: ncadg_ipx attributo
description: La parola chiave ncadg \_ ipx identifica IPX come famiglia di protocolli per l'endpoint. Questa famiglia di protocolli è obsoleta e non deve essere usata nelle nuove applicazioni.
ms.assetid: 6b136eb9-4e18-43ff-993b-a2ad005273f1
keywords:
- ncadg_ipx attributo MIDL
topic_type:
- apiref
api_name:
- ncadg_ipx
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbca1ef3cb5f51e54fe8b95aa16326c6438903ff9717258edea9fac491eebafa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067051"
---
# <a name="ncadg_ipx-attribute"></a>Attributo \_ ipx ncadg

La **parola chiave ncadg \_ ipx** identifica IPX come famiglia di protocolli per l'endpoint. Questa famiglia di protocolli è obsoleta e non deve essere usata nelle nuove applicazioni.

``` syntax
endpoint("ncadg_ipx:link-address[port-name]")
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*link-address* 
</dt> <dd>

Specifica il server host. Può trattarsi di una stringa di caratteri (nome del server) o di un numero esadecimale di 20 cifre costituito dall'indirizzo di rete del server host (8 cifre) concatenato all'indirizzo del nodo (12 cifre). Per istruzioni su come ottenere l'indirizzo di rete e l'indirizzo del nodo, vedere Osservazioni. Una **stringa NULL** specifica il computer locale.

</dd> <dt>

*port-name* 
</dt> <dd>

Specifica un numero facoltativo a 16 bit che rappresenta l'indirizzo del socket. I valori possono essere da 1 a 65535. Se non viene specificato alcun valore, il servizio di mapping degli endpoint seleziona un valore *di nome porta* valido.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le restrizioni seguenti si applicano ai protocolli datagrammi, **ncadg \_ ipx** e [**ncadg \_ ip \_ udp:**](ncadg-ip-udp.md)

-   Non supportano i callback. Tutte le funzioni che usano **\[** [**l'attributo di callback**](callback.md) avranno esito **\]** negativo.
-   Non supportano l'uso del costruttore [**del tipo di**](pipe.md) pipe.

Quando si usa **il trasporto \_ ncadg ipx,** il nome del server corrisponde esattamente al nome del server Windows 32 bit. Tuttavia, poiché i nomi vengono distribuiti tramite protocolli Novell, devono essere conformi alle convenzioni di denominazione di Novell. Se un nome di server non è un nome Novell valido, i server non saranno in grado di creare endpoint con il **trasporto \_ ipx ncadg.** Di seguito è riportato un elenco parziale di caratteri non consentiti nei nomi dei server Novell:

" \* + . / : ; < = > ? \[ \] \\ \|

Il **trasporto \_ ncadg ipx** è supportato dalla versione di NWLink fornita con MS Client 3.0.

Le applicazioni client Windows a 16 bit che usano il trasporto **\_ ipx ncadg** richiedono che il Nwipxspx.dll file sia installato per poter essere eseguito nel sottosistema WOW. Per ottenere questo file, contattare Novell.

Per ottenere gli indirizzi di rete e nodo, usare l'utilità **comcheck** di Novell o l'API definita da Novell **IPXGetInternetAddress**. In Windows, è anche possibile ottenere questi indirizzi con il **comando ipxroute config.**

La sintassi della stringa di porta del trasporto TCP/IP, come tutte le stringhe di porta, è definita indipendentemente dalla specifica IDL. Il compilatore esegue un controllo della sintassi, ma non garantisce che la specifica dell'endpoint sia corretta. Alcuni errori possono essere segnalati in fase di esecuzione anziché in fase di compilazione.

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

[**Endpoint**](endpoint.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**ncacn \_ in \_ dsp**](ncacn-at-dsp.md)
</dt> <dt>

[**ncacn \_ dnet \_ nsp**](ncacn-dnet-nsp.md)
</dt> <dt>

[**ncacn \_ ip \_ tcp**](ncacn-ip-tcp.md)
</dt> <dt>

[**ncacn \_ nb \_ ipx**](ncacn-nb-ipx.md)
</dt> <dt>

[**ncacn \_ spx**](ncacn-spx.md)
</dt> <dt>

[**ncacn \_ nb \_ nb**](ncacn-nb-nb.md)
</dt> <dt>

[**ncacn \_ nb \_ tcp**](ncacn-nb-tcp.md)
</dt> <dt>

[**ncacn \_ np**](ncacn-np.md)
</dt> <dt>

[**ncacn \_ vns \_ spp**](ncacn-vns-spp.md)
</dt> <dt>

[**ncalrpc**](ncalrpc.md)
</dt> <dt>

[**ncadg \_ ip \_ udp**](ncadg-ip-udp.md)
</dt> <dt>

[associazione di stringhe](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 