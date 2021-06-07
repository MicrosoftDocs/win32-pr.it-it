---
title: Attributo const
description: La parola chiave const modifica il tipo di una dichiarazione di tipo o il tipo di un parametro di funzione, impedendo la variazione del valore.
ms.assetid: 398fab76-93f3-4d5a-9223-1c57c612b2d7
keywords:
- Attributo const MIDL
topic_type:
- apiref
api_name:
- const
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7095e29daf18dc111caf37038b06b0beff5245a8
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387060"
---
# <a name="const-attribute"></a>Attributo const

La **parola chiave const** modifica il tipo di una dichiarazione di tipo o il tipo di un parametro di funzione, impedendo la variazione del valore.

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

*const-type* 
</dt> <dd>

Specifica un tipo MIDL intero, carattere, stringa o booleano valido. I tipi MIDL validi includono [**small**](small.md), [**short**](short.md), [**long**](long.md), [**char**](char-idl.md), **\* charÂ* _, _ [*wchar \_ t* *](wchar-t.md), **wchar \_ \* tÂ*_, _ [*byte* *](byte.md), **byteÂ \** _, e [_*voidÂ \**_](void.md). I tipi integer e carattere possono [essere _ *signed* *](signed.md) o [**unsigned.**](unsigned.md)

</dd> <dt>

*identifier* 
</dt> <dd>

Specifica un identificatore MIDL valido. Gli identificatori MIDL validi sono costituiti da un massimo di 31 caratteri alfanumerici e/o caratteri di sottolineatura e devono iniziare con un carattere alfabetico o di sottolineatura.

</dd> <dt>

*const-expression* 
</dt> <dd>

Specifica un'espressione, un identificatore o una costante numerica o carattere appropriata per il tipo specificato: valori letterali integer costanti o espressioni integer costanti per costanti Integer; Espressioni booleane che possono essere calcolate in fase di compilazione per [**i tipi booleani;**](boolean.md) costanti a carattere singolo per i [**tipi char;**](char-idl.md) e costanti stringa per i **\[** [**tipi**](string.md) **\]** stringa. [ * *VoidÂ \** _](void.md) type può essere inizializzato solo su _*NULL**.

</dd> <dt>

*type-attribute-list* 
</dt> <dd>

Specifica uno o più attributi che si applicano al tipo.

</dd> <dt>

*tipo di puntatore* 
</dt> <dd>

Specifica un tipo di puntatore MIDL valido.

</dd> <dt>

*declarator e declarator-list* 
</dt> <dd>

Specifica dichiaratori C standard, ad esempio identificatori, dichiaratori di puntatore e dichiaratori di matrice. Per altre informazioni, vedere [Matrici e Sized-Pointer,](array-and-sized-pointer-attributes.md) [**matrici**](arrays-1.md)e [matrici e puntatori.](/windows/desktop/Rpc/arrays-and-pointers) *Declarator-list* è costituito da uno o più dichiaratori, separati da virgole. L'identificatore del nome del parametro nel dichiaratore di funzione è facoltativo.

</dd> <dt>

*function-attr-list* 
</dt> <dd>

Specifica zero o più attributi che si applicano alla funzione. Gli attributi di funzione validi sono callback , local ; l'attributo puntatore ref , unique o ptr e la stringa degli attributi di utilizzo **\[** [](callback.md) **\]** **\[** [](local.md) **\]** **\[** [](ref.md) **\]** **\[** [](unique.md) **\]** **\[** [](ptr.md) **\]** , **\[** [](string.md) **\]** **\[** [**ignorano**](ignore.md) **\]** e **\[** [**gestiscono il \_ contesto**](context-handle.md) **\]** .

</dd> <dt>

*type-specifier* 
</dt> <dd>

Specifica un tipo [di \_ base,](midl-base-types.md) [**uno struct,**](struct.md) [**un'unione,**](union.md) [**un tipo enum**](enum.md) o un identificatore di tipo. Una specifica di archiviazione facoltativa può precedere *type-specifier*.

</dd> <dt>

*ptr-decl* 
</dt> <dd>

Specifica zero o più dichiaratori di puntatore. Un dichiaratore di puntatore è uguale al dichiaratore di puntatore usato in C. Viene costruito **\* *dall'designatore _ ,*** dai modificatori come _ far e dal qualificatore **const**.

</dd> <dt>

*function-name* 
</dt> <dd>

Specifica il nome della procedura remota.

</dd> <dt>

*parameter-attribute-list* 
</dt> <dd>

Specifica zero o più attributi direzionali, attributi di campo, attributi di utilizzo e attributi del puntatore appropriati per il tipo di parametro specificato. Separare più attributi con virgole.

</dd> </dl>

## <a name="remarks"></a>Commenti

MIDL consente di dichiarare i tipi costanti integer, carattere, stringa e booleano nel corpo dell'interfaccia del file IDL. Le dichiarazioni di tipo **const** vengono riprodotte nel file di intestazione generato come **\# direttive** define.

I compilatori IDL DCE non supportano le espressioni costanti. Pertanto, questa funzionalità non è disponibile quando si usa l'opzione [**/osf del compilatore**](-osf.md) MIDL.

Una costante definita in precedenza può essere usata come valore assegnato di una costante successiva. Il valore di un'espressione integrale costante viene convertito automaticamente nel rispettivo tipo Integer in base alle regole di conversione C.

Il valore di una costante carattere deve essere un carattere ASCII tra virgolette singole. Quando la costante carattere è il carattere virgoletta singola ('), il carattere barra rovesciata ( ) deve precedere il carattere virgolette \\ singole, come in \\ '.

Il valore di una costante stringa di caratteri deve essere una stringa tra virgolette doppie. All'interno di una stringa, il carattere barra rovesciata ( ) deve precedere un carattere letterale virgolette doppie **\\** ( **"** ), come in **\\ "**. All'interno di una stringa, il carattere barra rovesciata ( **\\** ) rappresenta un carattere di escape. Le costanti stringa possono essere costituite da un massimo di 255 caratteri.

Il valore **NULL** è l'unico valore valido per le costanti di [ * *tipo voidÂ \** _](void.md). Tutti gli attributi associati alla dichiarazione _ *const** vengono ignorati.

Il compilatore MIDL non verifica la presenza di errori di intervallo **nell'inizializzazione const.** Ad esempio, quando si specifica "const short x = 0xFFFFFFFF;" il compilatore MIDL non segnala un errore e l'inizializzatore viene riprodotto nel file di intestazione generato.

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

[**Matrici**](arrays-1.md)
</dt> <dt>

[Tipi di base MIDL](midl-base-types.md)
</dt> <dt>

[**Boolean**](boolean.md)
</dt> <dt>

[**byte**](byte.md)
</dt> <dt>

[**callback**](callback.md)
</dt> <dt>

[**Char**](char-idl.md)
</dt> <dt>

[**handle di \_ contesto**](context-handle.md)
</dt> <dt>

[**Enum**](enum.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Ignorare**](ignore.md)
</dt> <dt>

[**Locale**](local.md)
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

[**Firmato**](signed.md)
</dt> <dt>

[**Piccolo**](small.md)
</dt> <dt>

[**Stringa**](string.md)
</dt> <dt>

[**Struct**](struct.md)
</dt> <dt>

[**Unione**](union.md)
</dt> <dt>

[**Unico**](unique.md)
</dt> <dt>

[**Unsigned**](unsigned.md)
</dt> <dt>

[**void**](void.md)
</dt> <dt>

[**wchar \_ t**](wchar-t.md)
</dt> </dl>

 

 