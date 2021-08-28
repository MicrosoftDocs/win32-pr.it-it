---
description: A partire da TAPI 2.1, le DLL dell'interfaccia utente del provider di servizi di telefonia possono essere usate per gestire e visualizzare le finestre di dialogo. TAPI carica la DLL nel processo di un'applicazione che richiama una qualsiasi delle funzioni del provider di servizi in grado di visualizzare una finestra di dialogo.
ms.assetid: 0a0320d1-fb75-405e-8074-b37cef956c9f
title: Novità di TSPI versione 2.1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 260978ad99bf49ed0beae0e71b2a02a794eef1a7af0c25074c20a08c1da054c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119659821"
---
# <a name="whats-new-for-tspi-version-21"></a>Novità di TSPI versione 2.1

A partire da TAPI 2.1, le DLL dell'interfaccia utente del provider di servizi di telefonia possono essere usate per gestire e visualizzare le finestre di dialogo. TAPI carica la DLL nel processo di un'applicazione che richiama una qualsiasi delle funzioni del provider di servizi in grado di visualizzare una finestra di dialogo.

A partire da TAPI 2.1, i gestori delle richieste proxy possono essere implementati. Un gestore è un'applicazione di telefonia completa che in genere viene eseguita in un server di telefonia e fornisce servizi implementati in modo più appropriato in un'applicazione rispetto a un driver.

Le funzioni e i messaggi nuovi o modificati per TSPI versione 2.1 sono i seguenti:

-   [**TSPI_lineConditionalMediaDetection**](/windows/win32/api/tspi/nf-tspi-tspi_lineconditionalmediadetection)
-   **TSPI_lineDropNoOwner**:**obsoleto**
-   **TSPI_lineDropOnClose**:**obsoleto**
-   [**TSPI_lineGetID**](/windows/win32/api/tspi/nf-tspi-tspi_linegetid)
-   [**TSPI_lineSetCallData**](/windows/win32/api/tspi/nf-tspi-tspi_linesetcalldata)
-   [**TSPI_lineSetCallQualityOfService**](/windows/win32/api/tspi/nf-tspi-tspi_linesetcallqualityofservice)
-   [**TSPI_lineSetCallTreatment**](/windows/win32/api/tspi/nf-tspi-tspi_linesetcalltreatment)
-   [**TSPI_lineSetLineDevStatus**](/windows/win32/api/tspi/nf-tspi-tspi_linesetlinedevstatus)
-   [**TSPI_phoneGetID**](/windows/win32/api/tspi/nf-tspi-tspi_phonegetid)
-   [**TSPI_providerInit**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit)
-   [**TSPI_providerShutdown**](/windows/win32/api/tspi/nf-tspi-tspi_providershutdown)
-   [**LINE_GATHERDIGITS**](/previous-versions/windows/desktop/legacy/ms725229(v=vs.85))
-   [**LINE_GENERATE**](/previous-versions/windows/desktop/legacy/ms725230(v=vs.85))
-   [**LINE_MONITORDIGITS**](/previous-versions/windows/desktop/legacy/ms725232(v=vs.85))
-   [**LINE_MONITORMEDIA**](/previous-versions/windows/desktop/legacy/ms725233(v=vs.85))
-   [**LINE_MONITORTONE**](/previous-versions/windows/desktop/legacy/ms725234(v=vs.85))
-   [**LINE_REMOVE**](/previous-versions/windows/desktop/legacy/ms725237(v=vs.85))
-   [**PHONE_REMOVE**](/previous-versions/windows/desktop/legacy/ms725260(v=vs.85))

La DLL dell'interfaccia utente del provider di servizi di telefonia consente l'interazione dell'utente all'interno del contesto dell'applicazione anziché del provider di servizi stesso. TSPI versione 2.1 ha fornito le nuove funzioni, i messaggi e le strutture seguenti per l'implementazione:

-   [**TSPI_providerFreeDialogInstance**](/windows/win32/api/tspi/nf-tspi-tspi_providerfreedialoginstance)
-   [**TSPI_providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tspi_providergenericdialogdata)
-   [**TSPI_providerUIIdentify**](/windows/win32/api/tspi/nf-tspi-tspi_provideruiidentify)
-   [**TUISPI_lineConfigDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog)
-   [**TUISPI_lineConfigDialogEdit**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialogedit)
-   [**TUISPI_phoneConfigDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_phoneconfigdialog)
-   [**TUISPI_providerConfig**](/windows/win32/api/tspi/nf-tspi-tuispi_providerconfig)
-   [**TUISPI_providerGenericDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog)
-   [**TUISPI_providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata)
-   [**TUISPI_providerInstall**](/windows/win32/api/tspi/nf-tspi-tuispi_providerinstall)
-   [**TUISPI_providerRemove**](/windows/win32/api/tspi/nf-tspi-tuispi_providerremove)
-   [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams)
-   [**TUISPIDLLCALLBACK**](/windows/win32/api/tspi/nc-tspi-tuispidllcallback)
-   [**LINE_CREATEDIALOGINSTANCE**](line-createdialoginstance.md)
-   [**LINE_SENDDIALOGINSTANCEDATA**](line-senddialoginstancedata.md)

 

 
