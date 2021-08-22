---
title: strict_context_handle attributo
description: L'attributo \ strict \_ context \_ handle\ ACF imposta restrizioni sugli handle di contesto.
ms.assetid: c34f9018-d519-4a75-ad6f-70d386a20817
keywords:
- strict_context_handle attributo MIDL
topic_type:
- apiref
api_name:
- strict_context_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0db19c74efa323fa7e3abc4bfd17c14a471cbb9c81414ae78064f84bfc19fa7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013579"
---
# <a name="strict_context_handle-attribute"></a>Attributo strict \_ context \_ handle

L'attributo ACF **\[ strict context \_ \_ handle \]** imposta restrizioni sugli handle di contesto.

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

*interface-attribute-list* 
</dt> <dd>

Altri attributi ACF che si applicano all'interfaccia nel suo complesso. Gli attributi validi [**includono \_ l'handle automatico,**](auto-handle.md) [**\_ l'handle implicito,**](implicit-handle.md)l'handle [**\_ esplicito**](explicit-handle.md)e [**l'ottimizzazione**](optimize.md)di , il [**codice**](code.md)o [**nocode.**](nocode.md) Separare più attributi con virgole.

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

In genere, quando una chiamata a un metodo di interfaccia genera un handle di contesto, tale handle diventa disponibile gratuitamente per qualsiasi altra interfaccia. Quando si usa **\[ l'attributo strict context \_ \_ handle, \]** si garantisce che i metodi in tale interfaccia accettino solo gli handle di contesto creati da un metodo dalla stessa interfaccia. Le interfacce compilate senza **\[ handle di contesto \_ \_ strict \]** non possono accettare handle di contesto creati in interfacce compilate con **\[ handle di \_ contesto \_ strict \]**.

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

[**context \_ handle \_ noserialize**](context-handle-noserialize.md)
</dt> <dt>

[**handle \_ esplicito**](explicit-handle.md)
</dt> <dt>

[**handle \_ implicito**](implicit-handle.md)
</dt> <dt>

[**nocode**](nocode.md)
</dt> <dt>

[**Ottimizzare**](optimize.md)
</dt> <dt>

[handle \_ di contesto type strict \_ \_](type-strict-context-handle.md)
</dt> </dl>

 

 