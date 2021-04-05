---
title: attributo forse
description: La parola chiave \ Maybe indica che non è necessario eseguire la chiamata di procedura remota ogni volta che viene chiamata e che il client non prevede una risposta. Si noti che il protocollo \ Maybe non garantisce né il recapito né il completamento della chiamata.
ms.assetid: 163b9fd5-7dce-493e-95bc-63807f42a498
keywords:
- attributo MIDL probabilmente
topic_type:
- apiref
api_name:
- maybe
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68704e19d421150444933d74f6b78fc5bada46f6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045570"
---
# <a name="maybe-attribute"></a>attributo forse

La parola chiave **\[ potrebbe \]** indicare che non è necessario eseguire la chiamata di procedura remota ogni volta che viene chiamata e che il client non prevede una risposta. Si noti che il protocollo **\[ probabilmente \]** non garantisce né il recapito né il completamento della chiamata.

``` syntax
[
    interface-attribute-list
] 
interface interface-name 
{
    [maybe [, attribute-list]] returntype function-name(params)
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

Specifica il nome della funzione a cui verrà applicato l'attributo **\[ Maybe \]** .

</dd> <dt>

*params* 
</dt> <dd>

Elenco dei parametri della funzione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Una chiamata con l'attributo **\[ Maybe \]** non può contenere parametri di output ed è implicitamente una **\[** [**chiamata idempotente**](idempotent.md) **\]** .

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**trasmissione**](broadcast.md)
</dt> <dt>

[**idempotent**](idempotent.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> </dl>

 

 




