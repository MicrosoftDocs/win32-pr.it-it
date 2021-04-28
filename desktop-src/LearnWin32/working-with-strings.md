---
title: Uso delle stringhe
description: Uso delle stringhe
ms.assetid: 876ff8bb-67c3-4dcc-aa94-7fbd915c67dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4661c6b07a267d90e0fca05d04354c018be04527
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110969"
---
# <a name="working-with-strings"></a>Uso delle stringhe

Windows supporta in modo nativo stringhe Unicode per elementi dell'interfaccia utente, nomi di file e così via. Unicode è la codifica dei caratteri preferita, perché supporta tutti i set di caratteri e le lingue. Windows rappresenta i caratteri Unicode usando la codifica UTF-16, in cui ogni carattere viene codificato come valore a 16 bit. I caratteri UTF-16 sono detti *caratteri wide,* per distinguerli dai caratteri ANSI a 8 bit. Il Visual C++ supporta il tipo di dati **predefinito wchar \_ t** per i caratteri wide. Il file di intestazione WinNT.h definisce anche il **typedef seguente.**


```C++
typedef wchar_t WCHAR;
```



Entrambe le versioni saranno disponibili nel codice di esempio MSDN. Per dichiarare un valore letterale carattere wide o un valore letterale stringa di caratteri wide, inserire **L** prima del valore letterale.


```C++
wchar_t a = L'a';
wchar_t *str = L"hello";
```



Di seguito sono riportati altri typedef correlati alle stringhe che verranno visualizzati:



| Typedef                   | Definizione       |
|---------------------------|------------------|
| **CHAR**                  | `char`           |
| **PSTR** o **LPSTR**     | `char*`          |
| **PCSTR** o **LPCSTR**   | `const char*`    |
| **PWSTR** o **LPWSTR**   | `wchar_t*`       |
| **PCWSTR** o **LPCWSTR** | `const wchar_t*` |



 

## <a name="unicode-and-ansi-functions"></a>Funzioni Unicode e ANSI

Quando Microsoft ha introdotto il supporto Unicode per Windows, ha semplificato la transizione fornendo due set paralleli di API, uno per le stringhe ANSI e l'altro per le stringhe Unicode. Ad esempio, sono disponibili due funzioni per impostare il testo della barra del titolo di una finestra:

-   **SetWindowTextA accetta** una stringa ANSI.
-   **SetWindowTextW** accetta una stringa Unicode.

Internamente, la versione ANSI converte la stringa in Unicode. Le intestazioni di Windows definiscono anche una macro che viene risolta nella versione Unicode quando viene definito il simbolo del preprocessore o la `UNICODE` versione ANSI in caso contrario.


```C++
#ifdef UNICODE
#define SetWindowText  SetWindowTextW
#else
#define SetWindowText  SetWindowTextA
#endif 
```



In MSDN la funzione è documentata con il nome [**SetWindowText,**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta)anche se è effettivamente il nome della macro, non il nome effettivo della funzione.

Le nuove applicazioni devono sempre chiamare le versioni Unicode. Molte lingue del mondo richiedono Unicode. Se si usano stringhe ANSI, non sarà possibile localizzare l'applicazione. Anche le versioni ANSI sono meno efficienti, perché il sistema operativo deve convertire le stringhe ANSI in Unicode in fase di esecuzione. A seconda delle preferenze, è possibile chiamare le funzioni Unicode in modo esplicito, ad esempio **SetWindowTextW,** o usare le macro. Il codice di esempio in MSDN chiama in genere le macro, ma i due moduli sono esattamente equivalenti. La maggior parte delle API più nuove in Windows ha solo una versione Unicode, senza una versione ANSI corrispondente.

## <a name="tchars"></a>TCHAR

Quando le applicazioni dovevano supportare sia Windows NT che Windows 95, Windows 98 e Windows Me, era utile compilare lo stesso codice per stringhe ANSI o Unicode, a seconda della piattaforma di destinazione. A questo scopo, il Windows SDK macro che eseere il mapping delle stringhe a Unicode o ANSI, a seconda della piattaforma.



| Macro     | Unicode   | ANSI   |
|-----------|-----------|--------|
| TCHAR     | `wchar_t` | `char` |
| TEXT("x") | `L"x"`    | `"x"`  |



 

Ad esempio, il seguente codice:


```C++
SetWindowText(TEXT("My Application"));
```



viene risolto in uno degli elementi seguenti:


```C++
SetWindowTextW(L"My Application"); // Unicode function with wide-character string.

SetWindowTextA("My Application");  // ANSI function.
```



Le **macro TEXT** e **TCHAR** sono attualmente meno utili, perché tutte le applicazioni devono usare Unicode. Tuttavia, potrebbero essere visualizzati nel codice precedente e in alcuni esempi di codice MSDN.

Le intestazioni per le librerie di runtime di Microsoft C definiscono un set simile di macro. Ad esempio, **\_ tcslen** viene risolto in **strlen** se non è definito; in caso contrario, viene risolto in wcslen , che è la versione a caratteri wide `_UNICODE` di **strlen**. 


```C++
#ifdef _UNICODE
#define _tcslen     wcslen
#else
#define _tcslen     strlen
#endif 
```



Prestare attenzione: alcune intestazioni usano il simbolo del preprocessore `UNICODE` , altre usano con un prefisso di `_UNICODE` sottolineatura. Definire sempre entrambi i simboli. Visual C++ vengono impostate entrambe per impostazione predefinita quando si crea un nuovo progetto.

## <a name="next"></a>Prossima

[Che cos'è una finestra?](what-is-a-window-.md)

 

 
