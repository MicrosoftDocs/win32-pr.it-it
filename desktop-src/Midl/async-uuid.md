---
title: async_uuid (attributo)
description: L'attributo \ Async \_ UUID \ Interface indica al compilatore MIDL di definire versioni sincrone e asincrone di un'interfaccia com.
ms.assetid: 1c20eaa1-78b5-4463-a8c1-d81e55d5c618
keywords:
- attributo async_uuid MIDL
topic_type:
- apiref
api_name:
- async_uuid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39fd7b4d9d9bf7a595415e55de778a419d91051c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104117643"
---
# <a name="async_uuid-attribute"></a>\_attributo uuid asincrono

L'attributo di interfaccia **\[ \_ UUID \] asincrono** indica al compilatore MIDL di definire versioni sincrone e asincrone di un'interfaccia com.

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

*stringa-uuid1* 
</dt> <dd>

Stringa UUID, generata dall'utilità uuidgen, che identifica la versione sincrona dell'interfaccia.

</dd> <dt>

*stringa-UUID2* 
</dt> <dd>

Stringa UUID, generata dall'utilità uuidgen, che identifica la versione asincrona dell'interfaccia.

</dd> <dt>

*Interface-Attribute-List* 
</dt> <dd>

Altri attributi applicabili all'interfaccia nel suo complesso. Non è possibile usare l'attributo [**\[ version \]**](version.md) in un'interfaccia com.

</dd> <dt>

*Nome interfaccia* 
</dt> <dd>

Nome dell'interfaccia.

</dd> <dt>

*interfaccia di base* 
</dt> <dd>

Interfaccia da cui deriva questa interfaccia. L'interfaccia di base deve essere **IUnknown** o un'interfaccia asincrona che deriva direttamente o indirettamente da **IUnknown**.

</dd> <dt>

*interfaccia-definizione* 
</dt> <dd>

Specifica le istruzioni IDL che formano la definizione dell'interfaccia.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'uso di questo attributo richiede Windows 2000 o versioni successive di Windows.

Quando si applica l'attributo **\[ \_ UUID \] asincrono** a un'interfaccia com, ovvero un'interfaccia con l'attributo [**\[ Object \]**](object.md) , il compilatore MIDL genera una definizione asincrona dell'interfaccia, oltre alla versione sincrona tradizionale. L'interfaccia asincrona avrà gli stessi nomi dell'interfaccia sincrona, ma con un prefisso "Async". L'identificatore di interfaccia (IID) sarà l'UUID specificato come parametro per l'attributo **\[ \_ UUID \] asincrono** .

Per l'interfaccia asincrona, MIDL suddivide ogni metodo in metodi *Begin* e *Finish* distinti. Il metodo *Begin* ha il nome del metodo sincrono con un \_ prefisso "Begin" e include tutti i parametri [**\[ in \]**](in.md) del metodo sincrono. Il metodo *Finish* ha il nome del metodo sincrono con un prefisso "Finish \_ " e include tutti i parametri [**\[ out \]**](out-idl.md) del metodo sincrono. Se il metodo sincrono include un parametro **\[ in \] ,** i parametri out verranno inclusi nei metodi asincroni *Begin* e *Finish* .

Se un metodo di interfaccia asincrono ha la [**\[ chiamata \_ come \]**](call-as.md) attributo, MIDL genererà le dichiarazioni per i metodi *Begin* e *Finish* . È necessario implementare entrambi i metodi.

Ogni interfaccia asincrona è un modificatore su un'interfaccia sincrona e, di conseguenza, non ha un grafo di ereditarietà separato. Ciò significa che non è possibile definire un'interfaccia sincrona da un'interfaccia asincrona (diversa da **IUnknown**). Né possono ereditare interfacce sincrone da interfacce asincrone. Se si tenta di eseguire una delle due, il compilatore MIDL genererà un messaggio di errore.

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

[**chiama \_ come**](call-as.md)
</dt> <dt>

[**IID \_ è**](iid-is.md)
</dt> <dt>

[**in**](in.md)
</dt> <dt>

[**locale**](local.md)
</dt> <dt>

[**oggetto**](object.md)
</dt> <dt>

[**out**](out-idl.md)
</dt> <dt>

[**Versione**](version.md)
</dt> </dl>

 

 