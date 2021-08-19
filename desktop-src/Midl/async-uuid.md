---
title: async_uuid (attributo)
description: L'attributo di interfaccia \ async uuid\ indica al compilatore MIDL di definire versioni sincrone e \_ asincrone di un'interfaccia COM.
ms.assetid: 1c20eaa1-78b5-4463-a8c1-d81e55d5c618
keywords:
- async_uuid attributo MIDL
topic_type:
- apiref
api_name:
- async_uuid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83a784cadf470fa312a82e473f3934dbda1a2b6dce20d2ae34c7074c309398cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117808235"
---
# <a name="async_uuid-attribute"></a>Attributo \_ async uuid

**\[ L'attributo \_ dell'interfaccia asincrona uuid \]** indica al compilatore MIDL di definire versioni sincrone e asincrone di un'interfaccia COM.

``` syntax
[ 
    object, 
    uuid(string-uuid1), 
    async_uuid(string-uuid2)[ [, interface-attribute-list] 
]
interface interface-name : base-interface
{
    interface-definition
}
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*string-uuid1* 
</dt> <dd>

Stringa UUID, generata dall'utilità Uuidgen, che identifica la versione sincrona dell'interfaccia.

</dd> <dt>

*string-uuid2* 
</dt> <dd>

Stringa UUID, generata dall'utilità Uuidgen, che identifica la versione asincrona dell'interfaccia.

</dd> <dt>

*interface-attribute-list* 
</dt> <dd>

Altri attributi che si applicano all'intera interfaccia. Non è possibile usare [**\[ l'attributo version \]**](version.md) in un'interfaccia COM.

</dd> <dt>

*interface-name* 
</dt> <dd>

Nome dell'interfaccia.

</dd> <dt>

*interfaccia di base* 
</dt> <dd>

Interfaccia da cui deriva questa interfaccia. L'interfaccia di base deve **essere IUnknown** o un'interfaccia asincrona che deriva, direttamente o indirettamente, da **IUnknown**.

</dd> <dt>

*interface-definition* 
</dt> <dd>

Specifica le istruzioni IDL che formano la definizione dell'interfaccia.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'uso di questo attributo richiede Windows 2000 o versioni successive di Windows.

Quando si applica l'attributo **\[ \_ async uuid \]** a un'interfaccia COM, ovvero un'interfaccia con l'attributo [**\[ object, \]**](object.md) il compilatore MIDL genera una definizione asincrona dell'interfaccia, oltre alla versione sincrona tradizionale. L'interfaccia asincrona avrà gli stessi nomi dell'interfaccia sincrona, ma con un prefisso "Async". L'identificatore di interfaccia (IID) sarà l'UUID specificato come parametro per **\[ l'attributo \_ uuid \] asincrono.**

Per l'interfaccia asincrona, MIDL suddivide ogni metodo in metodi *begin* *e finish* separati. Il *metodo begin* ha il nome del metodo sincrono con un prefisso "Begin" e include tutti i parametri \_ [**\[ in \]**](in.md) del metodo sincrono. Il *metodo finish* ha il nome del metodo sincrono con un prefisso "Finish" e include tutti i parametri out \_ [**\[ \]**](out-idl.md) dal metodo sincrono. Se il metodo sincrono dispone di **\[ parametri in , \] i** parametri out verranno inclusi nei metodi asincroni *begin* *e finish.*

Se un metodo di interfaccia asincrono ha la [**\[ chiamata \_ come \]**](call-as.md) attributo, MIDL genererà dichiarazioni per i metodi *begin* *e finish.* È necessario implementare entrambi i metodi.

Ogni interfaccia asincrona è un modificatore su un'interfaccia sincrona e, di conseguenza, non dispone di un grafico di ereditarietà separato. Ciò significa che non è possibile definire un'interfaccia sincrona da un'interfaccia asincrona (diversa da **IUnknown**). Né le interfacce sincrone possono ereditare da interfacce asincrone. Il compilatore MIDL genera un messaggio di errore se si tenta di provarne uno.

## <a name="examples"></a>Esempi

``` syntax
[
    object, 
    uuid(0c733a30-2a1c-11ce-ade5-00aa0044773d),
    async_uuid(1c733a30-2a1c-11ce-ade5-00aa0044773d),
    pointer_default(unique)
]
interface IMyInterface : IUnknown
{
    /* Interface definition goes here*/
}
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Definizione di interfacce COM](/windows/desktop/com/defining-com-interfaces)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**chiamare \_ come**](call-as.md)
</dt> <dt>

[**iid \_ è**](iid-is.md)
</dt> <dt>

[**Pollici**](in.md)
</dt> <dt>

[**Locale**](local.md)
</dt> <dt>

[**Oggetto**](object.md)
</dt> <dt>

[**in uscita**](out-idl.md)
</dt> <dt>

[**Versione**](version.md)
</dt> </dl>

 

 