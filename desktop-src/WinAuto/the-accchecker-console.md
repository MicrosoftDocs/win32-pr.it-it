---
title: Console di AccChecker
description: AccChecker Console (AccCheckConsole.exe) è uno strumento da riga di comando per la verifica dell'implementazione dell'accessibilità dell'interfaccia utente dell'applicazione.
ms.assetid: 9E80BFDD-FB5D-45C5-BE69-7036AD29D863
keywords:
- Console AccChecker
- Strumento da riga di comando AccChecker
- riga di comando, AccChecker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34ef010b2079d364c43bf2a6e47b0e3b0f24bb37
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855557"
---
# <a name="the-accchecker-console"></a>Console di AccChecker

AccChecker Console (AccCheckConsole.exe) è uno strumento da riga di comando per la verifica dell'implementazione dell'accessibilità dell'interfaccia utente dell'applicazione. La riga di comando accetta un'ampia gamma di input (ad esempio, HWND, titolo della finestra e routine di verifica) e fornisce un codice di uscita corrispondente al numero di log degli errori.

-   [Sintassi della riga di comando](#command-line-syntax)
-   [Codici di errore della riga di comando](#command-line-error-codes)
-   [Esempi di riga di comando](#command-line-examples)
-   [Argomenti correlati](#related-topics)

![strumento da riga di comando della console AccChecker](images/accchecker-console.png)

## <a name="command-line-syntax"></a>Sintassi della riga di comando

La console di AccChecker presenta la sintassi della riga di comando seguente.

**\[Opzioni \] di AccCheckConsole (-HWND <hwnd> \| -Process <name> )\[<dlls>\]**

Di seguito sono riportate le opzioni della riga di comando.



| Opzioni                                                                                                                                                         | Descrizione                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span id="-hwnd__hwnd_"></span><span id="-HWND__HWND_"></span>-HWND <hwnd><br/>                                                                     | Convalida la finestra con l'handle specificato (HWND). L'handle può essere specificato in esadecimali o Decimal.<br/> |
| <span id="-window__title_"></span><span id="-WINDOW__TITLE_"></span>-finestra <title><br/>                                                            | Convalida la finestra con il titolo specificato.<br/>                                                                |
| <span id="__________________-process__name_"></span><span id="__________________-PROCESS__NAME_"></span> -processo <name><br/>                       | Convalida la finestra principale del processo con il nome specificato.<br/>                                             |
| <span id="____________________________-list"></span><span id="____________________________-LIST"></span> -elenco<br/>                                       | Elenca tutte le routine di verifica disponibili.<br/>                                                                 |
| <span id="__________________-enable__name_"></span><span id="__________________-ENABLE__NAME_"></span> -Abilita <name><br/>                          | Esegue la routine di verifica specificata. Questa opzione può essere specificata più di una volta.<br/>                             |
| <span id="_____________________________-disable__name_"></span><span id="_____________________________-DISABLE__NAME_"></span> -Disabilita <name><br/> | Esegue tutto tranne la routine di verifica specificata. Questa opzione può essere specificata più di una volta.<br/>                     |
| <span id="___________-log__info_warn_err_"></span><span id="___________-LOG__INFO_WARN_ERR_"></span> -log (info \| WARN \| Err)<br/>                          | Classificazione di evento più bassa che verrà registrata.<br/>                                                                      |
| <span id="__________________-logfile__file_"></span><span id="__________________-LOGFILE__FILE_"></span> -logfile <file><br/>                       | Scrive l'output nel file di log specificato. Questa opzione può essere specificata più di una volta.<br/>                          |
| <span id="-suppress__file_"></span><span id="-SUPPRESS__FILE_"></span>-non visualizzare <file><br/>                                                         | Utilizzare il file XML specificato per non visualizzare gli errori. <br/>                                                                   |
| <span id="-quiet"></span><span id="-QUIET"></span>-non interattiva<br/>                                                                                             | Non scrivere l'output di registrazione in stdout.<br/>                                                                            |
| <span id="-help__________________________________"></span><span id="-HELP__________________________________"></span>-Guida <br/>                           | Visualizza la Guida rapida. <br/>                                                                                             |



 

## <a name="command-line-error-codes"></a>Codici di errore della riga di comando

Di seguito sono riportati i codici di errore restituiti da AccCheckConsole quando si utilizza "echo% ERRORLEVEL%"



| Codice di errore                       | Descrizione                                 |
|----------------------------------|---------------------------------------------|
| <span id="0"></span>0<br/> | Nessun errore e nessun avviso.<br/>       |
| <span id="1"></span>1<br/> | È stata richiesta l'istruzione Usage. <br/> |
| <span id="2"></span>2<br/> | Errori e nessun avviso.<br/>          |
| <span id="3"></span>3<br/> | Errori e avvisi.<br/>             |
| <span id="4"></span>4<br/> | Avvisi ma senza errori.<br/>          |
| <span id="5"></span>5<br/> | Riga di comando non valida. <br/>           |



 

## <a name="command-line-examples"></a>Esempi di riga di comando

Di seguito sono riportati diversi esempi di riga di comando della console AccChecker.

-   Eseguire tutte le verifiche in una finestra con un nome specificato.

    **AccCheckConsole-finestra "senza nome-blocco note"**

-   Eseguire un subset di verifiche per un HWND, specificando un file di eliminazione.

    **AccCheckConsole-HWND 0x00382f00-Enable CheckTabbing-Enable CheckName-non visualizzare suppress.xml**

-   Eseguire tutte le verifiche da una nuova DLL di verifica.

    **AccCheckConsole-finestra "senza nome-blocco note" VerificationRoutine1.dll**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Verifica dell'accessibilità dell'interfaccia utente](ui-accessibility-checker.md)
</dt> </dl>

 

 





