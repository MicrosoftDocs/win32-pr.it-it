---
description: Si supponga, ai fini di un esempio, che l'applicazione chiami la funzione TAPI lineConfigDialog, progettata per aprire una finestra di dialogo per consentire la configurazione delle opzioni del provider di servizi correlate al dispositivo linea specificato.
ms.assetid: a388d192-a327-4e67-968b-344d80c19fb1
title: Funzioni progettate per generare l'interfaccia utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63e7aeda54d4c04a144b2786b56f32d13c51ab39c5274204485151caecc2db1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140614"
---
# <a name="functions-designed-to-generate-ui"></a>Funzioni progettate per generare l'interfaccia utente

Si supponga, ai fini di un esempio, che l'applicazione chiami la funzione [**TAPI lineConfigDialog,**](/windows/win32/api/tapi/nf-tapi-lineconfigdialog) progettata per aprire una finestra di dialogo per consentire la configurazione delle opzioni del provider di servizi correlate al dispositivo linea specificato. In risposta a questa chiamata, TAPI richiede a TAPISRV di chiamare [**provider \_ TSPIUIIdentify**](/windows/win32/api/tspi/nf-tspi-tspi_provideruiidentify) nel provider di servizi di telefonia, ottenendo il nome della DLL dell'interfaccia utente TSP.

Nel contesto dell'applicazione, TAPI carica la DLL dell'interfaccia utente TSP e chiama la funzione [**\_ lineConfigDialog TUISPI**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog) con i parametri forniti dall'applicazione e includendo un puntatore alla funzione [*DLLCallbackProc*](/windows/win32/api/tspi/nc-tspi-tuispidllcallback) TAPI. La DLL dell'interfaccia utente TSP visualizza la finestra di dialogo di configurazione, chiamando la funzione *DllCallbackProc* in base alle esigenze per ottenere dal provider di servizi di telefonia le informazioni da visualizzare. Ogni volta che viene chiamata la funzione *DllCallbackProc,* TAPI richiede a TAPISRV di chiamare la funzione [**TSPI \_ providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tspi_providergenericdialogdata) del provider del servizio di telefonia, passando il blocco di parametri dalla DLL dell'interfaccia utente e restituisce il blocco di parametri alla DLL dell'interfaccia utente. La DLL dell'interfaccia utente trasmette le modifiche di configurazione al provider di servizi di telefonia chiamando *DllCallbackProc*.

Al termine della funzione, la DLL dell'interfaccia utente restituisce da (in questo caso) [**LINEISPI \_ lineConfigDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog). TAPI chiama la [**funzione FreeLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary) per rilasciare la DLL dell'interfaccia utente e torna all'applicazione.

 

 
