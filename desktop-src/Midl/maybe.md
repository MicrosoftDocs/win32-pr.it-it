---
title: Attributo maybe
description: La parola chiave \ maybe\ indica che la chiamata di procedura remota non deve essere eseguita ogni volta che viene chiamata e il client non prevede una risposta. Si noti che il protocollo \maybe\ non garantisce né il recapito né il completamento della chiamata.
ms.assetid: 163b9fd5-7dce-493e-95bc-63807f42a498
keywords:
- attributo maybe MIDL
topic_type:
- apiref
api_name:
- maybe
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 178faf3d308f7dd282e31a8f0eabf8708bb8b3fe1a0d52a981e65adddb258ad1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067151"
---
# <a name="maybe-attribute"></a>Attributo maybe

La parola **\[ chiave potrebbe \]** indicare che la chiamata di procedura remota non deve essere eseguita ogni volta che viene chiamata e il client non prevede una risposta. Si noti che **\[ il protocollo maybe \]** non garantisce né il recapito né il completamento della chiamata.

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

Specifica il nome della funzione a cui verrà applicato **\[ \] l'attributo** maybe.

</dd> <dt>

*params* 
</dt> <dd>

Elenco di parametri della funzione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Una chiamata con **\[ l'attributo \] maybe** non può contenere parametri di output ed è implicitamente una chiamata **\[** [**idempotente.**](idempotent.md) **\]**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Trasmissione**](broadcast.md)
</dt> <dt>

[**idempotent**](idempotent.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> </dl>

 

 




