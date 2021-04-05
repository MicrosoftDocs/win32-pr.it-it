---
title: Annota attributo
description: L'attributo \ annotate \ consente di specificare una stringa di annotazione SAL per il metodo, il parametro o il campo della struttura specificato.
ms.assetid: D0A35DCD-BD2F-455B-A040-5D63E4572D83
keywords:
- Annota attributo MIDL
topic_type:
- apiref
api_name:
- annotate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 820310c6aca0e5269d6febff5dc7d3208413110c
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "103732087"
---
# <a name="annotate-attribute"></a>Annota attributo

L'attributo annotate consente di specificare una stringa di annotazione SAL per il metodo, il parametro o il campo della struttura specificato. **\[ \]**

``` syntax
[ annotation(â€œstringâ€0,  [, function-attribute-list] ] function-declarator ;
[ [function-attribute-list] ] type-specifier [pointer-declarator] function-name(
    [ annotation(â€œstringâ€) [ , parameter-attribute-list ] ] type-specifier [declarator]
    , ...);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*string* 
</dt> <dd>

Stringa di annotazione SAL specificata.

</dd> <dt>

*Function-Attribute-List* 
</dt> <dd>

Specifica zero o più attributi che si applicano alla funzione. Gli attributi di funzione validi includono [**\[ \] callback**](callback.md), gli attributi del puntatore [**\[ ref \]**](ref.md), [**\[ Unique \]**](unique.md)o [**\[ \] ptr**](ptr.md)e la [**\[ stringa \]**](string.md)degli attributi di utilizzo, [**\[ Ignore \]**](ignore.md)e l' [**\[ \_ handle \] di contesto**](context-handle.md). Più attributi devono essere separati da virgole.

</dd> <dt>

*Function-dichiaratore* 
</dt> <dd>

Specifica l'identificatore di tipo, il nome della funzione e l'elenco di parametri per la funzione.

</dd> <dt>

*identificatore di tipo* 
</dt> <dd>

Specifica un **\_ tipo di base**, uno [**\[ struct \]**](struct.md), un' [**Unione**](union.md)o un tipo [**\[ enum \]**](enum.md) o un identificatore di tipo. Una specifica di archiviazione facoltativa può precedere *Type-specifier*.

</dd> <dt>

*puntatore-dichiaratore* 
</dt> <dd>

Specifica zero o più dichiaratori di puntatore. Un dichiaratore di puntatore è lo stesso di un dichiaratore di puntatore utilizzato in C; viene costruita dall' \* indicatore, i modificatori, ad esempio **lontano**, e il qualificatore [**\[ const \]**](const.md).

</dd> <dt>

*Nome funzione* 
</dt> <dd>

Specifica il nome della procedura remota.

</dd> <dt>

*Parameter-Attribute-List* 
</dt> <dd>

Specifica zero o più attributi appropriati per il tipo di parametro. Gli attributi dei parametri con l'attributo in possono anche assumere l' [**\[ attributo \] Directional; gli**](out-idl.md)attributi [**\[ \] di**](in.md) campo [**\[ First \_ \] sono**](first-is.md), [**\[ Last \_ is \]**](last-is.md), [**\[ length \_ is \]**](length-is.md), [**\[ Max \_ is \]**](max-is.md), [**\[ size \_ is \]**](size-is.md)e [**\[ Switch \_ Type \]**](switch-type.md); gli attributi Pointer [**\[ ref \]**](ref.md), [**\[ Unique \]**](unique.md)o [**\[ ptr \]**](ptr.md); e la [**\[ stringa \]**](string.md)e l' [**\[ \_ handle \] di contesto**](context-handle.md) degli attributi Usage. L'attributo Usage [**\[ Ignore \]**](ignore.md) non può essere utilizzato come attributo di parametro. Più attributi devono essere separati da virgole.

</dd> <dt>

*dichiaratore* 
</dt> <dd>

Specifica i dichiaratori C standard, ad esempio identificatori, dichiaratori di puntatore e dichiaratori di matrici. Per altre informazioni, vedere [matrici e Sized-Pointer attributi](array-and-sized-pointer-attributes.md), [**\[ \] matrici**](../rpc/arrays.md)e [matrici e puntatori](/windows/desktop/Rpc/arrays-and-pointers). Il dichiaratore di parametro nel dichiaratore di funzione, ad esempio il nome del parametro, è facoltativo.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'attributo **\[ annotate \]** consente di eseguire l'override delle annotazioni SAL generate da MIDL o di aggiungerle in posizioni in cui MIDL non genera in modo esplicito un'annotazione. Se [**/Sal**](-sal.md) non è specificato nella riga di comando, questo attributo viene ignorato.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> <dt>

[**/sal**](-sal.md)
</dt> <dt>

[**/SAL \_ locale**](-sal-local.md)
</dt> </dl>

 

 