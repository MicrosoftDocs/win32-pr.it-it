---
title: Uso delle stringhe
description: .
ms.assetid: 876ff8bb-67c3-4dcc-aa94-7fbd915c67dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70c74530a1acd0eb94f0d88662924203a8c58116
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104117659"
---
# <a name="working-with-strings"></a>Uso delle stringhe

Windows supporta in modo nativo le stringhe Unicode per gli elementi dell'interfaccia utente, i nomi di file e così via. Unicode è la codifica dei caratteri preferita, perché supporta tutti i set di caratteri e le lingue. Windows rappresenta i caratteri Unicode usando la codifica UTF-16, in cui ogni carattere viene codificato come valore a 16 bit. I caratteri UTF-16 sono detti caratteri *Wide* per distinguerli da caratteri ANSI a 8 bit. Il compilatore Visual C++ supporta il tipo di dati predefinito **WCHAR \_ t** per i caratteri wide. Il file di intestazione WinNT. h definisce anche il **typedef** seguente.


```C++
typedef wchar_t WCHAR;
```



Vengono visualizzate entrambe le versioni nel codice di esempio MSDN. Per dichiarare un valore letterale a caratteri wide o un valore letterale stringa di caratteri wide, inserire **L** prima del valore letterale.


```C++
wchar_t a = L'a';
wchar_t *str = L"hello";
```



Di seguito sono riportati alcuni altri typedef correlati a stringhe che verranno visualizzati:



| Typedef                   | Definizione       |
|---------------------------|------------------|
| **CHAR**                  | `char`           |
| **Pstr** o **LPSTR**     | `char*`          |
| **PCSTR** o **LPCSTR**   | `const char*`    |
| **PWSTR** o **LPWSTR**   | `wchar_t*`       |
| **PCWSTR** o **LPCWSTR** | `const wchar_t*` |



 

## <a name="unicode-and-ansi-functions"></a>Funzioni Unicode e ANSI

Quando Microsoft ha introdotto il supporto Unicode per Windows, ha semplificato la transizione fornendo due set di API paralleli, uno per le stringhe ANSI e l'altro per le stringhe Unicode. Sono ad esempio disponibili due funzioni per impostare il testo della barra del titolo di una finestra:

-   **SetWindowTextA** accetta una stringa ANSI.
-   **SetWindowTextW** accetta una stringa Unicode.

Internamente, la versione ANSI converte la stringa in Unicode. Le intestazioni di Windows definiscono anche una macro che viene risolta nella versione Unicode quando viene definito il simbolo del preprocessore `UNICODE` o in caso contrario la versione ANSI.


```C++
#ifdef UNICODE
#define SetWindowText  SetWindowTextW
#else
#define SetWindowText  SetWindowTextA
#endif 
```



In MSDN, la funzione è documentata con il nome [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta), anche se è effettivamente il nome della macro, non il nome effettivo della funzione.

Le nuove applicazioni devono sempre chiamare le versioni Unicode. Molti linguaggi internazionali richiedono Unicode. Se si usano stringhe ANSI, sarà impossibile localizzare l'applicazione. Anche le versioni ANSI sono meno efficienti perché il sistema operativo deve convertire le stringhe ANSI in Unicode in fase di esecuzione. A seconda delle preferenze, è possibile chiamare le funzioni Unicode in modo esplicito, ad esempio **SetWindowTextW**, oppure utilizzare le macro. Il codice di esempio su MSDN chiama in genere le macro, ma le due forme sono esattamente equivalenti. Le API più recenti in Windows hanno solo una versione Unicode, senza alcuna versione ANSI corrispondente.

## <a name="tchars"></a>TCHARs

Quando le applicazioni sono necessarie per supportare sia Windows NT che Windows 95, Windows 98 e Windows me, è utile compilare lo stesso codice per le stringhe ANSI o Unicode, a seconda della piattaforma di destinazione. A questo scopo, il Windows SDK fornisce macro che mappano le stringhe a Unicode o ANSI, a seconda della piattaforma.



| Macro     | Unicode   | ANSI   |
|-----------|-----------|--------|
| TCHAR     | `wchar_t` | `char` |
| TESTO ("x") | `L"x"`    | `"x"`  |



 

Ad esempio, il seguente codice:


```C++
SetWindowText(TEXT("My Application"));
```



viene risolto in uno dei seguenti elementi:


```C++
SetWindowTextW(L"My Application"); // Unicode function with wide-character string.

SetWindowTextA("My Application");  // ANSI function.
```



Attualmente le macro **Text** e **TCHAR** sono meno utili, perché tutte le applicazioni devono utilizzare Unicode. Tuttavia, è possibile visualizzarli nel codice precedente e in alcuni degli esempi di codice MSDN.

Le intestazioni per le librerie di runtime di Microsoft C definiscono un set di macro simile. Ad esempio, **\_ tcslen** si risolve in **strlen** se `_UNICODE` non è definito; in caso contrario, viene risolto in **wcslen**, che è la versione a caratteri wide di **strlen**.


```C++
#ifdef _UNICODE
#define _tcslen     wcslen
#else
#define _tcslen     strlen
#endif 
```



Prestare attenzione: alcune intestazioni usano il simbolo del preprocessore `UNICODE` , altre usano `_UNICODE` con un prefisso di sottolineatura. Definire sempre entrambi i simboli. Per impostazione predefinita, Visual C++ li imposta entrambi quando si crea un nuovo progetto.

## <a name="next"></a>Prossima

[Che cos'è una finestra?](what-is-a-window-.md)

 

 