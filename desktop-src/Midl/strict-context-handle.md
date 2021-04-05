---
title: attributo strict_context_handle
description: L'attributo \ Strict \_ Context \_ handle \ ACF imposta le restrizioni sugli handle di contesto.
ms.assetid: c34f9018-d519-4a75-ad6f-70d386a20817
keywords:
- attributo strict_context_handle MIDL
topic_type:
- apiref
api_name:
- strict_context_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8e66fd0754ec82de2354983e10e23ffc6329569
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103956371"
---
# <a name="strict_context_handle-attribute"></a>\_attributo handle di contesto Strict \_

L'attributo di **\[ \_ \_ gestione \] del contesto rigido** ACF imposta le restrizioni sugli handle di contesto.

``` syntax
[ 
    strict_context_handle 
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

In genere, quando una chiamata a un metodo di interfaccia genera un handle di contesto, tale handle diventa liberamente disponibile per qualsiasi altra interfaccia. Quando si usa l'attributo **\[ strict \_ Context \_ handle \]** , si garantisce che i metodi di tale interfaccia accettino solo handle di contesto creati da un metodo dalla stessa interfaccia. Le interfacce compilate senza un **\[ \_ \_ handle \] di contesto rigido** non accettano handle di contesto creati in interfacce compilate con un **\[ \_ \_ \] handle di contesto rigido**

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

[tipo \_ strict \_ handle di contesto \_](type-strict-context-handle.md)
</dt> </dl>

 

 