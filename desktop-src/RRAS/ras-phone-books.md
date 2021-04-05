---
title: Libri telefonici RAS
description: Le rubriche telefoniche forniscono un modo standard per raccogliere e specificare le informazioni necessarie alla gestione connessione di accesso remoto per stabilire una connessione remota.
ms.assetid: db6d076c-c683-4e27-ace1-d2c0cd0931f6
keywords:
- Libri telefonici, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bbdfe7d2293f87e01fe33f3a078f861a35a732d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044813"
---
# <a name="ras-phone-books"></a>Libri telefonici RAS

Le rubriche telefoniche forniscono un modo standard per raccogliere e specificare le informazioni necessarie alla gestione connessione di accesso remoto per stabilire una connessione remota. Le rubriche telefoniche associano nomi di voce a informazioni quali numeri di telefono, porte COM e impostazioni del modem. Ogni voce del libro telefonico contiene le informazioni necessarie per stabilire una connessione RAS.

Le rubriche telefoniche sono archiviate in file di testo, ovvero file di testo contenenti i nomi di voce e informazioni associate. RAS crea un file di libro telefonico chiamato RASPHONE. PBK. L'utente può utilizzare la finestra di dialogo **connessione remota** principale per creare file personali della Rubrica. L'API RAS attualmente non fornisce supporto per la creazione di un file di libro telefonico. Alcune funzioni RAS, ad esempio la funzione [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) , hanno un parametro che specifica un file della rubrica telefonica. Se il chiamante non specifica un file della rubrica telefonica, la funzione utilizzerà il file predefinito della Rubrica, che è quello selezionato dall'utente nella finestra delle proprietà **Preferenze utente** della finestra di dialogo **connessione remota** .

Windows NT 4,0 fornisce le funzioni [**RasPhonebookDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasphonebookdlga) e [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) che visualizzano l'interfaccia utente RAS incorporata che consente agli utenti di utilizzare le rubriche telefoniche e le voci della Rubrica.

**Windows 95:** La rete remota archivia le voci del libro telefonico nel registro di sistema, anziché in un file di libro telefonico. Windows 95 non supporta i file o le funzioni personali della rubrica telefonica che visualizzano le finestre di dialogo RAS predefinite.

 

 




