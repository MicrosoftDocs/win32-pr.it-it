---
description: Quando si installa un'applicazione per la prima volta, è possibile applicare una patch del programma di installazione di Windows (MSP) usando la proprietà PATCH.
ms.assetid: 2c4b9d5a-34fb-4a0b-b530-30bf238468fd
title: Applicazione di patch alle installazioni iniziali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddf89c3a83a6000a5716b5317a9fc2965562c217b110b020a2795573f8175235
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118377634"
---
# <a name="patching-initial-installations"></a>Applicazione di patch alle installazioni iniziali

Quando si installa un'applicazione per la prima volta, è possibile applicare una patch del programma di installazione di Windows (MSP) usando la [**proprietà PATCH.**](patch.md)

Per applicare una patch alla prima installazione dell'applicazione, è necessario impostare la [**proprietà PATCH**](patch.md) nella riga di comando. Specificare il percorso completo della patch nella riga di comando come coppia proprietà-valore "PATCH={*path to patch*}".

Si noti che la specifica della [**proprietà PATCH**](patch.md) nella riga di comando sostituisce i controlli di applicabilità delle patch eseguiti quando si usa [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) o l'opzione della riga di [comando](command-line-options.md)/p .

Se viene applicata una patch usando [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) o l'opzione della riga di comando [/p](command-line-options.md), il programma di installazione confronta le applicazioni attualmente installate nel computer con l'elenco di codici prodotto idonei per la ricezione della patch nella proprietà Riepilogo [**modello.**](template-summary.md)

Quando si imposta la [**proprietà PATCH**](patch.md) nella riga di comando per l'installazione alla prima installazione, le applicazioni idonee per la ricezione della patch sono determinate dalle condizioni di convalida per le trasformazioni incorporate nel pacchetto di patch. Il metodo consigliato per la generazione di un pacchetto di patch è l'uso di uno strumento di creazione di patch, ad esempio [Msimsp.exe](msimsp-exe.md) e [PATCHWIZ.DLL](patchwiz-dll.md). Le condizioni di convalida per le trasformazioni nella patch provengono dalla colonna ProductValidateFlags nella tabella [TargetImages](targetimages-table-patchwiz-dll-.md) del file Patch Creation Properties (con estensione pcp).

La patch può essere applicata la prima volta che l'applicazione viene installata da una riga di comando, un'altra applicazione o uno script.

Di seguito viene illustrata la prima applicazione di patch dalla riga di comando.

**msiexec /I** *package.msi* **PATCH=**_"c: directory \\ \\ patch.msp"_

Di seguito viene illustrata la prima applicazione di patch da un'altra applicazione.

``` syntax
UINT uiStat = MsiInstallProduct(_T("package.msi"), _T("PATCH=c:\directory\patch.msp"));
```

Di seguito viene illustrata la prima applicazione di patch dallo script.


```VB
Dim Installer as Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "package.msi", "PATCH=c:\directory\patch.msp"
```



**Windows Installer 3.0 e versioni successive: **

A partire Windows Installer versione 3.0, è possibile applicare più patch quando si installa un'applicazione per la prima volta. Impostare la [**proprietà PATCH**](patch.md) su un elenco delimitato da punto e virgola dei percorsi completi delle patch. Di seguito viene illustrata la prima applicazione di patch di più patch dalla riga di comando.

**msiexec /I** *package.msi* **PATCH=**_"c: \\ directory \\ patch.msp;c: \\ directory \\ patch2.msp;c: \\ directory \\ patch3.msp"_

 

 



