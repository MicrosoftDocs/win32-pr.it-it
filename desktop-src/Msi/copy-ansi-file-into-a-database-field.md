---
description: Il file di esempio di codice VBScript WiTextIn.vbs viene fornito nei componenti Windows SDK per Windows Installer sviluppatori.
ms.assetid: ba6c6367-ebb1-4981-ae3a-bcff68aacdbf
title: Copia il file ANSI in un campo di database
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73dc6c4d3a945177581a35bf6b19d89855abb5ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313816"
---
# <a name="copy-ansi-file-into-a-database-field"></a>Copia il file ANSI in un campo di database

Il file di esempio di codice VBScript WiTextIn.vbs viene fornito nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md). Nell'esempio viene illustrato come è possibile utilizzare uno script per copiare un file in un campo di testo di un database di Windows Installer e viene illustrata l'elaborazione dei dati della chiave primaria.

L'esempio di codice mostra anche quanto segue:

-   [**Metodo OpenDatabase (oggetto Installer)**](installer-opendatabase.md) e [**Metodo LastErrorRecord**](installer-lasterrorrecord.md) dell' [**oggetto Installer**](installer-object.md)
-   [**Metodo OpenView**](database-openview.md), [**metodo commit**](database-commit.md)e [**Proprietà PrimaryKeys**](database-primarykeys.md) dell' [**oggetto di database**](database-object.md)
-   [**Metodo fetch**](view-fetch.md) e [**metodo modify**](view-modify.md) dell' [**oggetto View**](view-object.md)
-   [**Proprietà StringData**](record-stringdata.md) e [**Metodo ReadStream**](record-readstream.md) dell' [**oggetto record**](record-object.md)

Per utilizzare l'esempio di codice è necessario disporre della versione CScript.exe o WScript.exe di Windows script host.

**Per utilizzare CScript.exe per eseguire l'esempio**

-   Al prompt dei comandi digitare la sintassi seguente:

    **cscript WiTextIn.vbs \[ percorso del nome della tabella del database \] \[ nome della \] \[ colonna valori di chiave primaria \] \[ percorso del \] \[ file\]**

> [!Note]  
> La guida viene visualizzata se il primo argomento è/? oppure se vengono specificati troppi argomenti.

 

**Per reindirizzare l'output a un file**

-   Terminare la riga di comando con il seguente **> il \[ percorso del file vbs \] . T**

> [!Note]  
> L'esempio restituisce un valore pari a 0 (zero) per esito positivo, 1 (uno) se la guida viene richiamata e 2 (due) se lo script non riesce.

 

L'elenco seguente identifica gli elementi che è necessario specificare:

-   Consente di specificare il percorso del database di Windows Installer.
-   Consente di specificare il nome della tabella di database.
-   Specificare tutti i valori di chiave primaria per la riga, nell'ordine e concatenati con i due punti.
-   Specificare un nome di colonna che non sia una colonna chiave. Si tratta della colonna a cui si desidera ricevere i dati.
-   Specificare il percorso del file di testo da copiare.

> [!Note]  
> Se l'ultimo argomento viene omesso, viene visualizzato il valore corrente nel campo.

 

Per altri esempi di script, vedere [Windows Installer esempi di scripting](windows-installer-scripting-examples.md). Per utilità di esempio che non richiedono Windows script host, vedere [Windows Installer strumenti di sviluppo](windows-installer-development-tools.md).

 

 



