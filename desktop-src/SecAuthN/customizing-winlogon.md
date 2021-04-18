---
description: Personalizzare il comportamento di Winlogon implementando un provider di credenziali.
ms.assetid: 70b47e29-c755-4c59-a493-d7fcbbc94b83
title: Personalizzazione di Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b64da4baae9b52dd53e288c631f35d33ea5a3085
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308153"
---
# <a name="customizing-winlogon"></a>Personalizzazione di Winlogon

Personalizzare il comportamento di [*Winlogon*](/windows/desktop/SecGloss/w-gly) implementando un provider di credenziali. Per informazioni sui provider di credenziali, vedere [**interfaccia ICredentialProvider**](/windows/win32/api/credentialprovider/nn-credentialprovider-icredentialprovider).

**Windows Server 2003 e Windows XP:** I provider di credenziali non sono supportati.

Nelle sezioni seguenti vengono descritte le modalità di personalizzazione di Winlogon nelle versioni di Windows precedenti a Windows Vista.

> [!Note]  
> Le DLL GINA e i pacchetti di notifica Winlogon vengono ignorati in Windows Vista.

 

-   [Pacchetti di notifica di Winlogon](#winlogon-notification-packages)
-   [Stub GINA](#gina-stubs)
-   [Hook GINA](#gina-hooks)

## <a name="winlogon-notification-packages"></a>Pacchetti di notifica di Winlogon

Un pacchetto di notifica Winlogon è una DLL che esporta funzioni che gestiscono gli eventi Winlogon. Ad esempio, quando un utente accede al sistema, Winlogon chiama ogni pacchetto di notifica per fornire informazioni sull'evento. Per altre informazioni, vedere [pacchetti di notifica di Winlogon](winlogon-notification-packages.md).

## <a name="gina-stubs"></a>Stub GINA

Uno Stub [*Gina*](/windows/desktop/SecGloss/g-gly) è una DLL personalizzata Gina che usa le implementazioni delle funzioni di esportazione di una DLL GINA installata in precedenza (in genere MsGina.dll). Uno stub GINA ottiene i puntatori a ogni funzione esportata dalla DLL GINA installata in precedenza. Ogni funzione stub GINA usa quindi il puntatore a funzione appropriato per chiamare la funzione corrispondente nella DLL GINA installata in precedenza.

> [!IMPORTANT]
> Ogni funzione stub GINA deve chiamare la funzione corrispondente nell'oggetto GINA installato in precedenza.

 

Una funzione stub GINA può implementare funzionalità aggiuntive in una o più funzioni di esportazione. Ad esempio, la funzione [**WlxLoggedOutSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas) di uno stub GINA potrebbe controllare l'ora corrente prima di chiamare la funzione **WlxLoggedOutSAS** della MsGina.dll. Se l'ora corrente si trovava in un intervallo specifico, la funzione stub potrebbe visualizzare un messaggio che indica che l'accesso non è consentito durante tale periodo di tempo e restituire l' **\_ \_ azione \_ Nessuna** firma di accesso condiviso di WLX a Winlogon. La funzione **WlxLoggedOutSAS** del MsGina.dll verrebbe quindi chiamata solo durante il periodo di tempo consentito.

L'applicazione GINA Stub ottiene una tabella dispatch per le funzioni di supporto di Winlogon tramite il parametro *pWinlogonFunctions* della funzione [**WlxInitialize**](/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize) . L'applicazione GINA stub può usare questa tabella dispatch per chiamare le funzioni di supporto di Winlogon. Ad esempio, un'applicazione stub GINA può chiamare la funzione [**WlxSasNotify**](/windows/win32/api/winwlx/nc-winwlx-pwlx_sas_notify) per generare un evento di firma di [*attenzione sicura*](/windows/desktop/SecGloss/s-gly) quando una [*Smart Card*](/windows/desktop/SecGloss/s-gly) viene inserita in un [*lettore*](/windows/desktop/SecGloss/r-gly).

Per ulteriori informazioni sulla creazione di uno stub GINA, vedere l'esempio Gina Stub nella \\ directory Samples \\ Security \\ Gina \\ GinaStub di un'installazione di Platform Software Development Kit (SDK).

> [!Note]  
> Tutte le chiamate tra un oggetto GINA e Winlogon devono trovarsi all'interno di un singolo thread.

 

## <a name="gina-hooks"></a>Hook GINA

Un hook GINA è uno stub GINA che, nell'implementazione della funzione [**WlxInitialize**](/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize) , sostituisce il puntatore alla funzione di supporto [**WlxDialogBoxParam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param) nella tabella dispatch con un puntatore alla propria implementazione della funzione **WlxDialogBoxParam** . Di conseguenza, ogni volta che l'oggetto GINA precedentemente installato (in genere MsGina.dll) chiama la funzione **WlxDialogBoxParam** , viene chiamata la funzione implementata dall'hook Gina.

La funzione [**WlxDialogBoxParam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param) implementata dall'hook Gina può sostituire la routine di callback [**DialogProc**](/windows/win32/api/winuser/nc-winuser-dlgproc) che risponde a un evento specifico della finestra di dialogo.

Questo consente all'hook GINA di controllare completamente l'aspetto e il comportamento di tutte le finestre di dialogo create da MsGina.dll.

Per ulteriori informazioni sulla creazione di un hook GINA, vedere l'esempio relativo a Gina hook \\ nella \\ directory Samples Security \\ Gina \\ GinaHook dell'installazione di Platform SDK.

> [!Note]  
> Tutte le chiamate tra un oggetto GINA e Winlogon devono trovarsi all'interno di un singolo thread.

 

 

 
