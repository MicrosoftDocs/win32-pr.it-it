---
description: Si supponga ai fini di un esempio che l'applicazione chiama la funzione TAPI lineConfigDialog, progettata per aprire una finestra di dialogo per consentire la configurazione delle opzioni del provider di servizi correlate al dispositivo della linea specificato.
ms.assetid: a388d192-a327-4e67-968b-344d80c19fb1
title: Funzioni progettate per generare l'interfaccia utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa360effd2a1504d2325be2131c430664f1e7a5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966693"
---
# <a name="functions-designed-to-generate-ui"></a>Funzioni progettate per generare l'interfaccia utente

Si supponga ai fini di un esempio che l'applicazione chiama la funzione TAPI [**lineConfigDialog**](/windows/win32/api/tapi/nf-tapi-lineconfigdialog) , progettata per aprire una finestra di dialogo per consentire la configurazione delle opzioni del provider di servizi correlate al dispositivo della linea specificato. In risposta a questa chiamata, TAPI richiede TAPISRV per chiamare [**TSPI \_ providerUIIdentify**](/windows/win32/api/tspi/nf-tspi-tspi_provideruiidentify) nel provider del servizio di telefonia, ottenendo il nome della DLL dell'interfaccia utente di tsp.

Nel contesto dell'applicazione, TAPI carica la DLL dell'interfaccia utente di TSP e chiama la funzione [**TUISPI \_ lineConfigDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog) con i parametri forniti dall'applicazione e includendo un puntatore alla funzione TAPI [*DllCallbackProc*](/windows/win32/api/tspi/nc-tspi-tuispidllcallback) . La DLL dell'interfaccia utente di TSP Visualizza la finestra di dialogo di configurazione, chiamando la funzione *DllCallbackProc* , se necessario, per ottenere dal provider del servizio di telefonia le informazioni da visualizzare. Ogni volta che viene chiamata la funzione *DllCallbackProc* , TAPI richiede tapisrv per chiamare la funzione [**TSPI \_ providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tspi_providergenericdialogdata) del provider di servizi di telefonia, passando il blocco di parametri dalla DLL dell'interfaccia utente e restituendo il blocco di parametri alla DLL dell'interfaccia utente. La DLL dell'interfaccia utente trasmette qualsiasi modifica di configurazione al provider del servizio di telefonia chiamando *DllCallbackProc*.

Quando la funzione è completa, la DLL dell'interfaccia utente restituisce da (in questo caso) [**TUISPI \_ lineConfigDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog). TAPI chiama la funzione [**FreeLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary) per rilasciare la DLL dell'interfaccia utente e torna all'applicazione.

 

 
