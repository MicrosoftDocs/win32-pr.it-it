---
description: Personalizzare il comportamento di Winlogon implementando un Provider di credenziali.
ms.assetid: 70b47e29-c755-4c59-a493-d7fcbbc94b83
title: Personalizzazione di Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a10b2ae1e029bb741a2402a25d8e51f331fdd1cac1e9918dfef3b35b36c8e6d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008659"
---
# <a name="customizing-winlogon"></a>Personalizzazione di Winlogon

Personalizzare [*il comportamento di Winlogon*](/windows/desktop/SecGloss/w-gly) implementando un Provider di credenziali. Per informazioni sui provider di credenziali, vedere [**Interfaccia ICredentialProvider.**](/windows/win32/api/credentialprovider/nn-credentialprovider-icredentialprovider)

**Windows Server 2003 e Windows XP:** I provider di credenziali non sono supportati.

Le sezioni seguenti descrivono come personalizzare Winlogon nelle Windows precedenti a Windows Vista.

> [!Note]  
> LE DLL DELL'APPLICAZIONE e i pacchetti di notifica Winlogon vengono ignorati in Windows Vista.

 

-   [Pacchetti di notifica Winlogon](#winlogon-notification-packages)
-   [Stub DELL'anta](#gina-stubs)
-   [Hook DELL'associazione](#gina-hooks)

## <a name="winlogon-notification-packages"></a>Pacchetti di notifica Winlogon

Un pacchetto di notifica Winlogon è una DLL che esporta funzioni che gestiscono gli eventi Winlogon. Ad esempio, quando un utente accede al sistema, Winlogon chiama ogni pacchetto di notifica per fornire informazioni sull'evento. Per altre informazioni, vedere [Pacchetti di notifica Winlogon.](winlogon-notification-packages.md)

## <a name="gina-stubs"></a>Stub DELL'anta

Uno stub [*DELL'applicazione*](/windows/desktop/SecGloss/g-gly) è una DLL DELL'APPLICAZIONE personalizzata che usa le implementazioni della funzione di esportazione di una DLL DELLA installata in precedenza (in genere MsGina.dll). Uno stub DELL'applicazione ottiene puntatori a ogni funzione esportata dalla DLL DELL'APPLICAZIONE INSTALLATA in precedenza. Ogni funzione stub DELLA usa quindi il puntatore a funzione appropriato per chiamare la funzione corrispondente nella DLL DELL'APPLICAZIONE installata in precedenza.

> [!IMPORTANT]
> Ogni funzione stub DELL'applicazione deve chiamare la funzione corrispondente nell'applicazione DIA installata in precedenza.

 

Una funzione stub HANA può implementare funzionalità aggiuntive in una o più delle funzioni di esportazione. Ad esempio, la funzione [**WlxLoggedOutSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas) di uno stub DELL'applicazione POTREBBE controllare l'ora corrente prima di chiamare la funzione **WlxLoggedOutSAS** del MsGina.dll. Se l'ora corrente rientra in un intervallo specifico, la funzione stub potrebbe visualizzare un messaggio che indica che l'accesso non è consentito durante tale periodo di tempo e restituisce **WLX \_ SAS \_ ACTION \_ NONE** a Winlogon. La **funzione WlxLoggedOutSAS** del MsGina.dll verrà quindi chiamata solo durante il periodo di tempo consentito.

L'applicazione stub DELL'APPLICAZIONE ottiene una tabella dispatch per le funzioni di supporto di Winlogon tramite il parametro *pWinlogonFunctions* della [**funzione WlxInitialize.**](/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize) L'applicazione stub HANA può usare questa tabella dispatch per chiamare le funzioni di supporto winlogon. Ad esempio, un'applicazione stub DELL'applicazione PUÒ chiamare la funzione [**WlxSasNotify**](/windows/win32/api/winwlx/nc-winwlx-pwlx_sas_notify) per generare un evento di sequenza di attenzione sicura [](/windows/desktop/SecGloss/s-gly) (SAS) quando un [*smart card*](/windows/desktop/SecGloss/s-gly) viene inserito in un [*lettore*](/windows/desktop/SecGloss/r-gly).

Per altre informazioni sulla creazione di uno stub DELL'applicazione, vedere l'esempio Dia Stubs nella directory Samples Security Di un'installazione di \\ Platform Software Development Kit \\ \\ \\ (SDK).

> [!Note]  
> Tutte le chiamate tra UN'applicazione e Winlogon devono essere all'interno di un singolo thread.

 

## <a name="gina-hooks"></a>Hook DELL'associazione

Un hook DELL'interfaccia della riga di comando è uno stub DELL'interfaccia utente che, nell'implementazione della funzione [**WlxInitialize,**](/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize) sostituisce il puntatore alla funzione di supporto [**WlxDialogBoxParam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param) nella tabella Dispatch con un puntatore alla propria implementazione della **funzione WlxDialogBoxParam.** Di conseguenza, ogni volta che l'applicazione DELLA installata in precedenza (in genere MsGina.dll) chiama la funzione **WlxDialogBoxParam,** viene chiamata la funzione implementata dall'hook DELL'applicazione.

La [**funzione WlxDialogBoxParam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param) implementata dall'hook DELL'interfaccia a discesa può sostituire la routine di callback [**DialogProc**](/windows/win32/api/winuser/nc-winuser-dlgproc) che risponde a un evento della finestra di dialogo specifico.

In questo modo, l'hook DELL'associazione ha il controllo completo sull'aspetto e sul comportamento di tutte le finestre di dialogo create MsGina.dll finestra di dialogo.

Per altre informazioni sulla creazione di un hook DELL'applicazione, vedere l'esempio Dia Hook nella directory Samples Security Dell'installazione di \\ \\ Platform \\ \\ SDK.

> [!Note]  
> Tutte le chiamate tra UN'applicazione e Winlogon devono essere all'interno di un singolo thread.

 

 

 
