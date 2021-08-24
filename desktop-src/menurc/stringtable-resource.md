---
title: Risorsa STRINGTABLE
description: Definisce una o più risorse stringa per un'applicazione. Le risorse stringa sono semplicemente stringhe Unicode o ASCII con terminazione Null che possono essere caricate quando necessario dal file eseguibile, usando la funzione LoadString.
ms.assetid: 5868245d-3445-4792-86f5-253945310d36
keywords:
- Menu delle risorse STRINGTABLE e altre risorse
topic_type:
- apiref
api_name:
- STRINGTABLE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7994b6853195ba164c766ca6ee275e4535ab1249c0c78907ab996b9dc644013a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119720651"
---
# <a name="stringtable-resource"></a>Risorsa STRINGTABLE

Definisce una o più risorse stringa per un'applicazione. Le risorse stringa sono semplicemente stringhe Unicode o ASCII con terminazione Null che possono essere caricate quando necessario dal file eseguibile, usando la [**funzione LoadString.**](/windows/win32/api/winuser/nf-winuser-loadstringa)

Esistono due modi per formattare **un'istruzione STRINGTABLE:**

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

<span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*istruzioni facoltative*
</dt> <dd>

Questo parametro può essere zero o più delle istruzioni seguenti.



| Istruzione                                                        | Descrizione                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CHARACTERISTICS**](characteristics-statement.md) *dword*     | Informazioni definite dall'utente su una risorsa che possono essere usate dagli strumenti che leggono e scrivono file di risorse. Per altre informazioni, vedere [**CHARACTERISTICS**](characteristics-statement.md). |
| [**LANGUAGE**](language-statement.md) *language*, *sottolinguaggio* | Specifica la lingua per la risorsa. Per altre informazioni, vedere [**LANGUAGE**](language-statement.md).                                                                              |
| [**VERSION**](version-statement.md) *dword*                     | Numero di versione definito dall'utente per la risorsa che può essere usato dagli strumenti che leggono e scrivono file di risorse. Per altre informazioni, vedere [**VERSION**](version-statement.md).              |



 

</dd> <dt>

<span id="stringID"></span><span id="stringid"></span><span id="STRINGID"></span>*stringID*
</dt> <dd>

Intero senza segno a 16 bit che identifica la risorsa.

</dd> <dt>

<span id="string"></span><span id="STRING"></span>*Stringa*
</dt> <dd>

Una o più stringhe, racchiuse tra virgolette. La stringa non deve contenere più di 4097 caratteri e deve occupare una singola riga nel file di origine. Per aggiungere un ritorno a capo alla stringa, usare questa sequenza di caratteri: \\ 012. Ad esempio, "Riga \\ 1 012Line two" definisce una stringa che viene visualizzata come segue:

``` syntax
Line one
Line two
```

Per incorporare le virgolette nella stringa, usare la sequenza seguente: "". Ad esempio, """Riga tre"""" definisce una stringa che viene visualizzata come segue:

``` syntax
"Line three"
```

Per codificare i caratteri Unicode, usare una "L" seguita dai caratteri Unicode racchiusi tra virgolette. Per un esempio, vedere la sezione Esempi.

Il compilatore di risorse supporta anche le continuazioni di riga nella *stringa*. Per un esempio, vedere la sezione Esempi.

</dd> </dl>

Alcuni attributi sono supportati anche per la compatibilità con le versioni precedenti. Per altre informazioni, vedere [Attributi comuni delle risorse](common-resource-attributes.md).

## <a name="remarks"></a>Commenti

RC alloca 16 stringhe per ogni sezione e usa il valore dell'identificatore per determinare quale sezione deve contenere la stringa. Le stringhe i cui identificatori differiscono solo nei 4 bit più in basso vengono inserite nella stessa sezione. Per altre informazioni, vedere [Q196774](https://support.microsoft.com/kb/196774).

## <a name="examples"></a>Esempio

L'esempio seguente illustra l'uso **dell'istruzione STRINGTABLE** per visualizzare stringhe ASCII:

``` syntax
#define IDS_HELLO    1
#define IDS_GOODBYE  2

STRINGTABLE
{
    IDS_HELLO,   "Hello"
    IDS_GOODBYE, "Goodbye"
} 
```

L'esempio seguente illustra come codificare i caratteri Unicode:

``` syntax
STRINGTABLE
BEGINIDS_CHINESESTRING L"\x5e2e\x52a9"
IDS_RUSSIANSTRING L"\x0421\x043f\x0440\x0430\x0432\x043a\x0430"
IDS_ARABICSTRING L"\x062a\x0639\x0644\x064a\x0645\x0627\x062a"
END
```

L'esempio seguente illustra le stringhe con ASCII e Unicode. Si noti che le stringhe senza la "L" iniziale usano il formato di escape a 2 cifre:

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

L'esempio seguente illustra come è possibile usare le continuazioni di riga:

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

[**Acceleratori**](accelerators-resource.md)
</dt> <dt>

[**Caratteristiche**](characteristics-statement.md)
</dt> <dt>

[**Lingua**](language-statement.md)
</dt> <dt>

[**Menu**](menu-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**Versione**](version-statement.md)
</dt> </dl>

 

 