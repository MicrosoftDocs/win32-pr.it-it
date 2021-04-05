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
# <a name="the-accchecker-console"></a><span data-ttu-id="84cbc-106">Console di AccChecker</span><span class="sxs-lookup"><span data-stu-id="84cbc-106">The AccChecker Console</span></span>

<span data-ttu-id="84cbc-107">AccChecker Console (AccCheckConsole.exe) è uno strumento da riga di comando per la verifica dell'implementazione dell'accessibilità dell'interfaccia utente dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="84cbc-107">AccChecker Console (AccCheckConsole.exe) is a command-line tool for verifying the accessibility implementation of your application's UI.</span></span> <span data-ttu-id="84cbc-108">La riga di comando accetta un'ampia gamma di input (ad esempio, HWND, titolo della finestra e routine di verifica) e fornisce un codice di uscita corrispondente al numero di log degli errori.</span><span class="sxs-lookup"><span data-stu-id="84cbc-108">The command-line accepts a variety of inputs (such as HWND, window title, and verification routine) and supplies an exit code that corresponds to the error log count.</span></span>

-   [<span data-ttu-id="84cbc-109">Sintassi della riga di comando</span><span class="sxs-lookup"><span data-stu-id="84cbc-109">Command-line Syntax</span></span>](#command-line-syntax)
-   [<span data-ttu-id="84cbc-110">Codici di errore della riga di comando</span><span class="sxs-lookup"><span data-stu-id="84cbc-110">Command-line Error Codes</span></span>](#command-line-error-codes)
-   [<span data-ttu-id="84cbc-111">Esempi di riga di comando</span><span class="sxs-lookup"><span data-stu-id="84cbc-111">Command-line Examples</span></span>](#command-line-examples)
-   [<span data-ttu-id="84cbc-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="84cbc-112">Related topics</span></span>](#related-topics)

![strumento da riga di comando della console AccChecker](images/accchecker-console.png)

## <a name="command-line-syntax"></a><span data-ttu-id="84cbc-114">Sintassi della riga di comando</span><span class="sxs-lookup"><span data-stu-id="84cbc-114">Command-line Syntax</span></span>

<span data-ttu-id="84cbc-115">La console di AccChecker presenta la sintassi della riga di comando seguente.</span><span class="sxs-lookup"><span data-stu-id="84cbc-115">AccChecker Console has the following command-line syntax.</span></span>

<span data-ttu-id="84cbc-116">**\[Opzioni \] di AccCheckConsole (-HWND <hwnd> \| -Process <name> )\[<dlls>\]**</span><span class="sxs-lookup"><span data-stu-id="84cbc-116">**AccCheckConsole \[options\] (-hwnd <hwnd> \| -process <name>) \[<dlls>\]**</span></span>

<span data-ttu-id="84cbc-117">Di seguito sono riportate le opzioni della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="84cbc-117">The command-line options are as follows.</span></span>



| <span data-ttu-id="84cbc-118">Opzioni</span><span class="sxs-lookup"><span data-stu-id="84cbc-118">Options</span></span>                                                                                                                                                         | <span data-ttu-id="84cbc-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="84cbc-119">Description</span></span>                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84cbc-120"><span id="-hwnd__hwnd_"></span><span id="-HWND__HWND_"></span>-HWND <hwnd></span><span class="sxs-lookup"><span data-stu-id="84cbc-120"><span id="-hwnd__hwnd_"></span><span id="-HWND__HWND_"></span>-hwnd <hwnd></span></span><br/>                                                                     | <span data-ttu-id="84cbc-121">Convalida la finestra con l'handle specificato (HWND).</span><span class="sxs-lookup"><span data-stu-id="84cbc-121">Validates the window that has the specified handle (HWND).</span></span> <span data-ttu-id="84cbc-122">L'handle può essere specificato in esadecimali o Decimal.</span><span class="sxs-lookup"><span data-stu-id="84cbc-122">The handle can be specified in hexidecimal or decimal.</span></span><br/> |
| <span data-ttu-id="84cbc-123"><span id="-window__title_"></span><span id="-WINDOW__TITLE_"></span>-finestra <title></span><span class="sxs-lookup"><span data-stu-id="84cbc-123"><span id="-window__title_"></span><span id="-WINDOW__TITLE_"></span>-window <title></span></span><br/>                                                            | <span data-ttu-id="84cbc-124">Convalida la finestra con il titolo specificato.</span><span class="sxs-lookup"><span data-stu-id="84cbc-124">Validates the window that has the specified title.</span></span><br/>                                                                |
| <span data-ttu-id="84cbc-125"><span id="__________________-process__name_"></span><span id="__________________-PROCESS__NAME_"></span> -processo <name></span><span class="sxs-lookup"><span data-stu-id="84cbc-125"><span id="__________________-process__name_"></span><span id="__________________-PROCESS__NAME_"></span> -process <name></span></span><br/>                       | <span data-ttu-id="84cbc-126">Convalida la finestra principale del processo con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="84cbc-126">Validates the main window of the process that has the specified name.</span></span><br/>                                             |
| <span data-ttu-id="84cbc-127"><span id="____________________________-list"></span><span id="____________________________-LIST"></span> -elenco</span><span class="sxs-lookup"><span data-stu-id="84cbc-127"><span id="____________________________-list"></span><span id="____________________________-LIST"></span> -list</span></span><br/>                                       | <span data-ttu-id="84cbc-128">Elenca tutte le routine di verifica disponibili.</span><span class="sxs-lookup"><span data-stu-id="84cbc-128">Lists all of the available verification routines.</span></span><br/>                                                                 |
| <span data-ttu-id="84cbc-129"><span id="__________________-enable__name_"></span><span id="__________________-ENABLE__NAME_"></span> -Abilita <name></span><span class="sxs-lookup"><span data-stu-id="84cbc-129"><span id="__________________-enable__name_"></span><span id="__________________-ENABLE__NAME_"></span> -enable <name></span></span><br/>                          | <span data-ttu-id="84cbc-130">Esegue la routine di verifica specificata.</span><span class="sxs-lookup"><span data-stu-id="84cbc-130">Runs the specified verification routine.</span></span> <span data-ttu-id="84cbc-131">Questa opzione può essere specificata più di una volta.</span><span class="sxs-lookup"><span data-stu-id="84cbc-131">This option can be specified more than once.</span></span><br/>                             |
| <span data-ttu-id="84cbc-132"><span id="_____________________________-disable__name_"></span><span id="_____________________________-DISABLE__NAME_"></span> -Disabilita <name></span><span class="sxs-lookup"><span data-stu-id="84cbc-132"><span id="_____________________________-disable__name_"></span><span id="_____________________________-DISABLE__NAME_"></span> -disable <name></span></span><br/> | <span data-ttu-id="84cbc-133">Esegue tutto tranne la routine di verifica specificata.</span><span class="sxs-lookup"><span data-stu-id="84cbc-133">Runs all but the specified verification routine.</span></span> <span data-ttu-id="84cbc-134">Questa opzione può essere specificata più di una volta.</span><span class="sxs-lookup"><span data-stu-id="84cbc-134">This option can be specified more than once.</span></span><br/>                     |
| <span data-ttu-id="84cbc-135"><span id="___________-log__info_warn_err_"></span><span id="___________-LOG__INFO_WARN_ERR_"></span> -log (info \| WARN \| Err)</span><span class="sxs-lookup"><span data-stu-id="84cbc-135"><span id="___________-log__info_warn_err_"></span><span id="___________-LOG__INFO_WARN_ERR_"></span> -log (info\|warn\|err)</span></span><br/>                          | <span data-ttu-id="84cbc-136">Classificazione di evento più bassa che verrà registrata.</span><span class="sxs-lookup"><span data-stu-id="84cbc-136">The lowest event rating that will be logged.</span></span><br/>                                                                      |
| <span data-ttu-id="84cbc-137"><span id="__________________-logfile__file_"></span><span id="__________________-LOGFILE__FILE_"></span> -logfile <file></span><span class="sxs-lookup"><span data-stu-id="84cbc-137"><span id="__________________-logfile__file_"></span><span id="__________________-LOGFILE__FILE_"></span> -logfile <file></span></span><br/>                       | <span data-ttu-id="84cbc-138">Scrive l'output nel file di log specificato.</span><span class="sxs-lookup"><span data-stu-id="84cbc-138">Write the output to the specified log file.</span></span> <span data-ttu-id="84cbc-139">Questa opzione può essere specificata più di una volta.</span><span class="sxs-lookup"><span data-stu-id="84cbc-139">This option can be specified more than once.</span></span><br/>                          |
| <span data-ttu-id="84cbc-140"><span id="-suppress__file_"></span><span id="-SUPPRESS__FILE_"></span>-non visualizzare <file></span><span class="sxs-lookup"><span data-stu-id="84cbc-140"><span id="-suppress__file_"></span><span id="-SUPPRESS__FILE_"></span>-suppress <file></span></span><br/>                                                         | <span data-ttu-id="84cbc-141">Utilizzare il file XML specificato per non visualizzare gli errori.</span><span class="sxs-lookup"><span data-stu-id="84cbc-141">Use the specified XML file to suppress errors.</span></span> <br/>                                                                   |
| <span data-ttu-id="84cbc-142"><span id="-quiet"></span><span id="-QUIET"></span>-non interattiva</span><span class="sxs-lookup"><span data-stu-id="84cbc-142"><span id="-quiet"></span><span id="-QUIET"></span>-quiet</span></span><br/>                                                                                             | <span data-ttu-id="84cbc-143">Non scrivere l'output di registrazione in stdout.</span><span class="sxs-lookup"><span data-stu-id="84cbc-143">Do not write logging output to stdout.</span></span><br/>                                                                            |
| <span data-ttu-id="84cbc-144"><span id="-help__________________________________"></span><span id="-HELP__________________________________"></span>-Guida</span><span class="sxs-lookup"><span data-stu-id="84cbc-144"><span id="-help__________________________________"></span><span id="-HELP__________________________________"></span>-help</span></span> <br/>                           | <span data-ttu-id="84cbc-145">Visualizza la Guida rapida.</span><span class="sxs-lookup"><span data-stu-id="84cbc-145">Displays quick help.</span></span> <br/>                                                                                             |



 

## <a name="command-line-error-codes"></a><span data-ttu-id="84cbc-146">Codici di errore della riga di comando</span><span class="sxs-lookup"><span data-stu-id="84cbc-146">Command-line Error Codes</span></span>

<span data-ttu-id="84cbc-147">Di seguito sono riportati i codici di errore restituiti da AccCheckConsole quando si utilizza "echo% ERRORLEVEL%"</span><span class="sxs-lookup"><span data-stu-id="84cbc-147">Following are error codes returned from AccCheckConsole when using "echo %errorlevel%"</span></span>



| <span data-ttu-id="84cbc-148">Codice di errore</span><span class="sxs-lookup"><span data-stu-id="84cbc-148">Error code</span></span>                       | <span data-ttu-id="84cbc-149">Descrizione</span><span class="sxs-lookup"><span data-stu-id="84cbc-149">Description</span></span>                                 |
|----------------------------------|---------------------------------------------|
| <span data-ttu-id="84cbc-150"><span id="0"></span>0</span><span class="sxs-lookup"><span data-stu-id="84cbc-150"><span id="0"></span>0</span></span><br/> | <span data-ttu-id="84cbc-151">Nessun errore e nessun avviso.</span><span class="sxs-lookup"><span data-stu-id="84cbc-151">No errors and no warnings.</span></span><br/>       |
| <span data-ttu-id="84cbc-152"><span id="1"></span>1</span><span class="sxs-lookup"><span data-stu-id="84cbc-152"><span id="1"></span>1</span></span><br/> | <span data-ttu-id="84cbc-153">È stata richiesta l'istruzione Usage.</span><span class="sxs-lookup"><span data-stu-id="84cbc-153">Usages statement was requested.</span></span> <br/> |
| <span data-ttu-id="84cbc-154"><span id="2"></span>2</span><span class="sxs-lookup"><span data-stu-id="84cbc-154"><span id="2"></span>2</span></span><br/> | <span data-ttu-id="84cbc-155">Errori e nessun avviso.</span><span class="sxs-lookup"><span data-stu-id="84cbc-155">Errors and no warnings.</span></span><br/>          |
| <span data-ttu-id="84cbc-156"><span id="3"></span>3</span><span class="sxs-lookup"><span data-stu-id="84cbc-156"><span id="3"></span>3</span></span><br/> | <span data-ttu-id="84cbc-157">Errori e avvisi.</span><span class="sxs-lookup"><span data-stu-id="84cbc-157">Errors and warnings.</span></span><br/>             |
| <span data-ttu-id="84cbc-158"><span id="4"></span>4</span><span class="sxs-lookup"><span data-stu-id="84cbc-158"><span id="4"></span>4</span></span><br/> | <span data-ttu-id="84cbc-159">Avvisi ma senza errori.</span><span class="sxs-lookup"><span data-stu-id="84cbc-159">Warnings but no errors.</span></span><br/>          |
| <span data-ttu-id="84cbc-160"><span id="5"></span>5</span><span class="sxs-lookup"><span data-stu-id="84cbc-160"><span id="5"></span>5</span></span><br/> | <span data-ttu-id="84cbc-161">Riga di comando non valida.</span><span class="sxs-lookup"><span data-stu-id="84cbc-161">Invalid command line.</span></span> <br/>           |



 

## <a name="command-line-examples"></a><span data-ttu-id="84cbc-162">Esempi di riga di comando</span><span class="sxs-lookup"><span data-stu-id="84cbc-162">Command-line Examples</span></span>

<span data-ttu-id="84cbc-163">Di seguito sono riportati diversi esempi di riga di comando della console AccChecker.</span><span class="sxs-lookup"><span data-stu-id="84cbc-163">Following are several AccChecker Console command-line examples.</span></span>

-   <span data-ttu-id="84cbc-164">Eseguire tutte le verifiche in una finestra con un nome specificato.</span><span class="sxs-lookup"><span data-stu-id="84cbc-164">Run all verifications on a window with a specified name.</span></span>

    <span data-ttu-id="84cbc-165">**AccCheckConsole-finestra "senza nome-blocco note"**</span><span class="sxs-lookup"><span data-stu-id="84cbc-165">**AccCheckConsole -window "Untitled - Notepad"**</span></span>

-   <span data-ttu-id="84cbc-166">Eseguire un subset di verifiche per un HWND, specificando un file di eliminazione.</span><span class="sxs-lookup"><span data-stu-id="84cbc-166">Run a subset of the verifications against an HWND, specifying a suppression file.</span></span>

    <span data-ttu-id="84cbc-167">**AccCheckConsole-HWND 0x00382f00-Enable CheckTabbing-Enable CheckName-non visualizzare suppress.xml**</span><span class="sxs-lookup"><span data-stu-id="84cbc-167">**AccCheckConsole -hwnd 0x00382f00 -enable CheckTabbing -enable CheckName -suppress suppress.xml**</span></span>

-   <span data-ttu-id="84cbc-168">Eseguire tutte le verifiche da una nuova DLL di verifica.</span><span class="sxs-lookup"><span data-stu-id="84cbc-168">Run all verifications from a new verification DLL.</span></span>

    <span data-ttu-id="84cbc-169">**AccCheckConsole-finestra "senza nome-blocco note" VerificationRoutine1.dll**</span><span class="sxs-lookup"><span data-stu-id="84cbc-169">**AccCheckConsole -window "Untitled - Notepad" VerificationRoutine1.dll**</span></span>

## <a name="related-topics"></a><span data-ttu-id="84cbc-170">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="84cbc-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84cbc-171">Verifica dell'accessibilità dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="84cbc-171">UI Accessibility Checker</span></span>](ui-accessibility-checker.md)
</dt> </dl>

 

 





