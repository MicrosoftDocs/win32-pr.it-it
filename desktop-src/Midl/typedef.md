---
title: typedef (attributo)
description: La parola chiave typedef di IDL consente dichiarazioni typedef molto simili alle dichiarazioni typedef del linguaggio C.
ms.assetid: 995a233e-0d07-4051-9f00-d1dc0b563f8f
keywords:
- typedef attributo MIDL
topic_type:
- apiref
api_name:
- typedef
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecfce98e5a83f8d2a5e2499a5ceceba755e68f2c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725143"
---
# <a name="typedef-attribute"></a>typedef (attributo)

La parola chiave **typedef** di IDL consente dichiarazioni **typedef** molto simili alle dichiarazioni **typedef** del linguaggio C.

``` syntax
/* IDL file typedef syntax */
typedef [[ [ idl-type-attribute-list ] ]] type-specifier declarator-list;

/* ACF typedef syntax */
typedef [ acf-type-attribute-list ] typename;
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*IDL-Type-Attribute-List* 
</dt> <dd>

Specifica uno o più attributi che si applicano al tipo. Gli attributi di tipo validi in un file IDL includono **\[** [**handle**](handle.md) **\]** , **\[** [**\_ tipo di commutione**](switch-type.md) **\]** , **\[** [**trasmissione \_ come**](transmit-as.md), **\]** il riferimento all'attributo del puntatore **\[** [](ref.md) **\]** , **\[** [**univoco**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** e gli attributi di utilizzo **\[** [**\_ gestione del contesto**](context-handle.md) **\]** , **\[** [**stringa**](string.md) **\]** e **\[** [**Ignora**](ignore.md) **\]** . Separare più attributi con virgole.

</dd> <dt>

*identificatore di tipo* 
</dt> <dd>

Specifica un [tipo di base](midl-base-types.md), uno [**struct**](struct.md), un' [**Unione**](union.md), un tipo [**enum**](enum.md) o un identificatore di tipo. Una specifica di archiviazione facoltativa può precedere *Type-specifier*. La parola chiave [**const**](const.md) può precedere *Type-specifier*.

</dd> <dt>

*elenco di dichiaratori* 
</dt> <dd>

Specifica i dichiaratori MIDL standard, ad esempio identificatori, dichiaratori di puntatore e dichiaratori di matrici. Per altre informazioni, vedere [matrici e Sized-Pointer attributi](array-and-sized-pointer-attributes.md), [**matrici**](arrays-1.md)e [matrici e puntatori](/windows/desktop/Rpc/arrays-and-pointers). Il *declarator-list* è costituito da uno o più dichiaratori, separati da virgole.

</dd> <dt>

*ACF-Type-Attribute-List* 
</dt> <dd>

Specifica uno o più attributi che si applicano al tipo. Gli attributi di tipo validi in un ACF includono **\[** [**allocare**](allocate.md) **\]** , **\[** [**codificare**](encode.md) **\]** e **\[** [**decodificare**](decode.md) **\]** .

</dd> <dt>

*typeName* 
</dt> <dd>

Specifica un tipo definito nel file IDL.

</dd> </dl>

## <a name="remarks"></a>Commenti

La dichiarazione di **typedef** IDL è aumentata per consentire di associare gli attributi di tipo ai tipi definiti. Gli attributi di tipo validi includono **\[** [**handle**](handle.md) **\]** , **\[** [**\_ tipo di commutione**](switch-type.md) **\]** , **\[** [**trasmissione \_ come**](transmit-as.md) **\]** ; riferimento all'attributo del puntatore **\[** [](ref.md) **\]** , **\[** [**univoco**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** e l' **\[** [**\_ handle di contesto**](context-handle.md) **\]** , la **\[** [**stringa**](string.md) **\]** e l' **\[** [**Ignore**](ignore.md) **\]** degli attributi di utilizzo.

La parola chiave **typedef** in un ACF applica gli attributi ai tipi definiti nel file IDL corrispondente. Ad esempio, l'attributo [**allocate**](allocate.md) Type consente di personalizzare l'allocazione e la deallocazione della memoria sia dall'applicazione che dagli stub.

L'istruzione ACF **typedef** viene visualizzata come parte del corpo di ACF. Si noti che la sintassi di ACF **typedef** è diversa dalla sintassi **typedef** di IDL e dalla sintassi **typedef** del linguaggio C. Non è possibile introdurre nuovi tipi nell'ACF.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[File di configurazione dell'applicazione (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**allocare**](allocate.md)
</dt> <dt>

[**matrici**](arrays-1.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[**handle di contesto \_**](context-handle.md)
</dt> <dt>

[**decodificare**](decode.md)
</dt> <dt>

[**codificare**](encode.md)
</dt> <dt>

[**enum**](enum.md)
</dt> <dt>

[**gestire**](handle.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**ignorare**](ignore.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**string**](string.md)
</dt> <dt>

[**struct**](struct.md)
</dt> <dt>

[**tipo di opzione \_**](switch-type.md)
</dt> <dt>

[**Trasmetti \_ come**](transmit-as.md)
</dt> <dt>

[**Unione**](union.md)
</dt> <dt>

[**unico**](unique.md)
</dt> </dl>

 

 