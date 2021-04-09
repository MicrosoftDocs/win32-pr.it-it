---
title: Finestre di dialogo comuni RAS
description: Windows fornisce un set di funzioni che consentono di visualizzare le finestre di dialogo RAS fornite dal sistema.
ms.assetid: 8231511a-7339-4fbb-8a39-f643ac575856
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3032da8b0647b48941d85fc4f085ddb8ced0125f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118343"
---
# <a name="ras-common-dialog-boxes"></a>Finestre di dialogo comuni RAS

Windows fornisce un set di funzioni che consentono di visualizzare le finestre di dialogo RAS fornite dal sistema. Queste funzioni semplificano la visualizzazione di un'interfaccia utente familiare da parte delle applicazioni, in modo che gli utenti possano eseguire attività RAS. Ad esempio, gli utenti possono stabilire e monitorare le connessioni o utilizzare le voci della rubrica telefonica. Windows 95 attualmente non supporta queste funzioni.

La funzione [**RasPhonebookDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasphonebookdlga) Visualizza la finestra di dialogo **rete remota** principale. Da questa finestra di dialogo l'utente può comporre, modificare o eliminare una voce di rubrica selezionata, creare una nuova voce del telefono o specificare le preferenze dell'utente. La funzione **RasPhonebookDlg** usa la struttura [**RASPBDLG**](/previous-versions/windows/desktop/legacy/aa377607(v=vs.85)) per specificare parametri di input e output aggiuntivi. È possibile, ad esempio, impostare i membri della struttura per controllare la posizione della finestra di dialogo sullo schermo. È possibile utilizzare la struttura **RASPBDLG** per specificare una funzione di callback [**RasPBDlgFunc**](/windows/desktop/api/Rasdlg/nc-rasdlg-raspbdlgfunca) che riceve le notifiche dell'attività utente mentre la finestra di dialogo è aperta. Ad esempio, RAS chiama la funzione **RasPBDlgFunc** se l'utente compone, modifica, crea o Elimina una voce della rubrica telefonica.

È possibile utilizzare la funzione [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga) per avviare un'operazione di connessione RAS senza visualizzare la finestra di dialogo **rete remota** principale. Con **RasDialDlg** è possibile specificare un numero di telefono o una voce di telefono da chiamare. La funzione Visualizza un flusso di finestre di dialogo che indicano lo stato dell'operazione di connessione. La funzione **RasDialDlg** usa una struttura [**RasDialDlg**](/previous-versions/windows/desktop/legacy/aa377023(v=vs.85)) per specificare parametri di input e output aggiuntivi, ad esempio la posizione della finestra di dialogo e la sottovoce del libro telefonico da chiamare.

Per visualizzare la finestra delle proprietà di **rete remota** , chiamare la funzione [**RasMonitorDlg**](/previous-versions/windows/desktop/legacy/aa377584(v=vs.85)) . Questa finestra di dialogo consente all'utente di monitorare lo stato delle connessioni esistenti. La funzione **RasMonitorDlg** usa una struttura [**RasMonitorDlg**](/previous-versions/windows/desktop/legacy/aa377591(v=vs.85)) per specificare parametri di input e output aggiuntivi, ad esempio la posizione della finestra di dialogo e la pagina della finestra delle proprietà da visualizzare nella parte superiore.

È possibile chiamare la funzione [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) per visualizzare una finestra delle proprietà per la creazione, la modifica o la copia di una voce della rubrica telefonica. La funzione **RasEntryDlg** usa una struttura [**RasEntryDlg**](/previous-versions/windows/desktop/legacy/aa377260(v=vs.85)) per specificare parametri di input e output aggiuntivi, ad esempio la posizione della finestra di dialogo e il tipo di operazione della rubrica telefonica.

 

 