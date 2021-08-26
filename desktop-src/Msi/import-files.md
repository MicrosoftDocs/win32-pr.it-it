---
description: Il file VBScript WiImport.vbs disponibile in Windows SDK Components for Windows Installer Developers. Questo esempio illustra come scrivere uno script per importare tabelle in un database Windows Installer.
ms.assetid: 37580bd6-30c7-4239-9717-223a381ba021
title: Importare file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dc67cc3f698d1268a5ce08fe1e4c76b86a425216396fa168b0e8e6dc8a3f91f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043861"
---
# <a name="import-files"></a>Importare file

Il file VBScript WiImport.vbs in Windows [SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md). Questo esempio illustra come scrivere uno script per importare tabelle in un database Windows Installer.

Lo script si connette a un [**oggetto Installer,**](installer-object.md) apre un database, elabora un elenco di file ed esegue il commit delle modifiche prima di chiudere il database.

L'esempio illustra l'uso di:

-   [**Metodo OpenDatabase (oggetto Installer)**](installer-opendatabase.md)
-   [**Metodo LastErrorRecord**](installer-lasterrorrecord.md) [ **dell'oggetto Installer**](installer-object.md)
-   [**Metodo Import**](database-import.md)
-   [**Metodo Commit**](database-commit.md) [ **dell'oggetto Database**](database-object.md)

Per usare questo esempio, è CScript.exe o WScript.exe versione di Windows script host. Per usare CScript.exe eseguire questo esempio, usare la sintassi seguente al prompt dei comandi.

**cscript WiImport.vbs \[ percorso del database all'elenco di file di archivio delle opzioni \] \[ \] \[ \] \[ cartella**\]

La Guida viene visualizzata se il primo argomento è /? o se vengono specificati troppi argomenti. Per reindirizzare l'output a un file, terminare la riga di comando con VBS > \[ percorso del file \] . Nell'esempio viene restituito il valore 0 per l'esito positivo, 1 se viene richiamata la Guida e 2 se lo script non riesce.

Specificare il percorso di un Windows programma di installazione che deve essere creato o che deve ricevere le tabelle importate. Specificare il percorso della cartella contenente i file di archivio delle tabelle da importare. Elencare i nomi dei file di archivio da importare. I nomi di file con caratteri jolly, ad \* esempio idt, possono essere usati per importare più file.

Le opzioni seguenti possono essere specificate in qualsiasi punto della riga di comando prima dell'elenco di file.



| Opzione              | Descrizione                                                                                                                          |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| nessuna opzione specificata | Importare l'elenco dei file di archivio delle tabelle dalla cartella specificata nel database Windows Installer.                                |
| /C                  | Creare un database Windows Installer e quindi importare l'elenco dei file di archivio della tabella dalla cartella specificata nel nuovo database. |



 

Per altre informazioni, vedere Esempi [Windows di scripting del](windows-installer-scripting-examples.md) programma di installazione per altri esempi di scripting. Per le utilità di esempio che non richiedono Windows Script Host, vedere Windows [Installer Development Tools](windows-installer-development-tools.md).

Si noti che [un esempio di localizzazione illustra anche](a-localization-example.md) l'importazione di tabelle Error [localizzate e ActionText](importing-localized-error-and-actiontext-tables.md).

 

 



