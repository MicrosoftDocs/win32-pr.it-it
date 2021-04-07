---
description: Il file VBScript WiUseXfm.vbs viene fornito nei componenti Windows SDK per Windows Installer sviluppatori. In questo esempio viene illustrato come utilizzare lo script per applicare una trasformazione a un database Windows Installer.
ms.assetid: e647388e-5211-463d-9e3e-b502af01fc0c
title: Applicare una trasformazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9e86acc495fc2a0bb8dff562832e58d29483256
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881130"
---
# <a name="apply-a-transform"></a>Applicare una trasformazione

Il file VBScript WiUseXfm.vbs viene fornito nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md). In questo esempio viene illustrato come utilizzare lo script per applicare una trasformazione a un database Windows Installer.

Nell'esempio viene illustrato l'utilizzo di

-   [**Metodo OpenDatabase (oggetto Installer)**](installer-opendatabase.md)
-   [**Metodo LastErrorRecord**](installer-lasterrorrecord.md) dell' [ **oggetto Installer**](installer-object.md)
-   [**Metodo ApplyTransform**](database-applytransform.md)
-   [**Metodo commit**](database-commit.md) dell' [ **oggetto di database**](database-object.md)

Per usare questo esempio, è necessaria la versione CScript.exe o WScript.exe di Windows script host. Per utilizzare CScript.exe per eseguire questo esempio, digitare una riga di comando al prompt dei comandi utilizzando la sintassi seguente. La guida viene visualizzata se il primo argomento è/? oppure se vengono specificati troppi argomenti. Per reindirizzare l'output a un file, terminare la riga di comando con VBS > \[ *percorso del file* \] . Nell'esempio viene restituito il valore 0 per l'esito positivo, 1 se la guida viene richiamata e 2 se lo script ha esito negativo.

**cscript WiUseXfm.vbs \[ percorso al percorso del database originale \] \[ per le \] Opzioni del file di trasformazione \[\]**

Consente di specificare il percorso del database di Windows Installer. Consente di specificare il percorso del file di trasformazione. Se il percorso del file di trasformazione viene omesso, vengono confrontati solo i due database. Il terzo argomento è un valore numerico facoltativo che specifica un set di condizioni di errore che devono essere eliminati. Aggiungere questi valori insieme per escludere più condizioni.



| Valore | Condizione di errore da disattivare                   |
|-------|-----------------------------------------------|
| 1     | Aggiunta di una riga già esistente.             |
| 2     | Eliminazione di una riga inesistente.           |
| 4     | Aggiunta di una tabella già esistente.           |
| 8     | Eliminazione di una tabella inesistente.         |
| 16    | Aggiornamento di una riga inesistente.           |
| 256   | Mancata corrispondenza delle tabelle codici del database e della trasformazione. |



 

Per altri esempi di script, vedere [Windows Installer esempi di scripting](windows-installer-scripting-examples.md). Per utilità di esempio che non richiedono Windows script host, vedere [Windows Installer strumenti di sviluppo](windows-installer-development-tools.md).

 

 



