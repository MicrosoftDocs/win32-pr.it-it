---
description: Le funzioni seguenti vengono utilizzate nella gestione strutturata delle eccezioni.
ms.assetid: 61cf055b-eb9a-4e56-9d36-21fc95adea77
title: Funzioni di gestione delle eccezioni strutturate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c70b431be2961a55bba28bdfe07723e93b95ac69
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304662"
---
# <a name="structured-exception-handling-functions"></a>Funzioni di gestione delle eccezioni strutturate

Le funzioni seguenti vengono utilizzate nella gestione strutturata delle eccezioni.

-   [**AbnormalTermination**](abnormaltermination.md)

    Indica se il blocco **\_ \_ try** di un gestore di terminazione è terminato normalmente.

-   [**AddVectoredContinueHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredcontinuehandler)

    Registra un gestore di continuazione vettoriale.

-   [**AddVectoredExceptionHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredexceptionhandler)

    Registra un gestore di eccezioni vettoriale.

-   [**GetExceptionCode**](getexceptioncode.md)

    Recupera un codice che identifica il tipo di eccezione che si è verificata.

-   [**GetExceptionInformation**](getexceptioninformation.md)

    Recupera una descrizione indipendente dal computer di un'eccezione e le informazioni sullo stato del computer esistente per il thread quando si è verificata l'eccezione.

-   [**RaiseException**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception)

    Genera un'eccezione nel thread chiamante.

-   [**RemoveVectoredContinueHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredcontinuehandler)

    Annulla la registrazione di un gestore di continuazione vettoriale.

-   [**RemoveVectoredExceptionHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredexceptionhandler)

    Annulla la registrazione di un gestore di eccezioni vettoriale.

-   [**RtlAddGrowableFunctionTable**](/windows/desktop/api/WinNT/nf-winnt-rtladdgrowablefunctiontable)

    Informa il sistema di una tabella di funzioni dinamiche che rappresenta un'area di memoria contenente il codice.

-   [**RtlDeleteGrowableFunctionTable**](/windows/desktop/api/WinNT/nf-winnt-rtldeletegrowablefunctiontable)

    Informa il sistema che una tabella di funzioni dinamiche segnalata in precedenza non è più utilizzata.

-   [**RtlGrowFunctionTable**](/windows/desktop/api/WinNT/nf-winnt-rtlgrowfunctiontable)

    Segnala che una tabella di funzioni dinamiche è aumentata di dimensioni.

-   [**SetUnhandledExceptionFilter**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setunhandledexceptionfilter)

    Consente a un'applicazione di sostituire il gestore di eccezioni di primo livello di ogni thread e processo.

-   [**UnhandledExceptionFilter**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-unhandledexceptionfilter)

    Passa le eccezioni non gestite al debugger, se è in corso il debug del processo.

-   [**VectoredHandler**](/windows/desktop/api/WinNT/nc-winnt-pvectored_exception_handler)

    Funzione definita dall'applicazione che funge da gestore di eccezioni vettoriale.

Le funzioni seguenti vengono utilizzate solo in Windows a 64 bit.

-   [**RtlAddFunctionTable**](/windows/desktop/api/WinNT/nf-winnt-rtladdfunctiontable)

    Aggiunge una tabella di funzioni dinamiche all'elenco di tabelle di funzioni dinamiche.

-   [**RtlCaptureContext**](/windows/desktop/api/WinNT/nf-winnt-rtlcapturecontext)

    Recupera un record di contesto nel contesto del chiamante.

-   [**RtlDeleteFunctionTable**](/windows/desktop/api/WinNT/nf-winnt-rtldeletefunctiontable)

    Rimuove una tabella di funzioni dinamiche dall'elenco tabella di funzioni dinamiche.

-   [**RtlInstallFunctionTableCallback**](/windows/desktop/api/WinNT/nf-winnt-rtlinstallfunctiontablecallback)

    Aggiunge una tabella di funzioni dinamiche all'elenco di tabelle di funzioni dinamiche.

-   [**RtlRestoreContext**](/windows/desktop/api/WinNT/nf-winnt-rtlrestorecontext)

    Ripristina il contesto del chiamante nel record di contesto specificato.

 

 
