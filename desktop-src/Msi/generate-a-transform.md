---
description: Il file VBScript WiGenXfm.vbs disponibile in Windows SDK Components for Windows Installer Developers. Questo script di esempio può generare una trasformazione da due database Windows Installer. Per altre informazioni, vedere Trasformazioni di database.
ms.assetid: bfa918b8-8d90-4e14-8a06-6c3d5b5dc13b
title: Generare una trasformazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba16c894ec32bf300f1572eb26311be70315872b9711ca46573ce65e18802308
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142768"
---
# <a name="generate-a-transform"></a>Generare una trasformazione

Il file VBScript WiGenXfm.vbs in Windows [SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md). Questo script di esempio può generare una trasformazione da due database Windows Installer. Per altre informazioni, vedere [Trasformazioni di database.](database-transforms.md)

L'esempio illustra l'uso di:

[**Metodo OpenDatabase (oggetto Installer)**](installer-opendatabase.md)

[**Metodo LastErrorRecord**](installer-lasterrorrecord.md) [ **dell'oggetto Installer**](installer-object.md)

[**Metodo GenerateTransform**](database-generatetransform.md) [ **dell'oggetto Database**](database-object.md)

Per usare questo esempio, è CScript.exe o WScript.exe versione di Windows script host. Per usare CScript.exe eseguire questo esempio, digitare una riga di comando al prompt dei comandi usando la sintassi seguente. La Guida viene visualizzata se il primo argomento è /? o se vengono specificati troppi argomenti. Per reindirizzare l'output a un file, terminare la riga di comando con vbs > \[ *percorso del file* \] . Nell'esempio viene restituito il valore 0 per l'esito positivo, 1 se viene richiamata la Guida e 2 se lo script non riesce.

**cscript WiGenXfm.vbs \[ percorso del database \] \[ originale al percorso del database \] \[ modificato per trasformare il file\]**

Specificare il percorso del database Windows Installer. Specificare il percorso del database modificato. Specificare il percorso del file di trasformazione da creare. Se il percorso del file di trasformazione viene omesso, vengono confrontati solo i due database.

Per altri esempi di scripting, vedere Windows [di script del programma di installazione](windows-installer-scripting-examples.md). Per le utilità di esempio che non richiedono Windows Script Host, vedere Windows [Installer Development Tools](windows-installer-development-tools.md).

Si noti che [in un esempio di localizzazione](a-localization-example.md) viene [illustrata la generazione di una trasformazione di personalizzazione.](generating-a-customization-transform.md)

 

 



