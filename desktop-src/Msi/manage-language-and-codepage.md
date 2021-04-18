---
description: Il file VBScript WiLangID.vbs viene fornito nei componenti Windows SDK per Windows Installer sviluppatori.
ms.assetid: 319e9ffd-ff9f-4b4c-913e-2c571f2ec9ee
title: Gestisci lingua e tabella codici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cbfb96f04d75ed79f32c8a49fe58b8dcc86f184
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318279"
---
# <a name="manage-language-and-codepage"></a>Gestisci lingua e tabella codici

Il file VBScript WiLangID.vbs viene fornito nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md). In questo esempio viene illustrato come utilizzare lo script per accedere alle informazioni sulla lingua e alla tabella codici di un pacchetto. Per ulteriori informazioni, vedere la pagina relativa alla [localizzazione di un pacchetto di Windows Installer](localizing-a-windows-installer-package.md) e alla [gestione della tabella codici (Windows Installer)](code-page-handling-windows-installer-.md).

Nell'esempio viene illustrato l'utilizzo di:

-   [**Metodo OpenDatabase (oggetto Installer)**](installer-opendatabase.md)
-   [**Metodo CreaRecord**](installer-createrecord.md)
-   [**Metodo LastErrorRecord**](installer-lasterrorrecord.md) dell' [ **oggetto Installer**](installer-object.md)
-   [**OpenView (metodo)**](database-openview.md)
-   [**Proprietà SummaryInformation (oggetto di database)**](database-summaryinformation.md) dell' [ **oggetto di database**](database-object.md)

Per usare questo esempio è necessaria la versione CScript.exe o WScript.exe di Windows script host. Per utilizzare CScript.exe per eseguire questo esempio, digitare un comando al prompt dei comandi utilizzando la sintassi seguente. La guida viene visualizzata se il primo argomento è/? oppure se vengono specificati troppi argomenti. Per reindirizzare l'output a un file, terminare la riga di comando con VBS > \[ *percorso del file* \] . Nell'esempio viene restituito il valore 0 per l'esito positivo, 1 se la guida viene richiamata e 2 se lo script ha esito negativo.

**valore della \[ \] \[ parola chiave database \] cscript WiLangID.vbs Path \[\]**

Consente di specificare il percorso del database di Windows Installer. Per modificare un valore, specificare una delle parole chiave seguenti seguite dal nuovo valore. Se non viene specificato alcun valore, l'esempio restituisce il valore corrente.



| Parola chiave      | Descrizione                                                                                                                                                                                |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Pacchetto**  | Versioni del linguaggio supportate dal database. Per informazioni, vedere Proprietà di [**Riepilogo del modello**](template-summary.md) .                                                               |
| **Prodotto**  | Lingua che il programma di installazione deve usare per le stringhe nell'interfaccia utente che non sono state create nel database. Per informazioni, vedere proprietà [**ProductLanguage**](productlanguage.md) . |
| **Codepage** | Tabella codici ANSI singola per il pool di stringhe. Per informazioni, vedere la pagina relativa alla [gestione della tabella codici (Windows Installer)](code-page-handling-windows-installer-.md).                                       |



 

Per altri esempi di script, vedere [Windows Installer esempi di scripting](windows-installer-scripting-examples.md). Per utilità di esempio che non richiedono Windows script host, vedere [Windows Installer strumenti di sviluppo](windows-installer-development-tools.md).

Per ulteriori informazioni, vedere la pagina relativa alla [determinazione della tabella codici](determining-an-installation-database-s-code-page.md) di un database di installazione e [l'impostazione della tabella codici di un database](setting-the-code-page-of-a-database.md).

 

 



