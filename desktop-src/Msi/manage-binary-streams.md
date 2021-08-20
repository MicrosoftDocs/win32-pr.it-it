---
description: Il file VBScript WiStream.vbs è disponibile in componenti sdk Windows per Windows programma di installazione.
ms.assetid: f96d1fdd-81c8-4fb2-a23e-fda49ace8bef
title: Gestire le Flussi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32de268cc42a6dbb806d6f3c1503d8bb0cdf32aba037bf48da678ecb86fe2775
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118945626"
---
# <a name="manage-binary-streams"></a>Gestire le Flussi

Il file VBScript WiStream.vbs è disponibile in componenti sdk Windows [per Windows programma di installazione](platform-sdk-components-for-windows-installer-developers.md). Questo esempio illustra come usare lo script per gestire i flussi binari in un database Windows Installer. L'esempio può essere usato per immettere file cab compressi in un database. Questo esempio illustra il funzionamento della tabella [ \_ Flussi nel](-streams-table.md) database Windows Installer.

L'esempio illustra anche l'uso di:

-   [**Metodo OpenDatabase (oggetto Installer)**](installer-opendatabase.md)
-   [**Metodo CreateRecord**](installer-createrecord.md)
-   [**Metodo LastErrorRecord**](installer-lasterrorrecord.md) [ **dell'oggetto Installer**](installer-object.md)
-   [**Metodo OpenView**](database-openview.md)
-   [**Metodo Commit**](database-commit.md) [ **dell'oggetto Database**](database-object.md)
-   [**Metodo Fetch**](view-fetch.md)
-   [**Metodo Modify**](view-modify.md)
-   [**Metodo Execute**](view-execute.md) [ **dell'oggetto View**](view-object.md)
-   [**StringData - proprietà**](record-stringdata.md)
-   [**Metodo SetStream**](record-setstream.md) [ **dell'oggetto Record**](record-object.md)

Per usare questo esempio è CScript.exe o WScript.exe'host di script Windows. Per usare CScript.exe questo esempio, digitare una riga di comando al prompt dei comandi usando la sintassi seguente. Se il primo argomento è /? viene visualizzata la Guida o se vengono specificati troppi argomenti. Per reindirizzare l'output a un file, terminare la riga di comando con VBS > \[ *percorso del file* \] . L'esempio restituisce il valore 0 per l'esito positivo, 1 se viene richiamata la Guida e 2 se lo script ha esito negativo.

**cscript WiStream.vbs \[ percorso del database \] \[ al nome del flusso \] \[ delle opzioni \] \[ file\]**

Specificare il percorso del Windows installer che deve ricevere il flusso. Specificare un percorso del file binario contenente i dati del flusso. Per elencare i flussi nel database del programma di installazione, omettere questo percorso. È possibile specificare un nome di flusso facoltativo, se omesso, per impostazione predefinita viene utilizzato il nome del file.

È possibile che venga specificata l'opzione seguente.



| Opzione              | Descrizione                                                                                     |
|---------------------|-------------------------------------------------------------------------------------------------|
| nessuna opzione specificata | Aggiungere un flusso al database Windows Installer.                                                 |
| /d                  | Rimuovere un flusso. Questo flag di opzione deve essere seguito dal nome dell'archiviazione secondaria da rimuovere. |



 

Per altri esempi di scripting, vedere Windows [di scripting del programma di installazione](windows-installer-scripting-examples.md). Per utilità di esempio che non richiedono Windows Script Host, vedere Windows [Installer Development Tools](windows-installer-development-tools.md).

 

 



