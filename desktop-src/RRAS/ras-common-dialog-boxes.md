---
title: Finestre di dialogo comuni RAS
description: Windows fornisce un set di funzioni che visualizzano le finestre di dialogo RAS fornite dal sistema.
ms.assetid: 8231511a-7339-4fbb-8a39-f643ac575856
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be93db8e8d1819abe56d98bb293a7b6b027089be0648b00f7848d5204e911ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909721"
---
# <a name="ras-common-dialog-boxes"></a>Finestre di dialogo comuni RAS

Windows fornisce un set di funzioni che visualizzano le finestre di dialogo RAS fornite dal sistema. Queste funzioni semplificano la visualizzazione di un'interfaccia utente familiare per consentire agli utenti di eseguire attività RAS. Ad esempio, gli utenti possono stabilire e monitorare le connessioni o usare le voci della rubrica. Windows 95 non supporta attualmente queste funzioni.

La [**funzione RasPhonebookDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasphonebookdlga) visualizza la finestra di **Connessione remota** principale. Da questa finestra di dialogo l'utente può comporre, modificare o eliminare una voce della rubrica selezionata, creare una nuova voce della rubrica telefonica o specificare le preferenze dell'utente. La **funzione RasPhonebookDlg** usa la [**struttura RASPBDLG**](/previous-versions/windows/desktop/legacy/aa377607(v=vs.85)) per specificare parametri di input e output aggiuntivi. Ad esempio, è possibile impostare i membri della struttura per controllare la posizione della finestra di dialogo sullo schermo. È possibile usare la **struttura RASPBDLG** per specificare una funzione di callback [**RasPBDlgFunc**](/windows/desktop/api/Rasdlg/nc-rasdlg-raspbdlgfunca) che riceve le notifiche dell'attività dell'utente mentre la finestra di dialogo è aperta. Ras, ad esempio, chiama la funzione **RasPBDlgFunc** se l'utente chiama, modifica, crea o elimina una voce della rubrica.

È possibile usare la [**funzione RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga) per avviare un'operazione di connessione RAS senza visualizzare la finestra di **Connessione remota** principale. Con **RasDialDlg** è possibile specificare un numero di telefono o una voce della rubrica da chiamare. La funzione visualizza un flusso di finestre di dialogo che indicano lo stato dell'operazione di connessione. La **funzione RasDialDlg** usa una struttura [**RASDIALDLG**](/previous-versions/windows/desktop/legacy/aa377023(v=vs.85)) per specificare parametri di input e output aggiuntivi, ad esempio la posizione della finestra di dialogo e la voce secondaria della rubrica da chiamare.

Per visualizzare la **Connessione remota** delle proprietà, chiamare la [**funzione RasMonitorDlg.**](/previous-versions/windows/desktop/legacy/aa377584(v=vs.85)) Questa finestra di dialogo consente all'utente di monitorare lo stato delle connessioni esistenti. La **funzione RasMonitorDlg** usa una struttura [**RASMONITORDLG**](/previous-versions/windows/desktop/legacy/aa377591(v=vs.85)) per specificare parametri di input e output aggiuntivi, ad esempio la posizione della finestra di dialogo e la pagina della finestra delle proprietà da visualizzare in alto.

È possibile chiamare la [**funzione RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) per visualizzare una finestra delle proprietà per la creazione, la modifica o la copia di una voce della rubrica. La **funzione RasEntryDlg** usa una struttura [**RASENTRYDLG**](/previous-versions/windows/desktop/legacy/aa377260(v=vs.85)) per specificare parametri di input e output aggiuntivi, ad esempio la posizione della finestra di dialogo e il tipo di operazione di rubrica.

 

 