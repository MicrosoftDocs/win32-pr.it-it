---
title: WinMain il punto di ingresso dell'applicazione
description: .
ms.assetid: 389da5d4-d0f9-4339-be6c-0f4fecc59316
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bef44c4d31aa53dfd60f579b68c438a539058b85
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104223558"
---
# <a name="winmain-the-application-entry-point"></a>WinMain: punto di ingresso dell'applicazione

Ogni programma Windows include una funzione del punto di ingresso denominata **WinMain** o **wWinMain**. Di seguito è illustrata la firma di **wWinMain**.


```C++
int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, PWSTR pCmdLine, int nCmdShow);
```



I quattro parametri sono i seguenti:

-   *HINSTANCE* è un elemento denominato "handle per un'istanza" o "handle per un modulo". Il sistema operativo utilizza questo valore per identificare il file eseguibile (EXE) quando viene caricato in memoria. L'handle dell'istanza è necessario per determinate funzioni di Windows, ad esempio per caricare icone o bitmap.
-   *hPrevInstance* non ha alcun significato. È stata usata in Windows a 16 bit, ma ora è sempre zero.
-   *pCmdLine* contiene gli argomenti della riga di comando come stringa Unicode.
-   *nCmdShow* è un flag che indica se la finestra principale dell'applicazione verrà ridotta a icona, ingrandita o visualizzata normalmente.

La funzione restituisce un valore **int** . Il valore restituito non viene utilizzato dal sistema operativo, ma è possibile utilizzare il valore restituito per fornire un codice di stato a un altro programma che viene scritto.

**WINAPI** è la convenzione di chiamata. Una *convenzione di chiamata* definisce il modo in cui una funzione riceve parametri dal chiamante. Ad esempio, definisce l'ordine in cui i parametri vengono visualizzati nello stack. È sufficiente assicurarsi di dichiarare la funzione **wWinMain** come illustrato.

La funzione **WinMain** è identica a **wWinMain**, con la differenza che gli argomenti della riga di comando vengono passati come stringa ANSI. È preferibile la versione Unicode. È possibile usare la funzione ANSI **WinMain** anche se si compila il programma come Unicode. Per ottenere una copia Unicode degli argomenti della riga di comando, chiamare la funzione [**GetCommandLine**](/windows/desktop/api/processenv/nf-processenv-getcommandlinea) . Questa funzione restituisce tutti gli argomenti in una singola stringa. Se si desidera che gli argomenti siano una matrice di tipo *argv*, passare questa stringa a [**CommandLineToArgvW**](/windows/desktop/api/shellapi/nf-shellapi-commandlinetoargvw).

In che modo il compilatore sa richiamare **wWinMain** invece della funzione **Main** standard? In realtà, la libreria di runtime di Microsoft C (CRT) fornisce un'implementazione del **principale** che chiama **WinMain** o **wWinMain**.

> [!Note]  
> CRT esegue alcune operazioni aggiuntive all'interno di **Main**. Ad esempio, tutti gli inizializzatori statici vengono chiamati prima di **wWinMain**. Sebbene sia possibile indicare al linker di usare una funzione del punto di ingresso diversa, usare il valore predefinito se si collega a CRT. In caso contrario, il codice di inizializzazione CRT verrà ignorato, con risultati imprevedibili. Gli oggetti globali, ad esempio, non verranno inizializzati correttamente.

 

Ecco una funzione **WinMain** vuota.


```C++
INT WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance,
    PSTR lpCmdLine, INT nCmdShow)
{
    return 0;
}
```



Ora che si dispone di un punto di ingresso e si comprendono alcune delle convenzioni di codifica e terminologia di base, si è pronti per creare un programma Windows completo.

## <a name="next"></a>Prossima

[Modulo 1. Il primo programma Windows](your-first-windows-program.md).

 

 