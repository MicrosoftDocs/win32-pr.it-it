---
description: Il file VBScript WiGenXfm.vbs viene fornito nei componenti Windows SDK per Windows Installer sviluppatori. Questo script di esempio può generare una trasformazione da due database Windows Installer. Per altre informazioni, vedere trasformazioni del database.
ms.assetid: bfa918b8-8d90-4e14-8a06-6c3d5b5dc13b
title: Genera una trasformazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92617c2e007b9deb01685679d4940095285b8218
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757643"
---
# <a name="generate-a-transform"></a>Genera una trasformazione

Il file VBScript WiGenXfm.vbs viene fornito nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md). Questo script di esempio può generare una trasformazione da due database Windows Installer. Per altre informazioni, vedere [trasformazioni del database](database-transforms.md).

Nell'esempio viene illustrato l'utilizzo di:

[**Metodo OpenDatabase (oggetto Installer)**](installer-opendatabase.md)

[**Metodo LastErrorRecord**](installer-lasterrorrecord.md) dell' [ **oggetto Installer**](installer-object.md)

[**Metodo GenerateTransform**](database-generatetransform.md) dell' [ **oggetto di database**](database-object.md)

Per usare questo esempio, è necessaria la versione CScript.exe o WScript.exe di Windows script host. Per utilizzare CScript.exe per eseguire questo esempio, digitare una riga di comando al prompt dei comandi utilizzando la sintassi seguente. La guida viene visualizzata se il primo argomento è/? oppure se vengono specificati troppi argomenti. Per reindirizzare l'output a un file, terminare la riga di comando con VBS > \[ *percorso del file* \] . Nell'esempio viene restituito il valore 0 per l'esito positivo, 1 se la guida viene richiamata e 2 se lo script ha esito negativo.

**cscript WiGenXfm.vbs \[ percorso del database originale al percorso del \] \[ database modificato \] \[ per il file di trasformazione\]**

Consente di specificare il percorso del database di Windows Installer originale. Consente di specificare il percorso del database modificato. Consente di specificare il percorso del file di trasformazione da creare. Se il percorso del file di trasformazione viene omesso, vengono confrontati solo i due database.

Per altri esempi di script, vedere [Windows Installer esempi di scripting](windows-installer-scripting-examples.md). Per utilità di esempio che non richiedono Windows script host, vedere [Windows Installer strumenti di sviluppo](windows-installer-development-tools.md).

Si noti che [un esempio di localizzazione](a-localization-example.md) illustra la [generazione di una trasformazione di personalizzazione](generating-a-customization-transform.md).

 

 



