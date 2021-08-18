---
title: in (attributo)
description: L'attributo \ in\ indica che un parametro deve essere passato dalla routine chiamante alla routine chiamata.
ms.assetid: 85d5617e-8b73-449a-9627-2c8d5ab2b629
keywords:
- nell'attributo MIDL
topic_type:
- apiref
api_name:
- in
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb78ad08dd5ba5494181d3fb2adecb7a8441e4716c42ba6cd4f1c119b3ccb046
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067231"
---
# <a name="in-attribute"></a>in (attributo)

**\[ L'attributo in \]** indica che un parametro deve essere passato dalla routine chiamante alla routine chiamata.

``` syntax
[ [function-attribute-list] ] type-specifier [pointer-declarator] function-name(
    [ in [ , parameter-attribute-list ] ] type-specifier [declarator]
    , ...);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*function-attribute-list* 
</dt> <dd>

Specifica zero o più attributi che si applicano alla funzione. Gli attributi di funzione validi sono **\[ \] callback**, **\[ local \]**, pointer attribute **\[ ref \]**, **\[ unique \]** o **\[ ptr \]** e gli attributi di utilizzo **\[ string \]**, **\[ ignore \]** e context **\[ \_ handle \]**.

</dd> <dt>

*type-specifier* 
</dt> <dd>

Specifica un tipo **di \_ base,** [**uno struct,**](struct.md) [**un'unione**](union.md)o un tipo [**enum**](enum.md) o un identificatore di tipo. Una specifica di archiviazione facoltativa può precedere *type-specifier*.

</dd> <dt>

*dichiaratore di puntatore* 
</dt> <dd>

Specifica zero o più dichiaratori di puntatore. Un dichiaratore di puntatore è lo stesso del dichiaratore di puntatore usato in C; viene costruito dal \* designatore, dai modificatori come **far** e dal qualificatore [**const**](const.md).

</dd> <dt>

*function-name* 
</dt> <dd>

Specifica il nome della procedura remota.

</dd> <dt>

*parameter-attribute-list* 
</dt> <dd>

Specifica zero o più attributi appropriati per il tipo di parametro specificato. Gli attributi di parametro con l'attributo **\[ \]** **\[ in \]** possono anche rimuovere l'attributo direzionale; **\[ \]** **\[ \]** **\[ \]** **\[ \_ \]** **\[ \_ \]** **\[ \_ \]** **\[ \_ \]** **\[ \_ \]** gli attributi di campo prima sono , **\[ \_ \]** last è , length è , max è , size è e switch type ; l'attributo puntatore ref , unique o **\[ ptr \]** e l'handle **\[ \_ \]** di contesto e la stringa degli attributi di utilizzo . L'attributo **\[ di utilizzo ignore \]** non può essere usato come attributo di parametro. Separare più attributi con virgole.

</dd> <dt>

*Dichiaratore* 
</dt> <dd>

Specifica dichiaratori C standard, ad esempio identificatori, dichiaratori di puntatore e dichiaratori di matrice. Per altre informazioni, vedere [Matrici e Sized-Pointer attributi](array-and-sized-pointer-attributes.md), [**matrici**](arrays-1.md)e [matrici e puntatori](/windows/desktop/Rpc/arrays-and-pointers). Il dichiaratore di parametro nel dichiaratore di funzione, ad esempio il nome del parametro, è facoltativo.

</dd> </dl>

## <a name="remarks"></a>Commenti

**\[ L'attributo in \]** ha un attributo inverso, out , che indica che un parametro deve essere restituito dalla routine chiamata alla routine **\[** [](out-idl.md) **\]** chiamante. Gli **\[ attributi \] in** e **\[ out \]** sono noti come attributi dei parametri direzionali perché specificano la direzione in cui vengono passati i parametri. Un parametro può essere definito **\[ come \] in**, **\[ out \]** o **\[ in**, **out \]**.

**\[ L'attributo in \]** identifica i parametri di cui viene effettuato il marshalling dallo stub client per la trasmissione al server.

**\[ L'attributo in \]** viene applicato a un parametro per impostazione predefinita quando non viene specificato alcun attributo di parametro direzionale.

## <a name="examples"></a>Esempi

``` syntax
HRESULT MyFunction([in] short count);
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**midl \_ user \_ allocate**](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[**in uscita**](out-idl.md)
</dt> </dl>

 

 