---
description: Il file VBScript WiUseXfm.vbs è disponibile in componenti sdk Windows per Windows programma di installazione. Questo esempio illustra come usare lo script per applicare una trasformazione a un database Windows Installer.
ms.assetid: e647388e-5211-463d-9e3e-b502af01fc0c
title: Applicare una trasformazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 001737b1a08ea33ce233fa0aad90e96e23a1079f2c28f9d6308219cba270f6ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118381610"
---
# <a name="apply-a-transform"></a>Applicare una trasformazione

Il file VBScript WiUseXfm.vbs è disponibile in componenti sdk Windows [per sviluppatori Windows programma di installazione](platform-sdk-components-for-windows-installer-developers.md). Questo esempio illustra come usare lo script per applicare una trasformazione a un database Windows Installer.

L'esempio illustra l'uso di

-   [**Metodo OpenDatabase (oggetto Installer)**](installer-opendatabase.md)
-   [**Metodo LastErrorRecord**](installer-lasterrorrecord.md) [ **dell'oggetto Installer**](installer-object.md)
-   [**Metodo ApplyTransform**](database-applytransform.md)
-   [**Metodo Commit**](database-commit.md) [ **dell'oggetto Database**](database-object.md)

Per usare questo esempio è CScript.exe o WScript.exe'host script Windows script. Per usare CScript.exe questo esempio, digitare una riga di comando al prompt dei comandi usando la sintassi seguente. Se il primo argomento è /? viene visualizzata la Guida o se vengono specificati troppi argomenti. Per reindirizzare l'output a un file, terminare la riga di comando con vbs > \[ *percorso del file* \] . L'esempio restituisce il valore 0 per l'esito positivo, 1 se viene richiamata la Guida e 2 se lo script ha esito negativo.

**cscript WiUseXfm.vbs \[ percorso del database originale per trasformare le opzioni del \] \[ file \] \[\]**

Specificare il percorso del database Windows Installer. Specificare il percorso del file di trasformazione. Se il percorso del file di trasformazione viene omesso, i due database vengono confrontati solo. Il terzo argomento è un valore numerico facoltativo che specifica un set di condizioni di errore da eliminare. Aggiungere questi valori per eliminare più condizioni.



| Valore | Condizione di errore da eliminare                   |
|-------|-----------------------------------------------|
| 1     | Aggiunta di una riga già esistente.             |
| 2     | Eliminazione di una riga inesistente.           |
| 4     | Aggiunta di una tabella già esistente.           |
| 8     | Eliminazione di una tabella inesistente.         |
| 16    | Aggiornamento di una riga inesistente.           |
| 256   | Mancata corrispondenza delle tabelle codici di database e di trasformazione. |



 

Per altri esempi di scripting, vedere Windows [di scripting del programma di installazione](windows-installer-scripting-examples.md). Per utilità di esempio che non richiedono Windows Script Host, vedere Windows [Installer Development Tools](windows-installer-development-tools.md).

 

 



