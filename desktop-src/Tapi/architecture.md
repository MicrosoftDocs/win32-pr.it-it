---
description: Nella figura seguente viene illustrata l'architettura generale dei provider di servizi di telefonia e delle librerie di collegamento dinamico (dll UI) associate dell'interfaccia utente.
ms.assetid: b5efe57a-19b8-49c5-810f-180633ed50d2
title: Architettura (API di telefonia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14423dba77af1ded38af4a6f2b896e76d28ca2cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311911"
---
# <a name="architecture-telephony-api"></a>Architettura (API di telefonia)

Nella figura seguente viene illustrata l'architettura generale dei provider di servizi di telefonia e delle librerie di collegamento dinamico (dll UI) associate dell'interfaccia utente.

![TSPs e dll UI associate](images/spuidl01.png)

Il provider di servizi è costituito da un minimo di due componenti. DLL del provider di servizi (designata nell'illustrazione come principale). TSP) viene eseguito nel contesto del processo TAPISRV ed esegue tutte le attività del provider di servizi che non sono correlate agli elementi dell'interfaccia utente associati all'uso del dispositivo da parte di un'applicazione specifica (probabilmente, in combinazione con componenti di livello inferiore non mostrati nell'illustrazione). Tuttavia, a differenza delle versioni precedenti di TAPI, in cui il codice dell'interfaccia utente è stato integrato nel provider di servizi (ed eseguito, a causa dell'architettura precedente, all'interno del contesto dell'applicazione), il provider di servizi deve includere ora un componente separato che implementa gli elementi dell'interfaccia utente.

La DLL dell'interfaccia utente del provider di servizi deve esportare le funzioni chiamate da TAPI quando l'applicazione chiama funzioni TAPI che generano l'interfaccia utente: [**TUISPI \_ lineConfigDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog), [**TUISPI \_ lineConfigDialogEdit**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialogedit), [**TUISPI \_ PhoneConfigDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_phoneconfigdialog), [**TUISPI \_ providerConfig**](/windows/win32/api/tspi/nf-tspi-tuispi_providerconfig), TUISPI providerInstall e [**TUISPI \_**](/windows/win32/api/tspi/nf-tspi-tuispi_providerremove)providerRemove. [**\_**](/windows/win32/api/tspi/nf-tspi-tuispi_providerinstall) Ognuna di queste funzioni include come parametro un puntatore a una funzione di callback in TAPI, di tipo [**TUISPIDLLCALLBACK**](/windows/win32/api/tspi/nc-tspi-tuispidllcallback), che la DLL dell'interfaccia utente può usare per comunicare in modo bidirezionale (entrambi i dati di invio e ricezione) con la dll del provider di servizi in esecuzione nel processo tapisrv. Se il provider di servizi genera un'interfaccia utente spontanea, ad esempio la finestra di dialogo UniModel **Talk/hangup** , insieme a qualsiasi funzione TSPI per la quale non è prevista l'interfaccia utente (ad esempio, qualsiasi funzione che non ha un parametro *HWND* ), la DLL dell'interfaccia utente deve esportare [**TUISPI \_ providerGenericDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog) e [**TUISPI \_ providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata).

> [!Note]  
> Le funzioni originali di generazione dell'interfaccia utente di TSPI ( [**TSPI \_ lineConfigDialog**](/windows/win32/api/tspi/nf-tspi-tspi_lineconfigdialog), [**TSPI \_ lineConfigDialogEdit**](/windows/win32/api/tspi/nf-tspi-tspi_lineconfigdialogedit), TSPI [**\_ PhoneConfigDialog**](/windows/win32/api/tspi/nf-tspi-tspi_phoneconfigdialog) [**, TSPI \_ providerConfig**](/windows/win32/api/tspi/nf-tspi-tspi_providerconfig), TSPI [**\_ PROVIDERINSTALL**](/windows/win32/api/tspi/nf-tspi-tspi_providerinstall)e TSPI providerRemove) sono obsolete e non vengono mai chiamate da TAPI. [**\_**](/windows/win32/api/tspi/nf-tspi-tspi_providerremove) Pertanto, non è necessario che vengano esportate dalla DLL del provider di servizi. Tuttavia, se il provider di servizi vuole essere elencato come uno che può essere aggiunto dal pannello di controllo della telefonia, un'utilità fornita con la telefonia Windows nelle versioni 1,4 e precedenti, deve esportare **TSPI \_ providerInstall**; se si desidera che il pulsante [**Rimuovi**](/windows/win32/api/tapi3if/nn-tapi3if-itcollection2) sia abilitato nel pannello di controllo della telefonia quando è selezionato, deve esportare **TSPI \_ providerRemove**; e se desidera che il pulsante di **installazione** sia abilitato nel pannello di controllo della telefonia quando è selezionato, deve esportare **TSPI \_** providerConfig. Il pannello di controllo della telefonia verifica la presenza di queste funzioni nel file TSP del provider di servizi per regolare l'interfaccia utente in modo da riflettere le operazioni che possono essere eseguite.

 

La DLL del provider di servizi deve esportare la funzione [**TSPI \_ providerUIIdentify**](/windows/win32/api/tspi/nf-tspi-tspi_provideruiidentify) utilizzata dal processo tapisrv per ottenere il nome della DLL dell'interfaccia utente da caricare nel processo dell'applicazione. Deve esportare la funzione [**TSPI \_ providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tspi_providergenericdialogdata) per ricevere e rispondere alle richieste dalla DLL dell'interfaccia utente per la visualizzazione dei dati e deve esportare [**TSPI \_ providerFreeDialogInstance**](/windows/win32/api/tspi/nf-tspi-tspi_providerfreedialoginstance) per il processo tapisrv per indicare al provider di servizi quando rilasciare un'associazione stabilita allo scopo di generare un'interfaccia utente spontanea insieme a una funzione non definita come presentazione dell'interfaccia utente. La DLL del provider di servizi può inviare in modo unidirezionale i dati alla DLL dell'interfaccia utente usando la nuova riga di messaggio TSPI [**\_ SENDDIALOGINSTANCEDATA**](line-senddialoginstancedata.md).

Poiché i nomi delle funzioni TSPI e TUISPI sono intenzionalmente definiti come diversi, la DLL del provider di servizi e la DLL dell'interfaccia utente possono essere lo stesso file DLL, se lo si desidera. Con la segmentazione corretta, questo non comporta necessariamente un utilizzo non necessario della memoria nel contesto dell'applicazione e può semplificare il processo di installazione per i provider di servizi che attualmente possono essere implementati in una singola DLL. TAPI chiama solo le funzioni appropriate per il contesto in cui viene utilizzata la DLL.

Il provider di servizi di telefonia e la DLL dell'interfaccia utente devono essere entrambi progettati tenendo presente che le funzioni dell'interfaccia utente possono essere richiamate simultaneamente da più processi dell'applicazione. Devono inoltre tenere presente che l'applicazione e il servizio TAPI in cui è in esecuzione il provider di servizi di telefonia possono trovarsi in computer distinti in una LAN.

 

 
