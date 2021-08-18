---
description: Un valore del Registro di sistema può archiviare i dati in vari formati.
ms.assetid: 5fd828d6-4d62-4823-a2f1-15782b5cd28c
title: Tipi di valori del Registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed2bc73e03d9aab8d39bdda31ab308af1749f22315a262ceb4ae28ec743c8c69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885014"
---
# <a name="registry-value-types"></a>Tipi di valori del Registro di sistema

Un valore del Registro di sistema può archiviare i dati in vari formati. Quando si archiviano dati in un valore del Registro di sistema, ad esempio chiamando la funzione [**RegSetValueEx,**](/windows/desktop/api/Winreg/nf-winreg-regsetvalueexa) è possibile specificare uno dei valori seguenti per indicare il tipo di dati archiviati. Quando si recupera un valore del Registro di sistema, funzioni come [**RegQueryValueEx**](/windows/desktop/api/Winreg/nf-winreg-regqueryvalueexa) usano questi valori per indicare il tipo di dati recuperati.

In Winnt.h sono definiti i tipi di valore del Registro di sistema seguenti.



| Valore                                 | Tipo                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| REG \_ BINARY<br/>                | Dati binari in qualsiasi forma.<br/>                                                                                                                                                                                                                                                                                                                                                                                                     |
| REG \_ DWORD<br/>                 | Numero a 32 bit.<br/>                                                                                                                                                                                                                                                                                                                                                                                                             |
| REG \_ DWORD \_ LITTLE \_ ENDIAN<br/> | Numero a 32 bit in formato little-endian.<br/> Windows è progettato per l'esecuzione in architetture di computer little endian. Pertanto, questo valore è definito come REG DWORD nei \_ file di intestazione Windows file di intestazione.<br/>                                                                                                                                                                                                                          |
| REG \_ DWORD \_ BIG \_ ENDIAN<br/>    | Numero a 32 bit in formato big endian.<br/> Alcuni UNIX supportano architetture big endian.<br/>                                                                                                                                                                                                                                                                                                                         |
| REG \_ EXPAND \_ SZ<br/>            | Stringa con terminazione Null che contiene riferimenti non esplorati a variabili di ambiente, ad esempio "%PATH%". Sarà una stringa Unicode o ANSI a seconda che si usino le funzioni Unicode o ANSI. Per espandere i riferimenti alle variabili di ambiente, usare [**la funzione ExpandEnvironmentStrings.**](/windows/win32/api/processenv/nf-processenv-expandenvironmentstringsa)<br/>                                                                                 |
| COLLEGAMENTO \_ REG<br/>                  | Stringa Unicode con terminazione Null che contiene il percorso di destinazione di un collegamento simbolico creato chiamando la funzione [**RegCreateKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeyexa) con REG \_ OPTION CREATE \_ \_ LINK.<br/>                                                                                                                                                                                                                          |
| REG \_ MULTI \_ SZ<br/>             | Sequenza di stringhe con terminazione Null, terminata da una stringa vuota \\ (0).<br/> Di seguito è riportato un esempio:<br/> *Stringa1* \\ 0 *String2* \\ 0 *String3* \\ 0 *LastString* \\ 0 \\ 0<br/> Il primo 0 termina la prima stringa, il secondo all'ultimo 0 termina l'ultima stringa e l'ultimo \\ \\ \\ 0 termina la sequenza. Si noti che il carattere di terminazione finale deve essere inserito nella lunghezza della stringa.<br/> |
| REG \_ NONE<br/>                  | Nessun tipo di valore definito.<br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| REG \_ QWORD<br/>                 | Numero a 64 bit.<br/>                                                                                                                                                                                                                                                                                                                                                                                                             |
| REG \_ QWORD \_ LITTLE \_ ENDIAN<br/> | Numero a 64 bit in formato little endian.<br/> Windows è progettato per l'esecuzione in architetture di computer little endian. Pertanto, questo valore è definito come QWORD REG nei \_ file Windows di intestazione.<br/>                                                                                                                                                                                                                          |
| REG \_ SZ<br/>                    | Specifica una stringa che termina con Null. Si tratta di una stringa Unicode o ANSI, a seconda che si usino le funzioni Unicode o ANSI.<br/>                                                                                                                                                                                                                                                                                       |



 

## <a name="string-values"></a>Valori stringa

Se i dati hanno il tipo REG SZ, REG MULTI SZ o REG EXPAND SZ, è possibile che la stringa non sia stata archiviata con i caratteri \_ \_ Null di \_ \_ \_ terminazione corretto. Pertanto, quando si legge una stringa dal Registro di sistema, è necessario assicurarsi che la stringa venga terminata correttamente prima di usarla. in caso contrario, potrebbe sovrascrivere un buffer. Si noti che REG \_ Le \_ stringhe MULTI SZ devono contenere due caratteri null di terminazione.

Quando si scrive una stringa nel Registro di sistema, è necessario specificare la lunghezza della stringa, incluso il carattere null di terminazione ( \\ 0). Un errore comune è l'uso della funzione **strlen** per determinare la lunghezza della stringa, ma è importante dimenticare che **strlen** restituisce solo il numero di caratteri nella stringa, senza includere il carattere Null di terminazione. Pertanto, la lunghezza della stringa deve essere calcolata come segue: `strlen( string ) + 1`

Una stringa REG \_ MULTI \_ SZ termina con una stringa di lunghezza 0. Pertanto, non è possibile includere una stringa di lunghezza zero nella sequenza. Una sequenza vuota viene definita come segue: \\ 0.

L'esempio seguente illustra una stringa REG \_ MULTI \_ SZ.


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

In *formato little-endian*, un valore multi-byte viene archiviato in memoria dal byte più basso (l'"estremità piccola") al byte più alto. Ad esempio, il valore 0x12345678 viene archiviato come (0x78 0x56 0x34 0x12) in formato little-endian.

In *formato big-endian,* un valore multi-byte viene archiviato in memoria dal byte più alto (big end) al byte più basso. Ad esempio, il valore 0x12345678 viene archiviato come (0x12 0x34 0x56 0x78) in formato big-endian.

 

