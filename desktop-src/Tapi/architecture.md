---
description: La figura seguente illustra l'architettura generale dei provider di servizi di telefonia e le librerie a collegamento dinamico (DLL) dell'interfaccia utente associate.
ms.assetid: b5efe57a-19b8-49c5-810f-180633ed50d2
title: Architettura (API di telefonia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96d37c2911a664fee2670a41444ee01e4390c8ee5dd526bf550b75eab4990009
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118871980"
---
# <a name="architecture-telephony-api"></a>Architettura (API di telefonia)

La figura seguente illustra l'architettura generale dei provider di servizi di telefonia e le librerie a collegamento dinamico (DLL) dell'interfaccia utente associate.

![tsps e DLL dell'interfaccia utente associate](images/spuidl01.png)

Il provider di servizi è costituito da almeno due componenti. DLL del provider di servizi (designata nella figura come MAIN. TSP) viene eseguito nel contesto del processo TAPISRV ed esegue tutte le attività del provider di servizi non correlate agli elementi dell'interfaccia utente associati all'uso del dispositivo da parte di una determinata applicazione (molto probabilmente, in combinazione con i componenti di livello inferiore non illustrati nella figura). A differenza delle versioni precedenti di TAPI in cui il codice dell'interfaccia utente è stato integrato nel provider di servizi (ed eseguito, a causa dell'architettura precedente, all'interno del contesto dell'applicazione), il provider di servizi deve ora includere un componente separato che implementa gli elementi dell'interfaccia utente.

La DLL dell'interfaccia utente del provider di servizi deve esportare le funzioni chiamate da TAPI quando l'applicazione chiama le funzioni TAPI che generano l'interfaccia utente: [**TUISPI \_ lineConfigDialog,**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog) [**TUISPI \_ lineConfigDialogEdit,**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialogedit) [**TUISPI \_ phoneConfigDialog,**](/windows/win32/api/tspi/nf-tspi-tuispi_phoneconfigdialog) [**TUISPI \_ providerConfig,**](/windows/win32/api/tspi/nf-tspi-tuispi_providerconfig) [**TUISPI \_ providerInstall**](/windows/win32/api/tspi/nf-tspi-tuispi_providerinstall)e [**TUISPI \_ providerRemove**](/windows/win32/api/tspi/nf-tspi-tuispi_providerremove). Ognuna di queste funzioni include come parametro un puntatore a una funzione di callback in TAPI, di tipo [**TUISPIDLLCALLBACK,**](/windows/win32/api/tspi/nc-tspi-tuispidllcallback)che la DLL dell'interfaccia utente può usare per comunicare bidirezionale (invio e ricezione di dati) con la DLL del provider di servizi in esecuzione nel processo TAPISRV. Se il provider di servizi genera un'interfaccia utente non funzionante, ad esempio la finestra di dialogo Unimodem **Talk/Hangup,** insieme a qualsiasi funzione TSPI per cui l'interfaccia utente non è prevista (ad esempio, qualsiasi funzione che non dispone di un parametro *hwnd),* la DLL dell'interfaccia utente deve esportare il [**provider TUISPIGenericDialog \_**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog) e il [**provider TUISPIGenericDialogData \_**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata).

> [!Note]  
> Le funzioni originali di generazione dell'interfaccia utente [**TSPI (TSPI \_ lineConfigDialog,**](/windows/win32/api/tspi/nf-tspi-tspi_lineconfigdialog) [**TSPI \_ lineConfigDialogEdit,**](/windows/win32/api/tspi/nf-tspi-tspi_lineconfigdialogedit) [**TSPI \_ phoneConfigDialog,**](/windows/win32/api/tspi/nf-tspi-tspi_phoneconfigdialog) [**\_ providerConfig TSPI,**](/windows/win32/api/tspi/nf-tspi-tspi_providerconfig) [**provider \_ TSPIInstall**](/windows/win32/api/tspi/nf-tspi-tspi_providerinstall)e [**provider \_ TSPIRemove**](/windows/win32/api/tspi/nf-tspi-tspi_providerremove)) sono obsolete e non vengono mai chiamate da TAPI. Di conseguenza, non è necessario che siano esportati dalla DLL del provider di servizi. Tuttavia, se il provider di servizi vuole essere elencato come un provider che può essere aggiunto dal servizio di telefonia Pannello di controllo, Un'utilità fornita con Windows Telefonia [](/windows/win32/api/tapi3if/nn-tapi3if-itcollection2) nelle versioni 1.4 e precedenti, deve esportare **il provider TSPIInstall; \_** se si vuole che il pulsante Rimuovi sia abilitato nel Pannello di controllo di telefonia quando è selezionato, è necessario esportare il **provider TSPIRemove \_** e, se si desidera che il pulsante di installazione sia abilitato nel Pannello di controllo di telefonia quando è selezionato, è necessario esportare provider  **\_ TSPIConfig**. L'Pannello di controllo di telefonia verifica la presenza di queste funzioni nel file TSP del provider di servizi per modificare l'interfaccia utente in modo da riflettere le operazioni che possono essere eseguite.

 

La DLL del provider di servizi deve esportare la funzione [**provider \_ TSPIUIIdentify**](/windows/win32/api/tspi/nf-tspi-tspi_provideruiidentify) utilizzata dal processo TAPISRV per ottenere il nome della DLL dell'interfaccia utente da caricare nel processo dell'applicazione. Deve esportare la funzione [**TSPI \_ providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tspi_providergenericdialogdata) per ricevere e rispondere alle richieste dalla DLL dell'interfaccia utente per la visualizzazione dei dati e deve [**esportare il provider TSPIFreeDialogInstance \_**](/windows/win32/api/tspi/nf-tspi-tspi_providerfreedialoginstance) per il processo TAPISRV per indicare al provider di servizi quando rilasciare un'associazione stabilita allo scopo di generare un'interfaccia utente non funzionante insieme a una funzione non definita come presentazione dell'interfaccia utente all'utente. La DLL del provider di servizi può inviare dati in modo unidirezionale alla DLL dell'interfaccia utente usando il nuovo messaggio TSPI [**LINE \_ SENDDIALOGINSTANCEDATA**](line-senddialoginstancedata.md).

Poiché i nomi delle funzioni TSPI e TUISPI sono intenzionalmente definiti come diversi, la DLL del provider di servizi e la DLL dell'interfaccia utente possono essere lo stesso file DLL, se necessario. Con una segmentazione appropriata, ciò non comporta necessariamente un utilizzo non necessario della memoria nel contesto dell'applicazione e può semplificare il processo di installazione per i provider di servizi che possono essere attualmente implementati in una singola DLL. TAPI chiama solo le funzioni appropriate per il contesto in cui viene utilizzata la DLL.

Il provider di servizi di telefonia e la DLL dell'interfaccia utente devono essere entrambi progettati in base al requisito che le funzioni dell'interfaccia utente possano essere richiamate contemporaneamente da più processi dell'applicazione. Devono inoltre considerare che l'applicazione e il servizio TAPI in cui è in esecuzione il provider di servizi di telefonia possono essere in computer separati su una LAN.

 

 
