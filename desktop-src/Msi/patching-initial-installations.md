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
# <a name="patching-initial-installations"></a><span data-ttu-id="d1877-103">Applicazione di patch alle installazioni iniziali</span><span class="sxs-lookup"><span data-stu-id="d1877-103">Patching Initial Installations</span></span>

<span data-ttu-id="d1877-104">È possibile applicare una patch di Windows Installer (MSP) quando si installa un'applicazione per la prima volta tramite la proprietà [**patch**](patch.md) .</span><span class="sxs-lookup"><span data-stu-id="d1877-104">A Windows Installer Patch (MSP) can be applied when installing an application for the first time by using the [**PATCH**](patch.md) property.</span></span>

<span data-ttu-id="d1877-105">Per applicare una patch la prima volta che si installa l'applicazione, è necessario impostare la proprietà [**patch**](patch.md) nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="d1877-105">To apply a patch the first time the application is installed, the [**PATCH**](patch.md) property must be set on the command line.</span></span> <span data-ttu-id="d1877-106">Specificare il percorso completo della patch nella riga di comando come coppia proprietà-valore "PATCH = {*path to patch*}".</span><span class="sxs-lookup"><span data-stu-id="d1877-106">Specify the full path to the patch on the command line as the "PATCH={*path to patch*}" property-value pair.</span></span>

<span data-ttu-id="d1877-107">Si noti che l'impostazione della proprietà [**patch**](patch.md) nella riga di comando sostituisce i controlli di applicabilità della patch eseguiti quando si usa [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) o l' [opzione della riga di comando](command-line-options.md)/p.</span><span class="sxs-lookup"><span data-stu-id="d1877-107">Note that specifying the [**PATCH**](patch.md) property on the command line overrides the patch applicability checks performed when using [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) or the /p [Command Line Option](command-line-options.md).</span></span>

<span data-ttu-id="d1877-108">Se viene applicata una patch usando [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) o l' [opzione della riga di comando](command-line-options.md)/p, il programma di installazione Confronta le applicazioni attualmente installate nel computer con l'elenco dei codici prodotto idonei per la ricezione della patch nella proprietà di riepilogo del [**modello**](template-summary.md) .</span><span class="sxs-lookup"><span data-stu-id="d1877-108">If a patch is applied using [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) or the /p [Command Line Option](command-line-options.md), the installer compares the applications currently installed on the computer to the list of product codes eligible to receive the patch in the [**Template Summary**](template-summary.md) property.</span></span>

<span data-ttu-id="d1877-109">Quando si imposta la proprietà [**patch**](patch.md) nella riga di comando per installare durante la prima installazione, le applicazioni idonee per la ricezione della patch sono determinate dalle condizioni di convalida nelle trasformazioni incorporate nel pacchetto di patch.</span><span class="sxs-lookup"><span data-stu-id="d1877-109">When you set the [**PATCH**](patch.md) property on the command line to install on first installation, the applications eligible to receive the patch is determined by validation conditions on the transforms embedded in the patch package.</span></span> <span data-ttu-id="d1877-110">Il metodo consigliato per la generazione di un pacchetto di patch consiste nell'usare uno strumento per la creazione di patch, ad esempio [Msimsp.exe](msimsp-exe.md) e [PATCHWIZ.DLL](patchwiz-dll.md).</span><span class="sxs-lookup"><span data-stu-id="d1877-110">The recommended method for generating a patch package is to use a patch creation tool such as [Msimsp.exe](msimsp-exe.md) and [PATCHWIZ.DLL](patchwiz-dll.md).</span></span> <span data-ttu-id="d1877-111">Le condizioni di convalida per le trasformazioni nella patch provengono dalla colonna ProductValidateFlags nella tabella [TargetImages](targetimages-table-patchwiz-dll-.md) del file delle proprietà di creazione patch (. PCP).</span><span class="sxs-lookup"><span data-stu-id="d1877-111">The validation conditions on transforms in the patch originate from the ProductValidateFlags column in the [TargetImages](targetimages-table-patchwiz-dll-.md) table of the Patch Creation Properties (.pcp) file.</span></span>

<span data-ttu-id="d1877-112">La patch può essere applicata la prima volta che l'applicazione viene installata tramite una riga di comando, un'altra applicazione o uno script.</span><span class="sxs-lookup"><span data-stu-id="d1877-112">The patch can be applied the first time the application is installed by a command line, another application, or script.</span></span>

<span data-ttu-id="d1877-113">Di seguito viene illustrata l'applicazione di patch per la prima volta dalla riga di comando.</span><span class="sxs-lookup"><span data-stu-id="d1877-113">The following shows first-time patching from the command line.</span></span>

<span data-ttu-id="d1877-114">**msiexec/i** *package.msi* **patch =**_"c: \\ directory \\ patch. msp"_</span><span class="sxs-lookup"><span data-stu-id="d1877-114">**msiexec /I** *package.msi* **PATCH=**_"c:\\directory\\patch.msp"_</span></span>

<span data-ttu-id="d1877-115">Di seguito viene illustrata l'applicazione di patch per la prima volta da un'altra applicazione.</span><span class="sxs-lookup"><span data-stu-id="d1877-115">The following shows first-time patching from another application.</span></span>

``` syntax
UINT uiStat = MsiInstallProduct(_T("package.msi"), _T("PATCH=c:\directory\patch.msp"));
```

<span data-ttu-id="d1877-116">Di seguito viene illustrata l'applicazione di patch per la prima volta da script.</span><span class="sxs-lookup"><span data-stu-id="d1877-116">The following shows first-time patching from script.</span></span>


```VB
Dim Installer as Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "package.msi", "PATCH=c:\directory\patch.msp"
```



<span data-ttu-id="d1877-117">\* \* Windows Installer 3,0 e versioni successive: \* \*</span><span class="sxs-lookup"><span data-stu-id="d1877-117">\*\*Windows Installer 3.0 and later:  \*\*</span></span>

<span data-ttu-id="d1877-118">A partire da Windows Installer versione 3,0, è possibile applicare più patch quando si installa un'applicazione per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="d1877-118">Beginning with Windows Installer version 3.0, multiple patches can be applied when installing an application for the first time.</span></span> <span data-ttu-id="d1877-119">Impostare la proprietà [**patch**](patch.md) su un elenco delimitato da punti e virgola dei percorsi completi delle patch.</span><span class="sxs-lookup"><span data-stu-id="d1877-119">Set the [**PATCH**](patch.md) property to a semicolon delimited list of the patches' full paths.</span></span> <span data-ttu-id="d1877-120">Di seguito viene illustrata l'applicazione di patch per la prima volta di più patch dalla riga di comando.</span><span class="sxs-lookup"><span data-stu-id="d1877-120">The following shows first-time patching of multiple patches from the command line.</span></span>

<span data-ttu-id="d1877-121">**msiexec/i** *package.msi* **patch =**_"c: \\ directory \\ patch. msp; c: \\ directory \\ Patch2. msp; c: \\ directory \\ patch3. msp"_</span><span class="sxs-lookup"><span data-stu-id="d1877-121">**msiexec /I** *package.msi* **PATCH=**_"c:\\directory\\patch.msp;c:\\directory\\patch2.msp;c:\\directory\\patch3.msp"_</span></span>

 

 



