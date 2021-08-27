---
description: Il file VBScript WiLstXfm.vbs è disponibile in componenti sdk Windows per sviluppatori Windows programma di installazione. Questo esempio di script può essere usato per visualizzare un file di trasformazione.
ms.assetid: c2e3dd56-b0e5-481a-b7b8-5000fa686850
title: Visualizzare una trasformazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f599099ff858275f3b0c75df9b265129adfe0659a5c3c35d285417a8e295f58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995631"
---
# <a name="view-a-transform"></a>Visualizzare una trasformazione

Il file VBScript WiLstXfm.vbs è disponibile in componenti sdk Windows per [Windows programma di installazione](platform-sdk-components-for-windows-installer-developers.md). Questo esempio di script può essere usato per visualizzare un file di trasformazione.

L'esempio illustra l'uso di:

-   [\_Tabella TransformView](-transformview-table.md)
-   [**Metodo OpenDatabase (oggetto Installer)**](installer-opendatabase.md)
-   [**Metodo LastErrorRecord**](installer-lasterrorrecord.md) [ **dell'oggetto Installer**](installer-object.md)
-   [**Metodo ApplyTransform**](database-applytransform.md)
-   [**Metodo OpenView**](database-openview.md)
-   [**Metodo Commit**](database-commit.md) [ **dell'oggetto Database**](database-object.md)
-   [**Proprietà IsNull**](record-isnull.md)
-   [**Proprietà StringData**](record-stringdata.md) [ **dell'oggetto Record**](record-object.md)

L'uso di questo esempio richiede CScript.exe versione di Windows Script Host. Per usare CScript.exe eseguire questo esempio, digitare un comando al prompt dei comandi usando la sintassi seguente. La Guida viene visualizzata se il primo argomento è /? o se vengono specificati troppi argomenti. Per reindirizzare l'output a un file, terminare la riga di comando con VBS > \[ *percorso del file* \] . L'esempio restituisce il valore 0 per l'esito positivo, 1 se viene richiamata la Guida e 2 se lo script ha esito negativo.

**cscript WiLstXfm.vbs** *\[ percorso dell'opzione di database \] \[ di riferimento da trasformare \] \[ da visualizzare \]*

Specificare il percorso del database di Windows Installer. Specificare un elenco di percorsi per trasformare i file visualizzati. Ogni percorso nell'elenco può essere preceduto da un valore numerico facoltativo. Questo valore specifica un set di condizioni di errore che devono essere soppresse. È possibile aggiungere questi valori insieme per eliminare più condizioni. Se non viene specificata alcuna opzione numerica, tutte le condizioni di errore vengono soppresse. Gli argomenti in questo elenco vengono eseguiti nell'ordine da sinistra a destra in cui vengono visualizzati nella riga di comando.



| Valore | Condizione di errore da eliminare                   |
|-------|-----------------------------------------------|
| 1     | Aggiunta di una riga già esistente.             |
| 2     | Eliminazione di una riga inesistente.           |
| 4     | Aggiunta di una tabella già esistente.           |
| 8     | Eliminazione di una tabella inesistente.         |
| 16    | Aggiornamento di una riga inesistente.           |
| 256   | Mancata corrispondenza delle tabelle codici di database e di trasformazione. |



 

Per altri esempi di scripting, vedere Windows [di scripting del programma di installazione](windows-installer-scripting-examples.md). Per utilità di esempio che non richiedono Windows Script Host, vedere Windows [Installer Development Tools](windows-installer-development-tools.md).

 

 



