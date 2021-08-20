---
description: Il file VBScript WiToAnsi.vbs è disponibile in componenti sdk Windows per sviluppatori Windows programma di installazione. Questo esempio illustra come viene usato lo script per riscrivere un file di testo Unicode come file di testo ANSI.
ms.assetid: cb22495f-968c-470a-a2f1-d0e068133956
title: Copiare un file Unicode in un file ANSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 224a9115da67848bd43aaceb7e5d8f529693558191e52a04de2e7645a4e60aeb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118143375"
---
# <a name="copy-a-unicode-file-to-an-ansi-file"></a>Copiare un file Unicode in un file ANSI

Il file VBScript WiToAnsi.vbs è disponibile in componenti sdk Windows per [Windows programma di installazione](platform-sdk-components-for-windows-installer-developers.md). Questo esempio illustra come viene usato lo script per riscrivere un file di testo Unicode come file di testo ANSI.

L'uso di questo esempio richiede CScript.exe o WScript.exe versione di Windows Script Host. Per usare CScript.exe questo esempio, digitare una riga di comando al prompt dei comandi usando la sintassi seguente. La Guida viene visualizzata se il primo argomento è /? o se vengono specificati troppi argomenti. Per reindirizzare l'output a un file, terminare la riga di comando con VBS > \[ *percorso del file* \] . L'esempio restituisce il valore 0 per l'esito positivo, 1 se viene richiamata la Guida e 2 se lo script ha esito negativo.

**cscript WiToAnsi.vbs \[ percorso del file Unicode al file \] \[ ANSI\]**

Specificare il file di testo Unicode da convertire. Specificare il file di testo ANSI che viene creato. Se non viene specificato alcun file ANSI, il file Unicode viene sostituito.

Per altri esempi di scripting, vedere Windows [di scripting del programma di installazione](windows-installer-scripting-examples.md). Per utilità di esempio che non richiedono Windows Script Host, [vedere Windows Installer Development Tools](windows-installer-development-tools.md).

 

 



