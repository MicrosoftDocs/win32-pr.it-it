---
title: type_strict_context_handle attributo
description: Usare \ type \_ strict \_ context \_ handle\ in un file ACF per impostare restrizioni sugli handle di contesto.
ms.assetid: b67caad2-e87d-4eba-8555-8f347aadd515
keywords:
- type_strict_context_handle attributo MIDL
topic_type:
- apiref
api_name:
- type_strict_context_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef7e10c6231ac41287a08df7b9a0fa4e5361eddec9eb72bb6059b9f00dea5106
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105621"
---
# <a name="type_strict_context_handle-attribute"></a>Attributo type \_ strict \_ context \_ handle

Usare **\[ \_ \_ \_ l'handle \] di contesto type strict** in un file ACF per impostare restrizioni sugli handle di contesto.

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

*interface-attribute-list* 
</dt> <dd>

Altri attributi ACF che si applicano all'intera interfaccia. Gli attributi validi [**includono \_ l'handle automatico,**](auto-handle.md) [**\_ l'handle implicito,**](implicit-handle.md) [**\_ l'handle esplicito**](explicit-handle.md)e [**l'ottimizzazione,**](optimize.md) [**il codice**](code.md)o [**nocode.**](nocode.md) Separare più attributi con virgole.

</dd> <dt>

*interface-name* 
</dt> <dd>

Nome dell'interfaccia.

</dd> <dt>

*interface-definition-statements* 
</dt> <dd>

Una o più istruzioni MIDL che definiscono gli elementi [**dell'interfaccia**](interface.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

Per usare questo attributo, il flag -target deve essere impostato su NT60 (o versione successiva) quando si esegue midl.exe.

\[type \_ strict context handle è un \_ \_ \] superset funzionale \[ \_ dell'handle di contesto strict \_ \] . Nell'handle di contesto strict l'ID tipo dell'handle è sempre \[ 0. Nell'handle di contesto strict di tipo viene assegnato un ID tipo univoco dal \_ \_ \] \[ \_ \_ \_ \] compilatore MIDL.

È consigliabile usare \[ l'handle di contesto strict di tipo anziché \_ \_ \_ \] \[ \_ l'handle di contesto strict \_ \] . Gli handle di contesto non sono associati a un tipo specifico per impostazione predefinita. Quando nello stesso processo vengono usati più tipi di handle di contesto, è possibile che un client dannoso passi un handle di contesto al posto di un altro per produrre risultati indesiderati. L'uso di handle di contesto strict di tipo consente alle applicazioni di applicare la coerenza del tipo di handle di contesto e impedire qualsiasi utilizzo del tipo di handle di contesto \[ \_ non \_ \_ \] corrispondente.

Un handle di contesto con handle di contesto strict di tipo non può essere attribuita \[ anche con handle di contesto \_ strict \_ \_ \] \[ \_ \_ \] .

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[File di configurazione dell'applicazione (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**Codice**](code.md)
</dt> <dt>

[Handle di contesto](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[**serializzazione \_ dell'handle \_ di contesto**](context-handle-serialize.md)
</dt> <dt>

[**handle \_ di contesto \_ noserialize**](context-handle-noserialize.md)
</dt> <dt>

[**handle \_ esplicito**](explicit-handle.md)
</dt> <dt>

[**handle \_ implicito**](implicit-handle.md)
</dt> <dt>

[**nocode**](nocode.md)
</dt> <dt>

[**Ottimizzare**](optimize.md)
</dt> <dt>

[handle \_ di contesto \_ strict](strict-context-handle.md)
</dt> </dl>

 

 