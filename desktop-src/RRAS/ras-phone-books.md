---
title: Documentazione Telefono RAS
description: Telefono libri offrono un modo standard per raccogliere e specificare le informazioni necessarie per stabilire una connessione remota Gestione connessioni accesso remoto.
ms.assetid: db6d076c-c683-4e27-ace1-d2c0cd0931f6
keywords:
- Telefono libri, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba80b11696df220a904a13685855818b945794c17b9bd4233e9f897592ee7b7d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868421"
---
# <a name="ras-phone-books"></a>Documentazione Telefono RAS

Telefono libri offrono un modo standard per raccogliere e specificare le informazioni necessarie per stabilire una connessione remota Gestione connessioni accesso remoto. Telefono i nomi delle voci vengono associati a informazioni quali numeri di telefono, porte COM e impostazioni del modem. Ogni voce della rubrica contiene le informazioni necessarie per stabilire una connessione RAS.

Telefono libri vengono archiviati in file di rubrica telefonica, ovvero file di testo che contengono i nomi delle voci e le informazioni associate. RAS crea un file di rubrica denominato RASPHONE. PBK. L'utente può usare la finestra di **Connessione remota** finestra di dialogo principale per creare file di rubrica telefonica personali. L'API RAS non fornisce attualmente il supporto per la creazione di un file della rubrica telefonica. Alcune funzioni RAS, ad esempio [**la funzione RasDial,**](/windows/desktop/api/Ras/nf-ras-rasdiala) hanno un parametro che specifica un file della rubrica telefonica. Se il chiamante non specifica un file della rubrica telefonica, la funzione usa il file  predefinito della rubrica,  ovvero quello selezionato dall'utente nella finestra delle proprietà Preferenze utente della finestra di dialogo Connessione remota.

Windows NT 4.0 fornisce le funzioni [**RasPhonebookDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasphonebookdlga) e [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) che visualizzano l'interfaccia utente RAS predefinita che consente agli utenti di usare le rubriche telefoniche e le voci della rubrica telefonica.

**Windows 95:** La connessione remota archivia le voci della rubrica telefonica nel Registro di sistema anziché in un file della rubrica telefonica. Windows 95 non supporta i file o le funzioni personali della rubrica telefonica che visualizzano le finestre di dialogo RAS incorporate.

 

 




