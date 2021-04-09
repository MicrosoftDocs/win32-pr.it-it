---
description: In questo argomento vengono fornite le linee guida per l'installazione o la reinstallazione di un'installazione a più istanze di che utilizza le trasformazioni dell'istanza.
ms.assetid: cf9076b1-5674-4ba8-9890-e981221d7b03
title: Installazione di più istanze con le trasformazioni dell'istanza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bae8d73ad60567e1557257c1207558290ba29db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049647"
---
# <a name="installing-multiple-instances-with-instance-transforms"></a>Installazione di più istanze con le trasformazioni dell'istanza

In questo argomento vengono fornite le linee guida per l'installazione o la reinstallazione di un'installazione a più istanze di che utilizza le trasformazioni dell'istanza.

-   Quando si installa una nuova istanza di con una trasformazione istanza, includere la proprietà **MSINEWINSTANCE** e impostare **MSINEWINSTANCE**= 1.
-   Quando si installa una nuova istanza di con una trasformazione istanza, includere la proprietà Transforms e impostare la prima trasformazione nell'elenco di trasformazioni nella trasformazione istanza che modifica il codice del prodotto. Tutte le trasformazioni di personalizzazione devono seguire la trasformazione istanza all'inizio dell'elenco.
-   Il modo più semplice per avviare un'installazione di manutenzione e reinstallare un'istanza di consiste nel fare riferimento al codice prodotto dell'istanza. Se si avvia l'installazione di manutenzione utilizzando il percorso del pacchetto, è necessario specificare anche il codice prodotto dell'istanza. Dalla riga di comando, usare l'opzione/n {Product code}. Dal codice o dallo script, usare la proprietà **MSIINSTANCEGUID** .

Nell'esempio seguente viene illustrata l'installazione di una nuova istanza di da una riga di comando in cui la trasformazione dell'istanza è preceduta da due punti che specificano che la trasformazione è incorporata nel pacchetto.

**msiexec/I mypackage.msi Transforms =: instance. MST MSINEWINSTANCE = 1/QB**

Nell'esempio seguente viene illustrata l'installazione di una nuova istanza di utilizzando [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta).

``` syntax
UINT uiStat = MsiInstallProduct(_T("path to mypackage.msi"), _T("TRANSFORMS=:instance.mst MSINEWINSTANCE=1"));
```

Nell'esempio seguente viene illustrata l'installazione della nuova istanza da script.

``` syntax
Dim Installer As Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "path to mypackage.msi", "TRANSFORMS=:instance.mst MSINEWINSTANCE=1"
```

Nell'esempio seguente viene reinstallata un'istanza senza inserire nuovamente il pacchetto nella cache. All'istanza viene fatto riferimento dal codice del prodotto {00000001-0002-0000-0000-624474736554} .

**msiexec/I {00000001-0002-0000-0000-624474736554} REINSTALL = ALL REINSTALLMODE = omus/QB**

Nell'esempio seguente viene reinstallata un'istanza di e il pacchetto viene nuovamente memorizzato nella cache dalla riga di comando. Il percorso del pacchetto fa riferimento all'istanza. Se il prodotto è stato installato originariamente con una trasformazione istanza, è necessario includere l'opzione/n {Product code}.

**msiexec/I c: \\ newpath \\mypackage.msi/N {00000001-0002-0000-0000-624474736554} REINSTALL = ALL REINSTALLMODE = vomus/qb**

Nell'esempio seguente viene reinstallata un'istanza di e il pacchetto viene memorizzato nella cache utilizzando **MsiInstallProduct**. Il percorso del pacchetto fa riferimento all'istanza. Utilizzare la proprietà **MSIINSTANCEGUID** per fornire il codice prodotto dell'istanza.

``` syntax
UINT uiStat = MsiInstallProduct(_T("path to mypackage.msi"), _T("MSIINSTANCEGUID={00000001-0002-0000-0000-624474736554}  REINSTALL=ALL REINSTALLMODE=vomus"));
```

Nell'esempio seguente viene reinstallata un'istanza di e il pacchetto viene memorizzato nella cache tramite script. Utilizzare la proprietà **MSIINSTANCEGUID** per fornire il codice prodotto dell'istanza.

``` syntax
Dim Installer As Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "path to mypackage.msi", "MSIINSTANCEGUID={00000001-0002-0000-0000-624474736554}  REINSTALL=ALL REINSTALLMODE=vomus"
```

Nell'esempio seguente viene illustrato come annunciare un'istanza utilizzando la riga di comando.

**msiexec/JM mypackage.msi/t: instance. MST/c/QB**

Nell'esempio seguente viene illustrato come installare per annunciare un'istanza di utilizzando **MsiAdvertiseProductEx**.

``` syntax
UINT uiStat = MsiAdvertiseProductEx(_T("path to mypackage.msi"), NULL, _T(":instance.mst"), 0, 0, MSIADVERTISEOPTIONS_INSTANCE);
```

Nell'esempio seguente viene illustrato come applicare una patch a un'istanza da una riga di comando. Se il prodotto è stato originariamente installato con una trasformazione istanza, è necessario includere l'opzione/n {Product code}.

**msiexec/p. msp/n {00000001-0002-0000-0000-624474736554} /qb**

Nell'esempio seguente viene illustrato come applicare una patch a un'installazione di un'istanza utilizzando [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha).

``` syntax
UINT uiStat = MsiApplyPatch(_T("path to mypatch.msp"), _T("{00000001-0002-0000-0000-624474736554}"), INSTALLTYPE_SINGLE_INSTANCE, _T("REINSTALL=ALL REINSTALLMODE=omus"));
```

Per ulteriori informazioni, vedere [installazione di più istanze di prodotti e patch](installing-multiple-instances-of-products-and-patches.md) e [creazione di più istanze con le trasformazioni dell'istanza](authoring-multiple-instances-with-instance-transforms.md).

 

 



