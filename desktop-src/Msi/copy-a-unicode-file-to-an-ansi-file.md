---
description: Il file VBScript WiToAnsi.vbs viene fornito nei componenti Windows SDK per Windows Installer sviluppatori. In questo esempio viene illustrato come utilizzare lo script per riscrivere un file di testo Unicode come file di testo ANSI.
ms.assetid: cb22495f-968c-470a-a2f1-d0e068133956
title: Copiare un file Unicode in un file ANSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bde68c60eaa5a007aee7d2ca2d79159c9b7fce20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882737"
---
# <a name="copy-a-unicode-file-to-an-ansi-file"></a>Copiare un file Unicode in un file ANSI

Il file VBScript WiToAnsi.vbs viene fornito nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md). In questo esempio viene illustrato come utilizzare lo script per riscrivere un file di testo Unicode come file di testo ANSI.

Per usare questo esempio è necessaria la versione CScript.exe o WScript.exe di Windows script host. Per utilizzare CScript.exe per eseguire questo esempio, digitare una riga di comando al prompt dei comandi utilizzando la sintassi seguente. La guida viene visualizzata se il primo argomento è/? oppure se vengono specificati troppi argomenti. Per reindirizzare l'output a un file, terminare la riga di comando con VBS > \[ *percorso del file* \] . Nell'esempio viene restituito il valore 0 per l'esito positivo, 1 se la guida viene richiamata e 2 se lo script ha esito negativo.

**cscript WiToAnsi.vbs \[ percorso del file Unicode \] \[ al file ANSI\]**

Specificare il file di testo Unicode da convertire. Specificare il file di testo ANSI da creare. Se non viene specificato alcun file ANSI, il file Unicode viene sostituito.

Per altri esempi di script, vedere [Windows Installer esempi di scripting](windows-installer-scripting-examples.md). Per utilità di esempio che non richiedono Windows script host, vedere [Windows Installer strumenti di sviluppo](windows-installer-development-tools.md).

 

 



