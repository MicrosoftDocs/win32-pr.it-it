---
description: Un valore del registro di sistema può archiviare i dati in vari formati.
ms.assetid: 5fd828d6-4d62-4823-a2f1-15782b5cd28c
title: Tipi di valore del registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adc653e69c514bc77323704485e88f0a57eebaae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882345"
---
# <a name="registry-value-types"></a>Tipi di valore del registro di sistema

Un valore del registro di sistema può archiviare i dati in vari formati. Quando si archiviano dati sotto un valore del registro di sistema, ad esempio chiamando la funzione [**RegSetValueEx**](/windows/desktop/api/Winreg/nf-winreg-regsetvalueexa) , è possibile specificare uno dei valori seguenti per indicare il tipo di dati archiviati. Quando si recupera un valore del registro di sistema, le funzioni come [**RegQueryValueEx**](/windows/desktop/api/Winreg/nf-winreg-regqueryvalueexa) utilizzano questi valori per indicare il tipo di dati recuperati.

I tipi di valore del registro di sistema seguenti sono definiti in Winnt. h.



| Valore                                 | Tipo                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| REG \_ binario<br/>                | Dati binari in qualsiasi forma.<br/>                                                                                                                                                                                                                                                                                                                                                                                                     |
| REG \_ DWORD<br/>                 | Numero a 32 bit.<br/>                                                                                                                                                                                                                                                                                                                                                                                                             |
| \_ \_ Little Endian reg \_ DWORD<br/> | Numero a 32 bit in formato little-endian.<br/> Windows è progettato per l'esecuzione in architetture di computer little-endian. Questo valore viene pertanto definito come REG \_ DWORD nei file di intestazione di Windows.<br/>                                                                                                                                                                                                                          |
| REG \_ DWORD \_ Big \_ endian<br/>    | Un numero a 32 bit nel formato big-endian.<br/> Alcuni sistemi UNIX supportano le architetture big endian.<br/>                                                                                                                                                                                                                                                                                                                         |
| REG \_ Espandi \_ SZ<br/>            | Stringa con terminazione null che contiene riferimenti non espansi a variabili di ambiente (ad esempio, "% PATH%"). Si tratta di una stringa Unicode o ANSI, a seconda che si usino le funzioni Unicode o ANSI. Per espandere i riferimenti alle variabili di ambiente, usare la funzione [**ExpandEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-expandenvironmentstringsa) .<br/>                                                                                 |
| \_collegamento reg<br/>                  | Stringa Unicode con terminazione null che contiene il percorso di destinazione di un collegamento simbolico creato chiamando la funzione [**RegCreateKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeyexa) con il \_ collegamento reg option \_ Create \_ .<br/>                                                                                                                                                                                                                          |
| REG \_ - \_ SZ<br/>             | Sequenza di stringhe con terminazione null, terminata da una stringa vuota ( \\ 0).<br/> Di seguito è riportato un esempio:<br/> *String1* \\ 0 *string2* \\ 0 *string3* \\ 0 *LastString* \\ 0 \\ 0<br/> Il primo \\ 0 termina la prima stringa, il secondo all'ultimo \\ 0 termina l'ultima stringa e l'ultimo \\ 0 termina la sequenza. Si noti che è necessario fattorizzare il terminatore finale nella lunghezza della stringa.<br/> |
| REG \_ None<br/>                  | Nessun tipo di valore definito.<br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| REG \_ QWORD<br/>                 | Numero a 64 bit.<br/>                                                                                                                                                                                                                                                                                                                                                                                                             |
| REG \_ QWORD \_ Little \_ endian<br/> | Numero a 64 bit in formato little-endian.<br/> Windows è progettato per l'esecuzione in architetture di computer little-endian. Questo valore viene pertanto definito come REG \_ QWORD nei file di intestazione di Windows.<br/>                                                                                                                                                                                                                          |
| REG \_ SZ<br/>                    | Specifica una stringa che termina con Null. Si tratta di una stringa Unicode o ANSI, a seconda che si utilizzino le funzioni Unicode o ANSI.<br/>                                                                                                                                                                                                                                                                                       |



 

## <a name="string-values"></a>Valori stringa

Se i dati includono il \_ tipo reg SZ, reg \_ \_ multisz o reg \_ expand \_ SZ, è possibile che la stringa non sia stata archiviata con i caratteri null di terminazione appropriati. Pertanto, durante la lettura di una stringa dal registro di sistema, è necessario verificare che la stringa sia terminata correttamente prima di utilizzarla. in caso contrario, potrebbe sovrascrivere un buffer. (Si noti che REG \_ Le \_ stringhe a più SZ devono avere due caratteri di terminazione null.

Quando si scrive una stringa nel registro di sistema, è necessario specificare la lunghezza della stringa, incluso il carattere null di terminazione ( \\ 0). Un errore comune consiste nell'usare la funzione **strlen** per determinare la lunghezza della stringa, ma per dimenticare che **strlen** restituisce solo il numero di caratteri nella stringa, escluso il carattere null di terminazione. La lunghezza della stringa deve pertanto essere calcolata nel modo seguente: `strlen( string ) + 1`

Una \_ stringa reg \_ multisz termina con una stringa di lunghezza 0. Non è quindi possibile includere nella sequenza una stringa di lunghezza zero. Una sequenza vuota verrebbe definita come segue: \\ 0.

Nell'esempio seguente viene illustrata \_ una \_ stringa reg multisz.


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>

void SampleSzz(PTSTR pszz)
{
   _tprintf(_TEXT("\tBegin multi-sz string\n"));
   while (*pszz) 
   {
      _tprintf(_TEXT("\t\t%s\n"), pszz);
      pszz = pszz + _tcslen(pszz) + 1;
   }
   _tprintf(_TEXT("\tEnd multi-sz\n"));
}

int __cdecl main(int argc, char **argv)
{
   // Because the compiler adds a \0 at the end of quoted strings, 
   // there are two \0 terminators at the end. 

   _tprintf(_TEXT("Conventional multi-sz string:\n"));  
   SampleSzz(_TEXT("String1\0String2\0String3\0LastString\0"));

   _tprintf(_TEXT("\nTest case with no strings:\n"));  
   SampleSzz(_TEXT(""));

   return 0;
}
```



## <a name="byte-formats"></a>Formati di byte

In *formato little-endian*, un valore a più byte viene archiviato in memoria dal byte più basso, ovvero "estremità minima", al byte più alto. Il valore 0x12345678., ad esempio, viene archiviato come (0x78 0x56 0x34 0x12) in formato little-endian.

Nel *formato big-endian*, un valore a più byte viene archiviato in memoria dal byte più alto ("Big end") al byte più basso. Il valore 0x12345678., ad esempio, viene archiviato come (0x12 0x34 0x56 0x78) nel formato big-endian.

 

