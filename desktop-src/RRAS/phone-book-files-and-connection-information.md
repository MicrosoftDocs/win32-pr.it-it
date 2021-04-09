---
title: File di Phone-Book e informazioni di connessione
description: Una chiamata RasDial deve specificare le informazioni necessarie alla gestione connessione di accesso remoto per stabilire la connessione.
ms.assetid: bc3885a4-3c1e-47bc-b622-072b33ac3b51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11d352772eec057edd6ab8c9f53640c50ea0fc73
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118246"
---
# <a name="phone-book-files-and-connection-information"></a>File di Phone-Book e informazioni di connessione

Una chiamata [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) deve specificare le informazioni necessarie alla gestione connessione di accesso remoto per stabilire la connessione. In genere, la chiamata **RasDial** fornisce le informazioni di connessione specificando una voce della rubrica telefonica. Le informazioni di connessione in una voce della rubrica telefonica includono numeri di telefono, velocità di bps, [informazioni di autenticazione utente](user-authentication-information.md)e [altre informazioni di connessione](other-connection-information.md).

Un client RAS utilizza i parametri della funzione [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) per specificare un file della rubrica telefonica e una voce in tale file. Il parametro *lpszPhonebookPath* può specificare il nome di un file della rubrica telefonica oppure può essere **null** per indicare che deve essere usato il file predefinito della rubrica telefonica. Il parametro *lpRasDialParams* punta a una struttura [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) che specifica il nome della voce di Rubrica da usare.

Per visualizzare un elenco di voci della Rubrica da cui l'utente può selezionare una connessione, un client RAS può chiamare la funzione [**RasEnumEntries**](/windows/desktop/api/Ras/nf-ras-rasenumentriesa) per enumerare le voci in un file della rubrica telefonica.

Per stabilire una connessione senza usare una voce della rubrica telefonica, la chiamata [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) può specificare una stringa vuota per il membro **SzEntryName** della struttura [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) . Il membro **RASDIALPARAMS. szPhoneNumber** deve contenere il numero da chiamare. In questo caso, la gestione connessione di accesso remoto utilizza la prima porta modem disponibile e i valori predefiniti per tutte le altre impostazioni.

 

 