---
title: Phone-Book voci
description: Telefono-book contengono le informazioni necessarie per stabilire una connessione RAS. Un utente o un amministratore può usare la Connessione remota finestra di dialogo per creare, modificare e comporre voci della rubrica telefonica.
ms.assetid: 971d7020-f9fd-42d1-97c3-79ad6eba6964
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea62595504229dd5dd920385a92214156a7d112774cb3fefbaff3f1b5edc7cbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789821"
---
# <a name="phone-book-entries"></a>Phone-Book voci

Telefono-book contengono le informazioni necessarie per stabilire una connessione RAS. Un utente o un amministratore può usare **la Connessione remota** finestra di dialogo per creare, modificare e comporre voci della rubrica telefonica.

A partire da Windows NT Server 4.0, il sistema supporta le funzioni descritte per Windows 95, nonché una serie di funzioni aggiuntive che un'applicazione può usare per lavorare con le rubriche telefoniche e le voci della rubrica telefonica.

La [**funzione RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) visualizza una finestra delle proprietà che consente all'utente di creare, modificare o copiare voci della rubrica telefonica. Le [**funzioni RasCreatePhonebookEntry**](/windows/desktop/api/Ras/nf-ras-rascreatephonebookentrya) [**e RasEditPhonebookEntry**](/windows/desktop/api/Ras/nf-ras-raseditphonebookentrya) chiamano la **funzione RasEntryDlg.** È possibile usare la [**funzione RasRenameEntry**](/windows/desktop/api/Ras/nf-ras-rasrenameentrya) per rinominare una voce della rubrica oppure [**RasDeleteEntry**](/windows/desktop/api/Ras/nf-ras-rasdeleteentrya) per eliminare una voce. [**RasValidateEntryName**](/windows/desktop/api/Ras/nf-ras-rasvalidateentrynamea) determina se una stringa specificata ha il formato corretto da usare come nome di voce.

È possibile usare [**RasGetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rasgetentrypropertiesa) e [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) per ottenere e impostare informazioni aggiuntive su una voce della rubrica telefonica. Queste funzioni usano una [**struttura RASENTRY.**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85))

Le [**funzioni RasGetCredentials**](/windows/desktop/api/Ras/nf-ras-rasgetcredentialsa) e [**RasSetCredentials**](/windows/desktop/api/Ras/nf-ras-rassetcredentialsa) ottengono e impostano le credenziali utente associate a una voce della rubrica TELEFONICA RAS specificata. Queste funzioni usano una [**struttura RASCREDENTIALS.**](/previous-versions/windows/desktop/legacy/aa376730(v=vs.85))

La [**funzione RasGetCountryInfo**](/windows/desktop/api/Ras/nf-ras-rasgetcountryinfoa) recupera le informazioni di composizione specifiche del paese/area geografica dall'Windows di telefonia dei paesi. **RasGetCountryInfo** usa la [**struttura RASCTRYINFO.**](/previous-versions/windows/desktop/legacy/aa376731(v=vs.85))

**Windows 95: ** Supporta un set limitato di funzioni per l'uso delle voci della rubrica telefonica. È possibile usare le [**funzioni RasCreatePhonebookEntry**](/windows/desktop/api/Ras/nf-ras-rascreatephonebookentrya) e [**RasEditPhonebookEntry**](/windows/desktop/api/Ras/nf-ras-raseditphonebookentrya) per creare o modificare una voce della rubrica telefonica. Queste funzioni visualizzano una finestra di dialogo in cui l'utente può specificare informazioni sulla voce della rubrica telefonica. È possibile usare le [**funzioni RasGetEntryDialParams**](/windows/desktop/api/Ras/nf-ras-rasgetentrydialparamsa) e [**RasSetEntryDialParams**](/windows/desktop/api/Ras/nf-ras-rassetentrydialparamsa) per impostare o recuperare i parametri di connessione per una voce della rubrica telefonica. La [**funzione RasEnumEntries**](/windows/desktop/api/Ras/nf-ras-rasenumentriesa) recupera una matrice di [**strutture RASENTRYNAME**](/previous-versions/windows/desktop/legacy/aa377267(v=vs.85)) che contengono i nomi delle voci della rubrica telefonica.

 

 