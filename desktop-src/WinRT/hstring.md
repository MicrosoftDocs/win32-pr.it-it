---
description: Handle per una stringa Windows Runtime.
ms.assetid: 763ACE57-EFDD-482E-851E-668D7756C5DF
title: HSTRING (HSTRING. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76b9e73d7627a4bab8f02a95056e5b208569d922
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307081"
---
# <a name="hstring"></a>HSTRING

Handle per una stringa Windows Runtime.


```C++
typedef HSTRING__* HSTRING;
```



## <a name="remarks"></a>Commenti

Usare **HString** per rappresentare stringhe non modificabili nel Windows Runtime.

JavaScript e altri linguaggi, ad esempio C \# e Microsoft Visual Basic, possono usare stringhe rappresentate tramite **HString**. Nella tabella seguente viene illustrato il modo in cui un **HString** viene rappresentato in altre lingue.



| Linguaggio di programmazione                                                                    | Rappresentazione di stringa                                      |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------|
| [C++/WinRT](/windows/uwp/cpp-and-winrt-apis/intro-to-using-cpp-with-winrt)              | classe [WinRT:: HString](/uwp/cpp-ref-for-winrt/hstring)     |
| Estensioni del componente Visual C++ ([C++/CX](/cpp/cppcx/visual-c-language-reference-c-cx)) | Classe [Platform:: String](/cpp/cppcx/platform-string-class) |
| JavaScript                                                                              | String (oggetto)                                              |
| .NET Framework                                                                          | Classe System. String                                        |



 

L'handle **HString** è un tipo di handle standard. Semanticamente, un **HString** contenente il valore **null** rappresenta la stringa vuota, costituita da caratteri di contenuto zero e da un carattere **null** di terminazione. La creazione di una stringa tramite [**WindowsCreateString**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) con zero caratteri produrrà il valore dell'handle **null**. Quando si chiama [**WindowsGetStringRawBuffer**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer) con il valore **null**, viene restituito un puntatore a una stringa vuota seguita solo dal carattere di terminazione **NUL** . Non esiste alcun valore distinct per rappresentare un **HString** non inizializzato.

Chiamare la funzione [**WindowsCreateString**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) per creare un nuovo **HString** e chiamare la funzione [**WindowsDeleteString**](/windows/win32/api/winstring/nf-winstring-windowsdeletestring) per rilasciare il riferimento alla memoria della stringa di supporto. Chiamare la funzione [**WindowsCreateStringReference**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) per creare un riferimento a una stringa, anch ' esso denominato *stringa con passaggio rapido*.

Copiare un **HString** chiamando la funzione [**WindowsDuplicateString**](/windows/win32/api/winstring/nf-winstring-windowsduplicatestring) .

Concatenare due stringhe chiamando la funzione [**WindowsConcatString**](/windows/win32/api/winstring/nf-winstring-windowsconcatstring) .

Accedere alla memoria della stringa di supporto chiamando la funzione [**WindowsGetStringRawBuffer**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer) .

**HString** può archiviare e usare caratteri **NUL** incorporati. Utilizzare la funzione [**WindowsStringHasEmbeddedNull**](/windows/win32/api/winstring/nf-winstring-windowsstringhasembeddednull) per verificare la presenza di caratteri **NUL** incorporati prima di utilizzare qualsiasi funzione che può produrre risultati imprevisti. La maggior parte delle funzioni di Windows, ad esempio, utilizza **LPCWSTR** come parametro di input e calcola la lunghezza della stringa solo fino a quando non viene rilevato il primo **NUL** .

La stringa di supporto deve rimanere non modificabile e con terminazione null. Quando si chiama il codice crea un riferimento a una stringa tramite la funzione [**WindowsCreateStringReference**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) , la memoria contenente la rappresentazione di stringa di supporto è di proprietà del chiamante. Il Windows Runtime si basa sul contenuto della stringa originale per rimanere invariato. Quando si passa un riferimento a una stringa nel Windows Runtime, è responsabilità del chiamante assicurarsi che il contenuto della stringa sia invariato e **NUL** interrotto per la durata della chiamata. Il Windows Runtime rilascia tutti i riferimenti al riferimento alla stringa quando la chiamata restituisce.

Quando si riceve un **HString** come parametro out, è consigliabile impostare l'handle su **null** al termine dell'operazione.

Chiamare la funzione [**WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) per allocare un buffer di stringa modificabile che è possibile usare per creare un **HString** non modificabile. Una volta completato il popolamento del buffer, chiamare la funzione [**WindowsPromoteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) per creare il **HString**. Questo modello di costruzione a due fasi Abilita funzionalità simili a "generatore di stringhe".

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>HSTRING. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>


</dt> <dt>

[**WindowsCreateString**](/windows/win32/api/winstring/nf-winstring-windowscreatestring)
</dt> <dt>

[**WindowsDeleteString**](/windows/win32/api/winstring/nf-winstring-windowsdeletestring)
</dt> <dt>

[**WindowsDuplicateString**](/windows/win32/api/winstring/nf-winstring-windowsduplicatestring)
</dt> <dt>

[**WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer)
</dt> </dl>

 

 
