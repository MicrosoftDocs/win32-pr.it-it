---
description: Handle per una stringa Windows runtime.
ms.assetid: 763ACE57-EFDD-482E-851E-668D7756C5DF
title: HSTRING (Hstring.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4b43c92d439cec10c0d1683efb1e8ceafd8165a35c3c8aa9a1b35150e43a33a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121571"
---
# <a name="hstring"></a>HSTRING

Handle per una stringa Windows runtime.


```C++
typedef HSTRING__* HSTRING;
```



## <a name="remarks"></a>Commenti

Usare **HSTRING** per rappresentare stringhe non modificabili in Windows Runtime.

JavaScript e altri linguaggi, ad esempio C e Microsoft Visual Basic, possono usare stringhe rappresentate \# tramite **HSTRING.** Nella tabella seguente viene illustrato come **viene rappresentato un HSTRING** in altri linguaggi.



| Linguaggio di programmazione                                                                    | Rappresentazione di stringa                                      |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------|
| [C++/WinRT](/windows/uwp/cpp-and-winrt-apis/intro-to-using-cpp-with-winrt)              | [Classe winrt::hstring](/uwp/cpp-ref-for-winrt/hstring)     |
| Visual C++ estensioni del componente ([C++/CX](/cpp/cppcx/visual-c-language-reference-c-cx)) | [Classe Platform::String](/cpp/cppcx/platform-string-class) |
| JavaScript                                                                              | String (oggetto)                                              |
| .NET Framework                                                                          | Classe System.String                                        |



 

**L'handle HSTRING** è un tipo di handle standard. Dal punto di vista **semantico, un valore HSTRING** contenente il valore **NULL** rappresenta la stringa vuota, costituita da zero caratteri di contenuto e da un carattere **NULL di** terminazione. La creazione di una stringa [**tramite WindowsCreateString**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) con zero caratteri produrrà il valore dell'handle **NULL.** Quando si [**chiama WindowsGetStringRawBuffer**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer) con il valore **NULL,** viene restituito un puntatore a una stringa vuota seguita solo dal carattere di terminazione **NUL.** Non esiste alcun valore distinct per rappresentare **un HSTRING** non inizializzato.

Chiamare la [**funzione WindowsCreateString**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) per creare un nuovo **HSTRING** e chiamare la funzione [**WindowsDeleteString**](/windows/win32/api/winstring/nf-winstring-windowsdeletestring) per rilasciare il riferimento alla memoria della stringa di supporto. Chiamare la [**funzione WindowsCreateStringReference**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) per creare un riferimento a una stringa, detta anche stringa a *passaggio rapido.*

Copiare **un oggetto HSTRING** chiamando la [**funzione WindowsDuplicateString.**](/windows/win32/api/winstring/nf-winstring-windowsduplicatestring)

Concatenare due stringhe chiamando la [**funzione WindowsConcatString.**](/windows/win32/api/winstring/nf-winstring-windowsconcatstring)

Accedere alla memoria della stringa di supporto chiamando la [**funzione WindowsGetStringRawBuffer.**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer)

**HSTRING può** archiviare e usare caratteri **NUL** incorporati. Usare la [**funzione WindowsStringHasEmbeddedNull**](/windows/win32/api/winstring/nf-winstring-windowsstringhasembeddednull) per verificare la presenza di caratteri **NUL** incorporati prima di usare funzioni che possono produrre risultati imprevisti. Ad esempio, la maggior parte delle funzioni Windows usa **LPCWSTR** come parametro di input e calcola la lunghezza della stringa solo fino a quando non viene rilevato il primo **valore NUL.**

La stringa di supporto deve rimanere non modificabile e con terminazione Null. Quando il codice chiamante crea un riferimento a una stringa usando la funzione [**WindowsCreateStringReference,**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) la memoria contenente la rappresentazione della stringa di supporto è di proprietà del chiamante. Il Windows runtime si basa sul contenuto della stringa originale per rimanere invariato. Quando si passa un riferimento a una stringa in Windows Runtime, è responsabilità del chiamante assicurarsi che il contenuto della stringa sia invaso e che **NUL** termini per la durata della chiamata. Il Windows runtime rilascia tutti i riferimenti al riferimento di stringa quando la chiamata viene restituita.

Quando si riceve **un valore HSTRING** come parametro out, è consigliabile impostare l'handle su **NULL** al termine dell'operazione.

Chiamare la [**funzione WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) per allocare un buffer di stringa modificabile che è possibile usare per creare un oggetto **HSTRING non modificabile.** Al termine del popolamento del buffer, chiamare la funzione [**WindowsPromoteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) per creare **HSTRING**. Questo modello di costruzione a due fasi abilita funzionalità simili a un "generatore di stringhe".

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>Hstring.h</dt> </dl> |



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

 

 
