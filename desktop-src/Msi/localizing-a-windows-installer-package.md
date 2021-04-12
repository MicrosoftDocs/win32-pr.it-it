---
description: Per informazioni generali sulla localizzazione, vedere Servizi di globalizzazione.
ms.assetid: 734961f6-de0a-4c54-9866-ade994c41c7e
title: Localizzazione di un pacchetto di Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b325b211302fba632f454f30eefbcb688f30d819
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129682"
---
# <a name="localizing-a-windows-installer-package"></a>Localizzazione di un pacchetto di Windows Installer

Per informazioni generali sulla localizzazione, vedere [servizi di globalizzazione](../intl/globalization-services.md). Per la localizzazione di un pacchetto di Windows Installer è necessario modificare le stringhe visualizzate dall'interfaccia utente e potrebbe essere necessario aggiungere o modificare le risorse del prodotto. Ad esempio, la localizzazione può includere l'aggiunta di dll internazionali e file localizzati al prodotto.

**Per localizzare un pacchetto di Windows Installer**

1.  Prepararsi alla localizzazione durante la creazione del pacchetto di installazione originale. Progettare il layout dei file localizzati in modo che le versioni in lingue diverse possano coesistere se installate nel computer dell'utente. Organizzare i file che richiedono la localizzazione in componenti separati e installare questi file in directory separate. Creare un database di installazione di base che disponga di una pagina di controllo neutra. Vedere [preparazione di un pacchetto di Windows Installer per la localizzazione](preparing-a-windows-installer-package-for-localization.md).
2.  Impostare sempre la tabella codici del database da localizzare prima di aggiungere i dati localizzati. Se la tabella codici del database da localizzare è neutra, vedere [impostazione della tabella codici di un database](setting-the-code-page-of-a-database.md). Per determinare la tabella codici, vedere la pagina relativa alla [determinazione della tabella codici di un database di installazione](determining-an-installation-database-s-code-page.md).
3.  Importare una [tabella degli errori](error-table.md) localizzata e una [tabella ActionText](actiontext-table.md) nel database. Per ulteriori informazioni, vedere la pagina relativa [alla localizzazione delle tabelle Error e ActionText](localizing-the-error-and-actiontext-tables.md) per un elenco di lingue supportate da Microsoft Windows Software Development Kit (SDK). È possibile importare queste tabelle usando Msidb.exe o [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).
4.  Modificare le altre colonne localizzabili del database utilizzando un editor di tabella o le query SQL. Per le funzioni di accesso SQL, vedere [utilizzo delle query](working-with-queries.md). Gli argomenti per le tabelle di database identificano le colonne di database che è possibile localizzare. Per ulteriori informazioni, vedere l'elenco di tabelle in [tabelle di database](database-tables.md).
5.  Impostare la proprietà [**ProductLanguage**](productlanguage.md) nella [tabella delle proprietà](property-table.md) su LangID del database. Quando si crea un pacchetto come indipendente dalla lingua, impostare la proprietà ProductLanguage su 0 e usare il tipo di carattere MS Shell Dlg come stile di testo per tutte le finestre di dialogo Create. Poiché alcuni tipi di carattere non supportano tutti i set di caratteri, è possibile verificare che il testo venga visualizzato correttamente in tutte le versioni localizzate del sistema operativo utilizzando questo tipo di carattere.
6.  Impostare il campo lingua della proprietà [**Riepilogo modello**](template-summary.md) in modo da riflettere il LangID del database.
7.  Se le stringhe di testo nel [flusso di informazioni di riepilogo](summary-information-stream.md) sono localizzate, impostare la proprietà [**Riepilogo codepage**](codepage-summary.md) sulla tabella codici.
8.  Impostare la proprietà [**ProductCode**](productcode.md) nella [tabella delle proprietà](property-table.md) e impostare il codice del pacchetto nella proprietà [**Riepilogo numero revisione**](revision-number-summary.md) su un nuovo codice del pacchetto. Un prodotto localizzato è considerato un prodotto diverso. Ad esempio, le versioni tedesche e in inglese di un'applicazione sono considerate due prodotti diversi e devono avere codici prodotto diversi.
9.  La localizzazione può richiedere la modifica delle risorse già esistenti o l'aggiunta di nuove risorse, ad esempio file o chiavi del registro di sistema. Verificare che il codice del componente venga modificato per ogni componente esistente in cui è stata aggiunta una nuova risorsa. Altre modifiche possono richiedere anche modifiche al codice di un componente. Per ulteriori informazioni, vedere [modifica del codice componente](changing-the-component-code.md).
10. Assicurarsi di salvare la localizzazione e altre modifiche apportate al database salvando il pacchetto con lo strumento di modifica o chiamando [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit).

Per ulteriori informazioni, vedere [un esempio di localizzazione](a-localization-example.md).

 

 
