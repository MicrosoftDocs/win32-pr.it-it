---
description: Il file VBScript WiLstScr.vbs è disponibile in componenti sdk Windows per sviluppatori Windows programma di installazione. Questo script di esempio illustra il visualizzatore Windows di script del programma di installazione.
ms.assetid: 18989c16-e0c8-4d11-b915-730951b6845b
title: Visualizzare lo script del programma di installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4797d73c4c90266b94a02b9d73657fb95de75e153617ef1e34797f28035ee701
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117803982"
---
# <a name="view-installer-script"></a>Visualizzare lo script del programma di installazione

Il file VBScript WiLstScr.vbs è disponibile in componenti sdk Windows per [Windows programma di installazione](platform-sdk-components-for-windows-installer-developers.md). Questo script di esempio illustra il visualizzatore Windows di script del programma di installazione.

L'esempio illustra l'uso di:

-   [**Metodo OpenDatabase (oggetto Installer)**](installer-opendatabase.md)
-   [**Metodo LastErrorRecord**](installer-lasterrorrecord.md) [**dell'oggetto Installer**](installer-object.md)
-   [**Metodo OpenView**](database-openview.md) [**dell'oggetto Database**](database-object.md)
-   [**Metodo Fetch**](view-fetch.md) [**dell'oggetto View**](view-object.md)
-   [**Metodo FormatText**](record-formattext.md)
-   [**Proprietà FieldCount**](record-fieldcount.md)
-   [**Proprietà StringData**](record-stringdata.md) [**dell'oggetto Record**](record-object.md)
-   [\_Tabella TransformView](-transformview-table.md)

L'uso di questo esempio richiede CScript.exe versione di Windows Script Host. Per usare CScript.exe eseguire questo esempio, digitare un comando al prompt dei comandi usando la sintassi seguente. La Guida viene visualizzata se il primo argomento è /? o se vengono specificati troppi argomenti. Per reindirizzare l'output a un file, terminare la riga di comando con VBS > \[ *percorso del file* \] . L'esempio restituisce il valore 0 per l'esito positivo, 1 se viene richiamata la Guida e 2 se lo script ha esito negativo.

**Percorso WiLstScr.vbs** *\[ cscript per Windows script di \] esecuzione del programma di installazione*

Specificare il percorso dello script di esecuzione del programma di installazione.

Per altri esempi di scripting, vedere Windows [di scripting del programma di installazione](windows-installer-scripting-examples.md). Per utilità di esempio che non richiedono Windows Script Host, vedere Windows [Installer Development Tools](windows-installer-development-tools.md).

 

 



