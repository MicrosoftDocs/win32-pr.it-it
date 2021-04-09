---
description: Il metodo consigliato per la generazione di un pacchetto di patch consiste nell'usare uno strumento per la creazione di patch, ad esempio Msimsp.exe per chiamare UiCreatePatchPackage in Patchwiz.dll. In Windows Installer SDK sono disponibili Msimsp.exe e PatchWiz.dll.
ms.assetid: 7fa661aa-d52c-4b08-961f-90ec778f02ff
title: Generazione di un pacchetto di patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ef64ac66cd0201ae99080ec86e32230bc88407b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967801"
---
# <a name="generating-a-patch-package"></a>Generazione di un pacchetto di patch

Il metodo consigliato per la generazione di un pacchetto di patch consiste nell'usare uno strumento per la creazione di patch, ad esempio [Msimsp.exe](msimsp-exe.md) per chiamare [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) in [Patchwiz.dll](patchwiz-dll.md). In Windows Installer SDK sono disponibili Msimsp.exe e PatchWiz.dll.

La riga di comando di esempio seguente usa Msimsp.exe e il file con estensione PCP creato in [creazione di un file delle proprietà di creazione patch](creating-a-patch-creation-properties-file.md) per generare il pacchetto di patch di esempio MNP2000. msp.

**Msimsp.exe-s C: \\ Nota \_ patch del programma di installazione \\ \\ MNP2000. PCP-p C: \\ Nota \_ patch di installazione \\ \\ MNP2000. msp**

Uno strumento di creazione patch creato può generare il pacchetto di patch chiamando [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) come indicato di seguito.

``` syntax
UiCreatePatchPackage ("C:\\Note_Installer\\Patch\\MNP2000.pcp", "C:\\Note_Installer\\Patch\\MNP2000.msp", NULL, NULL, "", TRUE)
```

[Continua](applying-a-patch-package-to-a-local-installation.md)

 

 



