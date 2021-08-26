---
title: The AccChecker Console
description: AccChecker Console (AccCheckConsole.exe) è uno strumento da riga di comando per verificare l'implementazione dell'accessibilità dell'interfaccia utente dell'applicazione.
ms.assetid: 9E80BFDD-FB5D-45C5-BE69-7036AD29D863
keywords:
- AccChecker Console
- Strumento da riga di comando AccChecker
- riga di comando, AccChecker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 272447e2513f109206af6fedaaf6adffe665e8b8
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122887034"
---
# <a name="the-accchecker-console"></a>The AccChecker Console

AccChecker Console (AccCheckConsole.exe) è uno strumento da riga di comando per verificare l'implementazione dell'accessibilità dell'interfaccia utente dell'applicazione. La riga di comando accetta un'ampia gamma di input (ad esempio HWND, titolo della finestra e routine di verifica) e fornisce un codice di uscita corrispondente al numero di log degli errori.

-   [Sintassi della riga di comando](#command-line-syntax)
-   [Codici di errore della riga di comando](#command-line-error-codes)
-   [Esempi della riga di comando](#command-line-examples)
-   [Argomenti correlati](#related-topics)

![Strumento da riga di comando della console accchecker](images/accchecker-console.png)

## <a name="command-line-syntax"></a>Sintassi della riga di comando

AccChecker Console ha la sintassi della riga di comando seguente.

**Opzioni accCheckConsole \[ \] (-hwnd &lt; hwnd &gt; \| -nome &lt; processo ) &gt; \[ &lt; DLL&gt;\]**

Le opzioni della riga di comando sono le seguenti.



| Opzioni                                                                                                                                                         | Descrizione                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span id="-hwnd__hwnd_"></span><span id="-HWND__HWND_"></span>-hwnd &lt; hwnd&gt;<br/>                                                                     | Convalida la finestra con l'handle (HWND) specificato. L'handle può essere specificato in formato esadecimale o decimale.<br/> |
| <span id="-window__title_"></span><span id="-WINDOW__TITLE_"></span>-window &lt; title&gt;<br/>                                                            | Convalida la finestra con il titolo specificato.<br/>                                                                |
| <span id="__________________-process__name_"></span><span id="__________________-PROCESS__NAME_"></span> -process &lt; name&gt;<br/>                       | Convalida la finestra principale del processo con il nome specificato.<br/>                                             |
| <span id="____________________________-list"></span><span id="____________________________-LIST"></span> -list<br/>                                       | Elenca tutte le routine di verifica disponibili.<br/>                                                                 |
| <span id="__________________-enable__name_"></span><span id="__________________-ENABLE__NAME_"></span> -enable &lt; name&gt;<br/>                          | Esegue la routine di verifica specificata. Questa opzione può essere specificata più volte.<br/>                             |
| <span id="_____________________________-disable__name_"></span><span id="_____________________________-DISABLE__NAME_"></span> -disable &lt; name&gt;<br/> | Esegue tutte le routine di verifica, ad esempio la routine di verifica specificata. Questa opzione può essere specificata più volte.<br/>                     |
| <span id="___________-log__info_warn_err_"></span><span id="___________-LOG__INFO_WARN_ERR_"></span> -log (info \| warn \| err)<br/>                          | Classificazione dell'evento più bassa che verrà registrata.<br/>                                                                      |
| <span id="__________________-logfile__file_"></span><span id="__________________-LOGFILE__FILE_"></span> -logfile &lt; file&gt;<br/>                       | Scrive l'output nel file di log specificato. Questa opzione può essere specificata più volte.<br/>                          |
| <span id="-suppress__file_"></span><span id="-SUPPRESS__FILE_"></span>-suppress &lt; file&gt;<br/>                                                         | Utilizzare il file XML specificato per eliminare gli errori. <br/>                                                                   |
| <span id="-quiet"></span><span id="-QUIET"></span>-quiet<br/>                                                                                             | Non scrivere l'output di registrazione in stdout.<br/>                                                                            |
| <span id="-help__________________________________"></span><span id="-HELP__________________________________"></span>-help <br/>                           | Visualizza la Guida rapida. <br/>                                                                                             |



 

## <a name="command-line-error-codes"></a>Codici di errore della riga di comando

Di seguito sono riportati i codici di errore restituiti da AccCheckConsole quando si usa "echo %errorlevel%"



| Codice di errore                       | Descrizione                                 |
|----------------------------------|---------------------------------------------|
| <span id="0"></span>0<br/> | Nessun errore e nessun avviso.<br/>       |
| <span id="1"></span>1<br/> | È stata richiesta l'istruzione usages. <br/> |
| <span id="2"></span>2<br/> | Errori e nessun avviso.<br/>          |
| <span id="3"></span>3<br/> | Errori e avvisi.<br/>             |
| <span id="4"></span>4<br/> | Avvisi ma nessun errore.<br/>          |
| <span id="5"></span>5<br/> | Riga di comando non valida. <br/>           |



 

## <a name="command-line-examples"></a>Esempi della riga di comando

Di seguito sono riportati alcuni esempi di riga di comando della console AccChecker.

-   Eseguire tutte le verifiche in una finestra con un nome specificato.

    **AccCheckConsole -window "Untitled - Blocco note"**

-   Eseguire un subset delle verifiche su un oggetto HWND, specificando un file di eliminazione.

    **AccCheckConsole -hwnd 0x00382f00 -enable CheckTabbing -enable CheckName -suppress suppress.xml**

-   Eseguire tutte le verifiche da una nuova DLL di verifica.

    **AccCheckConsole -window "Untitled - Blocco note" VerificationRoutine1.dll**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Verifica dell'accessibilità dell'interfaccia utente](ui-accessibility-checker.md)
</dt> </dl>

 

 





