---
title: attributo type_strict_context_handle
description: "\\_ \\_ Per impostare le restrizioni sugli handle di contesto, utilizzare l'handle di contesto Strict \\ Type \\_ \\ in un file ACF."
ms.assetid: b67caad2-e87d-4eba-8555-8f347aadd515
keywords:
- attributo type_strict_context_handle MIDL
topic_type:
- apiref
api_name:
- type_strict_context_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e16c9ae74d618b1b0cafef2c5bf618085d79284
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472790"
---
# <a name="type_strict_context_handle-attribute"></a>Digitare \_ l' \_ attributo dell'handle di contesto Strict \_

Usare l' **\[ \_ \_ \_ handle \] di contesto Strict di tipo** in un file ACF per impostare le restrizioni sugli handle di contesto.

``` syntax
[ 
    type_strict_context_handle 
    [, interface-attribute-list] 
] 
interface interface-name
{
    interface-definition-statements
}
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*Interface-Attribute-List* 
</dt> <dd>

Altri attributi di ACF che si applicano all'interfaccia nel suo complesso. Gli attributi validi [**includono \_ handle automatico**](auto-handle.md), [**\_ handle implicito**](implicit-handle.md), [**\_ handle esplicito**](explicit-handle.md)e [**ottimizza**](optimize.md), [**codice**](code.md)o [**NoCode**](nocode.md). Separare più attributi con virgole.

</dd> <dt>

*Nome interfaccia* 
</dt> <dd>

Nome dell'interfaccia.

</dd> <dt>

*Interface-Definition-Statements* 
</dt> <dd>

Una o più istruzioni MIDL che definiscono gli elementi dell' [**interfaccia**](interface.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

Per usare questo attributo, il flag-target deve essere impostato su NT60 (o versione successiva) quando si esegue midl.exe.

\[\_il tipo \_ strict \_ handle \] di contesto è un superset funzionale dell' \[ handle di \_ contesto Strict \_ \] . In \[ \_ un handle di contesto rigoroso \_ \] , l'ID del tipo dell'handle è sempre 0; nell' \[ handle di contesto Strict del tipo \_ \_ \_ \] , un ID di tipo univoco viene assegnato dal compilatore MIDL.

È consigliabile usare un \[ handle di \_ \_ contesto Strict \_ del tipo anziché un \] \[ handle di contesto rigoroso \_ \_ \] . Per impostazione predefinita, gli handle di contesto non sono associati a un tipo specifico. Quando nello stesso processo vengono usati più tipi di handle di contesto, è possibile che un client malintenzionato passi un handle di contesto al posto di un altro per produrre risultati non desiderati. L'utilizzo di \[ \_ un handle di contesto di tipo strict \_ consente alle \_ \] applicazioni di applicare la coerenza del tipo di handle del contesto ed evitare qualsiasi utilizzo del tipo di handle del contesto non corrispondente.

Un handle di contesto attribuito con un \[ \_ handle di contesto Strict di tipo \_ \_ \] non può essere attribuito anche con un \[ handle di \_ contesto rigido \_ \] .

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[File di configurazione dell'applicazione (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**codice**](code.md)
</dt> <dt>

[Handle di contesto](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[**\_serializzazione handle di contesto \_**](context-handle-serialize.md)
</dt> <dt>

[**gestore del contesto \_ \_ noserialize**](context-handle-noserialize.md)
</dt> <dt>

[**handle esplicito \_**](explicit-handle.md)
</dt> <dt>

[**handle implicito \_**](implicit-handle.md)
</dt> <dt>

[**NoCode**](nocode.md)
</dt> <dt>

[**ottimizzare**](optimize.md)
</dt> <dt>

[\_handle di contesto Strict \_](strict-context-handle.md)
</dt> </dl>

 

 