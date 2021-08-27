---
description: In questo argomento vengono fornite linee guida per l'installazione o la reinstallazione di un'installazione a più istanze che usa trasformazioni di istanza.
ms.assetid: cf9076b1-5674-4ba8-9890-e981221d7b03
title: Installazione di più istanze con trasformazioni di istanza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a25b2cba8fd91316d62692d278345e0f7d9751f018e1c33239412988bfe118a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074901"
---
# <a name="installing-multiple-instances-with-instance-transforms"></a>Installazione di più istanze con trasformazioni di istanza

In questo argomento vengono fornite linee guida per l'installazione o la reinstallazione di un'installazione a più istanze che usa trasformazioni di istanza.

-   Quando si installa una nuova istanza con una trasformazione di istanza, includere la **proprietà MSINEWINSTANCE** e impostare **MSINEWINSTANCE**=1.
-   Quando si installa una nuova istanza con una trasformazione di istanza, includere la proprietà TRANSFORMS e impostare la prima trasformazione nell'elenco delle trasformazioni nella trasformazione dell'istanza che modifica il codice del prodotto. Tutte le trasformazioni di personalizzazione devono seguire la trasformazione dell'istanza all'inizio di questo elenco.
-   Il modo più semplice per avviare un'installazione di manutenzione e reinstallare un'istanza è fare riferimento al codice prodotto dell'istanza. Se si avvia l'installazione di manutenzione usando il percorso del pacchetto, è necessario specificare anche il codice prodotto dell'istanza. Dalla riga di comando usare l'opzione /n {Product Code}. Dal codice o dallo script usare la **proprietà MSIINSTANCEGUID.**

Nell'esempio seguente viene illustrata l'installazione di una nuova istanza da una riga di comando in cui la trasformazione dell'istanza è preceduta da due punti che specifica che la trasformazione è incorporata nel pacchetto.

**msiexec /I mypackage.msi TRANSFORMS=:instance.mst MSINEWINSTANCE=1 /qb**

Nell'esempio seguente viene illustrata l'installazione di una nuova istanza tramite [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta).

``` syntax
UINT uiStat = MsiInstallProduct(_T("path to mypackage.msi"), _T("TRANSFORMS=:instance.mst MSINEWINSTANCE=1"));
```

Nell'esempio seguente viene illustrata l'installazione della nuova istanza di dallo script.

``` syntax
Dim Installer As Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "path to mypackage.msi", "TRANSFORMS=:instance.mst MSINEWINSTANCE=1"
```

Nell'esempio seguente viene reinstallata un'istanza di senza memorizzare nuovamente nella cache il pacchetto. L'istanza viene definita dal codice prodotto {00000001-0002-0000-0000-624474736554} .

**msiexec /I {00000001-0002-0000-0000-624474736554} REINSTALL=ALL REINSTALLMODE=omus /qb**

L'esempio seguente reinstalla un'istanza di e memorizza nuovamente nella cache il pacchetto dalla riga di comando. Il percorso del pacchetto fa riferimento all'istanza. È necessario includere l'opzione /n {Codice prodotto} solo se il prodotto è originariamente installato con una trasformazione di istanza.

**msiexec /I c: \\ newpath \\mypackage.msi /n {00000001-0002-0000-0000-624474736554} REINSTALL=ALL REINSTALLMODE=vomus /qb**

L'esempio seguente reinstalla un'istanza di e memorizza nella cache il pacchetto **usando MsiInstallProduct**. Il percorso del pacchetto fa riferimento all'istanza. Usare la **proprietà MSIINSTANCEGUID** per fornire il codice prodotto dell'istanza.

``` syntax
UINT uiStat = MsiInstallProduct(_T("path to mypackage.msi"), _T("MSIINSTANCEGUID={00000001-0002-0000-0000-624474736554}  REINSTALL=ALL REINSTALLMODE=vomus"));
```

Nell'esempio seguente viene reinstallata un'istanza di e il pacchetto viene memorizzato nella cache usando lo script . Usare la **proprietà MSIINSTANCEGUID** per fornire il codice prodotto dell'istanza.

``` syntax
Dim Installer As Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "path to mypackage.msi", "MSIINSTANCEGUID={00000001-0002-0000-0000-624474736554}  REINSTALL=ALL REINSTALLMODE=vomus"
```

Nell'esempio seguente viene illustrato come annunciare un'istanza tramite la riga di comando.

**msiexec /jm mypackage.msi /t :instance.mst /c /qb**

L'esempio seguente illustra come installare per annunciare un'istanza usando **MsiAdvertiseProductEx**.

``` syntax
UINT uiStat = MsiAdvertiseProductEx(_T("path to mypackage.msi"), NULL, _T(":instance.mst"), 0, 0, MSIADVERTISEOPTIONS_INSTANCE);
```

Nell'esempio seguente viene illustrato come applicare una patch a un'istanza di da una riga di comando. È necessario includere l'opzione /n {Codice prodotto} solo se il prodotto è stato originariamente installato con una trasformazione di istanza.

**msiexec /p mypatch.msp /n {00000001-0002-0000-0000-624474736554} /qb**

Nell'esempio seguente viene illustrato come applicare una patch a un'installazione di istanza usando [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha).

``` syntax
UINT uiStat = MsiApplyPatch(_T("path to mypatch.msp"), _T("{00000001-0002-0000-0000-624474736554}"), INSTALLTYPE_SINGLE_INSTANCE, _T("REINSTALL=ALL REINSTALLMODE=omus"));
```

Per altre informazioni, vedere [Installazione di più istanze](installing-multiple-instances-of-products-and-patches.md) di prodotti e patch e Creazione di più istanze con trasformazioni di [istanza](authoring-multiple-instances-with-instance-transforms.md).

 

 



