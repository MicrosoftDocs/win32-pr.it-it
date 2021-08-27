---
title: WinMain The Application Entry Point description: WinMain: The Application Entry Point ms.assetid: 389da5d4-d0f9-4339-be6c-0f4fecc59316 ms.topic: article ms.date: 05/31/2018
---

# <a name="winmain-the-application-entry-point"></a>WinMain: punto di ingresso dell'applicazione

Ogni Windows include una funzione del punto di ingresso denominata **WinMain** o **wWinMain**. Ecco la firma per **wWinMain**.


```C++
int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, PWSTR pCmdLine, int nCmdShow);
```



I quattro parametri sono:

-   *hInstance* è un elemento denominato "handle a un'istanza" o "handle per un modulo". Il sistema operativo usa questo valore per identificare il file eseguibile (EXE) quando viene caricato in memoria. L'handle di istanza è necessario per determinate Windows, ad esempio per caricare icone o bitmap.
-   *hPrevInstance* non ha alcun significato. È stato usato in Windows a 16 bit, ma ora è sempre zero.
-   *pCmdLine contiene* gli argomenti della riga di comando come stringa Unicode.
-   *nCmdShow è* un flag che indica se la finestra principale dell'applicazione verrà ridotta a icona, ingrandita o visualizzata normalmente.

La funzione restituisce un **valore int.** Il valore restituito non viene usato dal sistema operativo, ma è possibile usare il valore restituito per trasmettere un codice di stato a un altro programma scritto.

**WINAPI è** la convenzione di chiamata. Una *convenzione di* chiamata definisce il modo in cui una funzione riceve i parametri dal chiamante. Ad esempio, definisce l'ordine in cui i parametri vengono visualizzati nello stack. Assicurarsi di dichiarare la funzione **wWinMain** come illustrato.

La **funzione WinMain** è identica a **wWinMain**, ad eccezione del fatto che gli argomenti della riga di comando vengono passati come stringa ANSI. È preferibile la versione Unicode. È possibile usare la funzione ANSI **WinMain** anche se si compila il programma come Unicode. Per ottenere una copia Unicode degli argomenti della riga di comando, chiamare la [**funzione GetCommandLine.**](/windows/desktop/api/processenv/nf-processenv-getcommandlinea) Questa funzione restituisce tutti gli argomenti in una singola stringa. Se si vogliono gli argomenti come matrice di tipo *argv,* passare questa stringa a [**CommandLineToArgvW**](/windows/desktop/api/shellapi/nf-shellapi-commandlinetoargvw).

Come fa il compilatore a richiamare **wWinMain** anziché la funzione **main** standard? Ciò che accade è che la libreria di runtime di Microsoft C (CRT) fornisce un'implementazione **di main** che chiama **WinMain** o **wWinMain**.

> [!Note]  
> CRT esegue alcune operazioni aggiuntive all'interno **di main**. Ad esempio, tutti gli inizializzatori statici vengono chiamati prima **di wWinMain**. Anche se è possibile indicare al linker di usare una funzione del punto di ingresso diversa, usare l'impostazione predefinita se ci si collega a CRT. In caso contrario, il codice di inizializzazione CRT verrà ignorato, con risultati imprevedibili. Ad esempio, gli oggetti globali non verranno inizializzati correttamente.

 

Ecco una funzione **WinMain** vuota.


```C++
INT WINAPI WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance,
    PSTR lpCmdLine, INT nCmdShow)
{
    return 0;
}
```



Dopo aver creato il punto di ingresso e aver compreso alcune delle convenzioni di terminologia e codifica di base, si è pronti per creare un programma Window completo.

## <a name="next"></a>Prossima

[Modulo 1. Il programma First Windows](your-first-windows-program.md).

 

 
