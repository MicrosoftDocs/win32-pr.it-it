---
title: attributo const
description: La parola chiave const modifica il tipo di una dichiarazione di tipo o il tipo di un parametro di funzione, impedendo la variazione del valore.
ms.assetid: 398fab76-93f3-4d5a-9223-1c57c612b2d7
keywords:
- attributo const MIDL
topic_type:
- apiref
api_name:
- const
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d2980f0f484c838e4f972bbf12fb72173edb3e7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103724967"
---
# <a name="const-attribute"></a>attributo const

La parola chiave **const** modifica il tipo di una dichiarazione di tipo o il tipo di un parametro di funzione, impedendo la variazione del valore.

``` syntax
const const-type identifier = const-expression ;

[ typedef [ , type-attribute-list ] ] const const-type declarator-list;

[ typedef [ , type-attribute-list ] ] pointer-type const declarator-list;

[ [ function-attr-list ] ] type-specifier [ ptr-decl ] function-name(
    [ [ parameter-attribute-list ] ] ) const; 

const-type [declarator], [ [ parameter-attribute-list ] ] pointer-type const [declarator], ...);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*tipo const* 
</dt> <dd>

Specifica un Integer MIDL, un carattere, una stringa o un tipo booleano valido. I tipi MIDL validi [**includono Small**](small.md), [**short**](short.md), [**Long**](long.md), [**char**](char-idl.md), **\* charÂ**, [**WCHAR \_ t**](wchar-t.md), **WCHAR \_ tÂ \***, [**byte**](byte.md), **byteÂ \*** e [**voidÂ \***](void.md). I tipi integer e character possono essere [**firmati**](signed.md) o [**senza segno**](unsigned.md).

</dd> <dt>

*identifier* 
</dt> <dd>

Specifica un identificatore MIDL valido. Gli identificatori MIDL validi sono costituiti da un massimo di 31 caratteri alfanumerici e/o di sottolineatura e devono iniziare con un carattere alfabetico o di sottolineatura.

</dd> <dt>

*const-espressione* 
</dt> <dd>

Specifica un'espressione, un identificatore o una costante numerica o carattere appropriata per il tipo specificato: valori letterali integer costanti o espressioni integer costanti per le costanti Integer; Espressioni booleane che possono essere calcolate in fase di compilazione per i tipi [**booleani**](boolean.md) ; costanti a carattere singolo per i tipi [**char**](char-idl.md) ; e costanti di stringa per i tipi di **\[** [**stringa**](string.md) **\]** . Il [**tipo \* voidÂ**](void.md) può essere inizializzato solo su **null**.

</dd> <dt>

*tipo-Attribute-List* 
</dt> <dd>

Specifica uno o più attributi che si applicano al tipo.

</dd> <dt>

*tipo di puntatore* 
</dt> <dd>

Specifica un tipo di puntatore MIDL valido.

</dd> <dt>

*dichiaratore e declarator-list* 
</dt> <dd>

Specifica i dichiaratori C standard, ad esempio identificatori, dichiaratori di puntatore e dichiaratori di matrici. Per altre informazioni, vedere [matrici e Sized-Pointer attributi](array-and-sized-pointer-attributes.md), [**matrici**](arrays-1.md)e [matrici e puntatori](/windows/desktop/Rpc/arrays-and-pointers). Il *declarator-list* è costituito da uno o più dichiaratori, separati da virgole. L'identificatore di nome parametro nel dichiaratore di funzione è facoltativo.

</dd> <dt>

*Function-attr-List* 
</dt> <dd>

Specifica zero o più attributi che si applicano alla funzione. Gli attributi di funzione validi sono **\[** [**callback**](callback.md) **\]** , **\[** [**local**](local.md), **\]** l'attributo Pointer **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** e gli attributi Usage **\[** [**String**](string.md) **\]** , **\[** [**Ignore**](ignore.md) **\]** e **\[** [**Context \_ handle**](context-handle.md) **\]** .

</dd> <dt>

*identificatore di tipo* 
</dt> <dd>

Specifica un [ \_ tipo di base](midl-base-types.md), uno [**struct**](struct.md), un' [**unione**](union.md), un tipo [**enum**](enum.md) o un identificatore di tipo. Una specifica di archiviazione facoltativa può precedere *Type-specifier*.

</dd> <dt>

*PTR-decl* 
</dt> <dd>

Specifica zero o più dichiaratori di puntatore. Un dichiaratore di puntatore è uguale al dichiaratore del puntatore utilizzato in C. Viene costruita dall' **\*** indicatore, i modificatori, ad esempio **lontano**, e il qualificatore **const**.

</dd> <dt>

*Nome funzione* 
</dt> <dd>

Specifica il nome della procedura remota.

</dd> <dt>

*Parameter-Attribute-List* 
</dt> <dd>

Specifica zero o più attributi direzionali, attributi di campo, attributi di utilizzo e attributi del puntatore appropriati per il tipo di parametro specificato. Separare più attributi con virgole.

</dd> </dl>

## <a name="remarks"></a>Commenti

MIDL consente di dichiarare tipi integer costanti, caratteri, stringa e booleani nel corpo dell'interfaccia del file IDL. Le dichiarazioni di tipo **const** vengono riprodotte nel file di intestazione generato come direttive **\# define** .

I compilatori IDL DCE non supportano espressioni costanti. Questa funzionalità non è pertanto disponibile quando si usa l'opzione [**/OSF**](-osf.md) del compilatore MIDL.

Una costante definita in precedenza può essere usata come valore assegnato di una costante successiva. Il valore di un'espressione integrale costante viene convertito automaticamente nel rispettivo tipo integer in base alle regole di conversione C.

Il valore di una costante carattere deve essere un carattere ASCII racchiuso tra virgolette singole. Quando la costante carattere è il carattere con virgolette singole ('), il carattere barra rovesciata ( \) deve precedere il carattere con virgolette singole, come in \\ '.

Il valore di una costante stringa di caratteri deve essere una stringa racchiusa tra virgolette doppie. All'interno di una stringa, il carattere barra rovesciata ( **\\** ) deve precedere un carattere virgolette doppie ( **"** ), come in **\\ "**. All'interno di una stringa, il carattere barra rovesciata ( **\\** ) rappresenta un carattere di escape. Le costanti di stringa possono contenere fino a 255 caratteri.

Il valore **null** è l'unico valore valido per le costanti di tipo [**voidÂ \***](void.md). Qualsiasi attributo associato alla Dichiarazione **const** viene ignorato.

Il compilatore MIDL non controlla la presenza di errori di intervallo nell'inizializzazione **const** . Ad esempio, quando si specifica "const short x = 0xFFFFFFFF;", il compilatore MIDL non segnala un errore e l'inizializzatore viene riprodotto nel file di intestazione generato.

## <a name="examples"></a>Esempi

``` syntax
const void *  p1        = NULL; 
const char    my_char1  = 'a'; 
const char    my_char2  = my_char1; 
const wchar_t my_wchar3 = L'a'; 
const wchar_t * pszNote = L"Note"; 
const unsigned short int x = 123; 
 
typedef [string] const char *LPCSTR; 
 
HRESULT GetName([out] wchar_t * const pszName );
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**matrici**](arrays-1.md)
</dt> <dt>

[Tipi di base MIDL](midl-base-types.md)
</dt> <dt>

[**Boolean**](boolean.md)
</dt> <dt>

[**byte**](byte.md)
</dt> <dt>

[**callback**](callback.md)
</dt> <dt>

[**char**](char-idl.md)
</dt> <dt>

[**handle di contesto \_**](context-handle.md)
</dt> <dt>

[**enum**](enum.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**ignorare**](ignore.md)
</dt> <dt>

[**locale**](local.md)
</dt> <dt>

[**long**](long.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**con segno**](signed.md)
</dt> <dt>

[**piccolo**](small.md)
</dt> <dt>

[**string**](string.md)
</dt> <dt>

[**struct**](struct.md)
</dt> <dt>

[**Unione**](union.md)
</dt> <dt>

[**unico**](unique.md)
</dt> <dt>

[**unsigned**](unsigned.md)
</dt> <dt>

[**void**](void.md)
</dt> <dt>

[**WCHAR \_ t**](wchar-t.md)
</dt> </dl>

 

 