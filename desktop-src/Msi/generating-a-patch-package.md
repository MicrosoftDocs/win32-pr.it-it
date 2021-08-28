---
description: Il metodo consigliato per generare un pacchetto patch è usare uno strumento di creazione di patch, ad esempio Msimsp.exe per chiamare UiCreatePatchPackage in Patchwiz.dll. Msimsp.exe e PatchWiz.dll sono disponibili nell'SDK Windows Installer.
ms.assetid: 7fa661aa-d52c-4b08-961f-90ec778f02ff
title: Generazione di un pacchetto di patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0577c678bbb378da425ff438a0e165dcba95d6e1fc1eecc1d9c311fe2c78bca2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581431"
---
# <a name="generating-a-patch-package"></a>Generazione di un pacchetto di patch

Il metodo consigliato per generare un pacchetto di patch è usare uno strumento di creazione di patch, ad esempio [Msimsp.exe](msimsp-exe.md) per chiamare [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) [ in ](patchwiz-dll.md)Patchwiz.dll. Msimsp.exe e PatchWiz.dll sono disponibili nell'SDK Windows Installer.

La riga di comando di esempio seguente usa Msimsp.exe e il file con estensione pcp creato in Creazione di un [file](creating-a-patch-creation-properties-file.md) delle proprietà di creazione patch per generare il pacchetto di patch di esempio MNP2000.msp.

**Msimsp.exe -s C: Nota Installer \\ \_ Patch \\ \\ MNP2000.pcp -p C: \\ Nota Installer Patch \_ \\ \\ MNP2000.msp**

Uno strumento di creazione di patch creato può generare il pacchetto patch chiamando [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) come indicato di seguito.

``` syntax
UiCreatePatchPackage ("C:\\Note_Installer\\Patch\\MNP2000.pcp", "C:\\Note_Installer\\Patch\\MNP2000.msp", NULL, NULL, "", TRUE)
```

[Continua](applying-a-patch-package-to-a-local-installation.md)

 

 



