---
description: È possibile applicare una patch di Windows Installer (MSP) quando si installa un'applicazione per la prima volta tramite la proprietà PATCH.
ms.assetid: 2c4b9d5a-34fb-4a0b-b530-30bf238468fd
title: Applicazione di patch alle installazioni iniziali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa85e15da18f7342f38cf82228bc31b6e3085f09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968581"
---
# <a name="patching-initial-installations"></a>Applicazione di patch alle installazioni iniziali

È possibile applicare una patch di Windows Installer (MSP) quando si installa un'applicazione per la prima volta tramite la proprietà [**patch**](patch.md) .

Per applicare una patch la prima volta che si installa l'applicazione, è necessario impostare la proprietà [**patch**](patch.md) nella riga di comando. Specificare il percorso completo della patch nella riga di comando come coppia proprietà-valore "PATCH = {*path to patch*}".

Si noti che l'impostazione della proprietà [**patch**](patch.md) nella riga di comando sostituisce i controlli di applicabilità della patch eseguiti quando si usa [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) o l' [opzione della riga di comando](command-line-options.md)/p.

Se viene applicata una patch usando [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) o l' [opzione della riga di comando](command-line-options.md)/p, il programma di installazione Confronta le applicazioni attualmente installate nel computer con l'elenco dei codici prodotto idonei per la ricezione della patch nella proprietà di riepilogo del [**modello**](template-summary.md) .

Quando si imposta la proprietà [**patch**](patch.md) nella riga di comando per installare durante la prima installazione, le applicazioni idonee per la ricezione della patch sono determinate dalle condizioni di convalida nelle trasformazioni incorporate nel pacchetto di patch. Il metodo consigliato per la generazione di un pacchetto di patch consiste nell'usare uno strumento per la creazione di patch, ad esempio [Msimsp.exe](msimsp-exe.md) e [PATCHWIZ.DLL](patchwiz-dll.md). Le condizioni di convalida per le trasformazioni nella patch provengono dalla colonna ProductValidateFlags nella tabella [TargetImages](targetimages-table-patchwiz-dll-.md) del file delle proprietà di creazione patch (. PCP).

La patch può essere applicata la prima volta che l'applicazione viene installata tramite una riga di comando, un'altra applicazione o uno script.

Di seguito viene illustrata l'applicazione di patch per la prima volta dalla riga di comando.

**msiexec/i** *package.msi* **patch =**_"c: \\ directory \\ patch. msp"_

Di seguito viene illustrata l'applicazione di patch per la prima volta da un'altra applicazione.

``` syntax
UINT uiStat = MsiInstallProduct(_T("package.msi"), _T("PATCH=c:\directory\patch.msp"));
```

Di seguito viene illustrata l'applicazione di patch per la prima volta da script.


```VB
Dim Installer as Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "package.msi", "PATCH=c:\directory\patch.msp"
```



* * Windows Installer 3,0 e versioni successive: * *

A partire da Windows Installer versione 3,0, è possibile applicare più patch quando si installa un'applicazione per la prima volta. Impostare la proprietà [**patch**](patch.md) su un elenco delimitato da punti e virgola dei percorsi completi delle patch. Di seguito viene illustrata l'applicazione di patch per la prima volta di più patch dalla riga di comando.

**msiexec/i** *package.msi* **patch =**_"c: \\ directory \\ patch. msp; c: \\ directory \\ Patch2. msp; c: \\ directory \\ patch3. msp"_

 

 



