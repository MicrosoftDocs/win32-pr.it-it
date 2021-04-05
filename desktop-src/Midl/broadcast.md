---
title: Broadcast (attributo)
description: La parola chiave \ broadcast \ specifica che le chiamate a procedure remote devono essere inviate a tutti i server in una rete locale.
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
ms.openlocfilehash: 72c2bbb724fc292a5e3942bf2b6de61b5631cdc0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104334431"
---
# <a name="broadcast-attribute"></a>Broadcast (attributo)

La parola chiave **\[ broadcast \]** indica che le chiamate a procedure remote devono essere inviate a tutti i server in una rete locale.

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

*Interface-Attribute-List* 
</dt> <dd>

Specifica un elenco di zero o più attributi IDL che si applicano all'interfaccia nel suo complesso. Quando sono presenti due o più attributi di interfaccia, devono essere separati da virgole.

</dd> <dt>

*Nome interfaccia* 
</dt> <dd>

Specifica il nome dell'interfaccia.

</dd> <dt>

*elenco attributi* 
</dt> <dd>

Specifica gli attributi aggiuntivi da applicare alla funzione. Separare più attributi con virgole.

</dd> <dt>

*returnType* 
</dt> <dd>

Specifica il tipo restituito della funzione.

</dd> <dt>

*Nome funzione* 
</dt> <dd>

Specifica il nome della funzione a cui verrà applicato l'attributo **\[ broadcast \]** .

</dd> <dt>

*params* 
</dt> <dd>

Elenco dei parametri della funzione.

</dd> </dl>

## <a name="remarks"></a>Commenti

La parola chiave **\[ broadcast \]** specifica che la routine viene sempre trasmessa a tutti i server nella rete, anziché essere recapitata a un server specifico. Il client riceve l'output dalla prima risposta per restituire correttamente, mentre le risposte successive vengono scartate.

Un'operazione con l'attributo **\[ broadcast \]** è implicitamente un'operazione [**\[ idempotente \]**](idempotent.md) . Tuttavia, l'attributo **\[ broadcast \]** specifica proprietà aggiuntive che non sono disponibili nelle funzioni con l'attributo **\[ idempotente \]** . In particolare, le funzioni che usano l'attributo **\[ broadcast \]** specificano che la routine può essere chiamata più volte come risultato di una chiamata di procedura remota. Allo stesso tempo, possono essere inviati a più server. Questa operazione è diversa dall'attributo **\[ idempotente \]** , che specifica solo che è possibile ritentare una chiamata se non è stata completata.

Se una procedura remota trasmette la chiamata a tutti gli host in una rete locale, deve usare la sequenza di protocollo [**\_ IPX**](ncadg-ipx.md) [**ncadg \_ \_**](ncadg-ip-udp.md) o ncadg. Si noti che la dimensione di un pacchetto di **\[ broadcast \]** è determinata dal servizio datagramma in uso.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**idempotent**](idempotent.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Forse**](maybe.md)
</dt> <dt>

[**\_UDP IP \_ ncadg**](ncadg-ip-udp.md)
</dt> <dt>

[**ncadg \_ IPX**](ncadg-ipx.md)
</dt> </dl>

 

 




