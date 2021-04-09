---
title: Risorsa un'STRINGTABLE
description: Definisce una o più risorse di stringa per un'applicazione. Le risorse di tipo stringa sono semplicemente stringhe Unicode o ASCII con terminazione null che possono essere caricate quando necessario dal file eseguibile, usando la funzione LoadString.
ms.assetid: 5868245d-3445-4792-86f5-253945310d36
keywords:
- Menu risorse un'STRINGTABLE e altre risorse
topic_type:
- apiref
api_name:
- STRINGTABLE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 271abd022bdedd3b27e0434e7364542fa51c8987
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104117738"
---
# <a name="stringtable-resource"></a>Risorsa un'STRINGTABLE

Definisce una o più risorse di stringa per un'applicazione. Le risorse di tipo stringa sono semplicemente stringhe Unicode o ASCII con terminazione null che possono essere caricate quando necessario dal file eseguibile, usando la funzione [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa) .

Esistono due modi per formattare un'istruzione **un'STRINGTABLE** :

``` syntax
STRINGTABLE  [optional-statements] {stringID string  ...}
```

\- - oppure -

``` syntax
STRINGTABLE
  [optional-statements]
BEGIN
stringID string
. . .
END
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*facoltativo-istruzioni*
</dt> <dd>

Questo parametro può essere costituito da zero o più delle istruzioni seguenti.



| Istruzione                                                        | Descrizione                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Caratteristiche**](characteristics-statement.md) *DWORD*     | Informazioni definite dall'utente su una risorsa che possono essere usate da strumenti per la lettura e la scrittura di file di risorse. Per ulteriori informazioni, vedere [**caratteristiche**](characteristics-statement.md). |
| [](language-statement.md) *Lingua* lingua, *lingua* | Specifica la lingua per la risorsa. Per ulteriori informazioni, vedere [**Language**](language-statement.md).                                                                              |
| [](version-statement.md) *DWORD* versione                     | Numero di versione definito dall'utente per la risorsa che può essere usato da strumenti che leggono e scrivono file di risorse. Per ulteriori informazioni, vedere [**Version**](version-statement.md).              |



 

</dd> <dt>

<span id="stringID"></span><span id="stringid"></span><span id="STRINGID"></span>*stringID*
</dt> <dd>

Intero senza segno a 16 bit che identifica la risorsa.

</dd> <dt>

<span id="string"></span><span id="STRING"></span>*stringa*
</dt> <dd>

Una o più stringhe, racchiuse tra virgolette. La stringa non deve contenere più di 4097 caratteri e deve occupare una sola riga nel file di origine. Per aggiungere un ritorno a capo alla stringa, usare questa sequenza di caratteri: \\ 012. Ad esempio, "Line One \\ 012Line Two" definisce una stringa che viene visualizzata come segue:

``` syntax
Line one
Line two
```

Per incorporare le virgolette nella stringa, usare la sequenza seguente: "". Ad esempio, "" "riga tre" "" definisce una stringa che viene visualizzata come segue:

``` syntax
"Line three"
```

Per codificare i caratteri Unicode, usare "L" seguito dai caratteri Unicode racchiusi tra virgolette. Per un esempio, vedere la sezione esempi.

Il compilatore di risorse supporta inoltre le continuazioni di riga nella *stringa*. Per un esempio, vedere la sezione esempi.

</dd> </dl>

Alcuni attributi sono supportati anche per la compatibilità con le versioni precedenti. Per altre informazioni, vedere [attributi di risorse comuni](common-resource-attributes.md).

## <a name="remarks"></a>Commenti

RC alloca 16 stringhe per sezione e usa il valore Identifier per determinare quale sezione deve contenere la stringa. Le stringhe i cui identificatori differiscono solo nei 4 bit inferiori vengono inserite nella stessa sezione. Per ulteriori informazioni, vedere [Q196774](https://support.microsoft.com/kb/196774).

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato l'uso dell'istruzione **un'STRINGTABLE** per visualizzare le stringhe ASCII:

``` syntax
#define IDS_HELLO    1
#define IDS_GOODBYE  2

STRINGTABLE
{
    IDS_HELLO,   "Hello"
    IDS_GOODBYE, "Goodbye"
} 
```

Nell'esempio seguente viene illustrato come codificare i caratteri Unicode:

``` syntax
STRINGTABLE
BEGINIDS_CHINESESTRING L"\x5e2e\x52a9"
IDS_RUSSIANSTRING L"\x0421\x043f\x0440\x0430\x0432\x043a\x0430"
IDS_ARABICSTRING L"\x062a\x0639\x0644\x064a\x0645\x0627\x062a"
END
```

Nell'esempio seguente vengono illustrate le stringhe con ASCII e Unicode. Si noti che le stringhe senza "L" iniziale utilizzano il formato di escape a 2 cifre:

``` syntax
STRINGTABLE
BEGIN
IDS_1 L"5\x00BC-Inch Floppy Disk"
IDS_1a "5\xBC-Inch Floppy Disk"
IDS_2 L"Don't confuse \x2229 (intersection) with \x222A (union)"
IDS_3 "Copyright \xA92001"
IDS_3a L"Copyright \x00a92001"
END
```

Nell'esempio seguente viene illustrato come è possibile utilizzare le continuazioni di riga:

``` syntax
STRINGTABLE
BEGIN
IDS_VERYLONGSTRING "blah blah blah blah blah blah \
blah blah blah blah blah blah \
blah blah blah blah blah blah \
blah blah blah blah blah blah"
END
```

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa)
</dt> <dt>

[**ACCELERATORI**](accelerators-resource.md)
</dt> <dt>

[**CARATTERISTICHE**](characteristics-statement.md)
</dt> <dt>

[**LINGUAGGIO**](language-statement.md)
</dt> <dt>

[**MENU**](menu-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**Versione**](version-statement.md)
</dt> </dl>

 

 