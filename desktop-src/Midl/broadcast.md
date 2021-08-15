---
title: attributo broadcast
description: La parola chiave \broadcast\ specifica che le chiamate di procedura remota devono essere inviate a tutti i server in una rete locale.
ms.assetid: 3951c80f-b7f1-457b-9eee-6e075291b27e
keywords:
- attributo broadcast MIDL
topic_type:
- apiref
api_name:
- broadcast
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f176b03f9d33ee1bbe1d0e805dfc109de477b7499f8fd624ba7732709dc61a10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118385237"
---
# <a name="broadcast-attribute"></a>attributo broadcast

La parola **\[ chiave broadcast \]** specifica che le chiamate di procedura remota devono essere inviate a tutti i server in una rete locale.

``` syntax
[
    interface-attribute-list
] 
interface interface-name 
{
    [broadcast [, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*interface-attribute-list* 
</dt> <dd>

Specifica un elenco di zero o più attributi IDL che si applicano all'intera interfaccia. Quando sono presenti due o più attributi di interfaccia, devono essere separati da virgole.

</dd> <dt>

*interface-name* 
</dt> <dd>

Specifica il nome dell'interfaccia.

</dd> <dt>

*attribute-list* 
</dt> <dd>

Specifica attributi aggiuntivi da applicare alla funzione. Separare più attributi con virgole.

</dd> <dt>

*Returntype* 
</dt> <dd>

Specifica il tipo restituito della funzione.

</dd> <dt>

*function-name* 
</dt> <dd>

Specifica il nome della funzione a cui verrà **applicato \[ \]** l'attributo broadcast.

</dd> <dt>

*params* 
</dt> <dd>

Elenco di parametri della funzione.

</dd> </dl>

## <a name="remarks"></a>Commenti

La parola chiave **\[ broadcast \]** specifica che la routine viene sempre trasmessa a tutti i server della rete, anziché essere recapitata a un server specifico. Il client riceve l'output dalla prima risposta per restituire correttamente, mentre le risposte successive vengono rimosse.

Un'operazione con **\[ l'attributo broadcast \]** è implicitamente [**\[ un'operazione idempotente. \]**](idempotent.md) Tuttavia, **\[ l'attributo broadcast \]** specifica proprietà aggiuntive che non sono disponibili nelle funzioni con l'attributo **\[ idempotente. \]** In particolare, le funzioni che **\[ usano l'attributo broadcast \]** specificano che la routine può essere chiamata più volte come risultato di una chiamata di procedura remota. Allo stesso tempo, possono essere inviati a più server. Questo è diverso **\[ dall'attributo \] idempotente,** che specifica solo che è possibile ritentare una chiamata se non viene completata.

Se una procedura remota trasmette la chiamata a tutti gli host in una rete locale, deve usare la sequenza di protocollo [**ncadg \_ ip \_ udp**](ncadg-ip-udp.md) o [**\_ ncadg ipx.**](ncadg-ipx.md) Si noti che le dimensioni di un **\[ pacchetto broadcast \]** sono determinate dal servizio datagrammi in uso.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**idempotent**](idempotent.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Forse**](maybe.md)
</dt> <dt>

[**ncadg \_ ip \_ udp**](ncadg-ip-udp.md)
</dt> <dt>

[**ncadg \_ ipx**](ncadg-ipx.md)
</dt> </dl>

 

 




