---
description: A partire da Windows Installer 3,0, è possibile disinstallare alcune patch dalle applicazioni.
ms.assetid: 11e995b7-30c7-4992-b436-3af289ac3966
title: Disinstallazione di patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff9418704bdeeb5ccc57839cbe2416faa5692265
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234179"
---
# <a name="uninstalling-patches"></a><span data-ttu-id="13d54-103">Disinstallazione di patch</span><span class="sxs-lookup"><span data-stu-id="13d54-103">Uninstalling Patches</span></span>

<span data-ttu-id="13d54-104">A partire da Windows Installer 3,0, è possibile disinstallare alcune patch dalle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="13d54-104">Beginning with Windows Installer 3.0, it is possible to uninstall some patches from applications.</span></span> <span data-ttu-id="13d54-105">La patch deve essere una [patch non installabile](uninstallable-patches.md).</span><span class="sxs-lookup"><span data-stu-id="13d54-105">The patch must be an [uninstallable patch](uninstallable-patches.md).</span></span> <span data-ttu-id="13d54-106">Quando si usa una versione di Windows Installer inferiore alla versione 3,0, la [rimozione delle patch](removing-patches.md) richiede la disinstallazione del prodotto patch e la reinstallazione del prodotto senza applicare la patch.</span><span class="sxs-lookup"><span data-stu-id="13d54-106">When using a Windows Installer version less than version 3.0, [removing patches](removing-patches.md) requires uninstalling the patch product and reinstalling the product without applying the patch.</span></span>

<span data-ttu-id="13d54-107">**Windows Installer 2,0:** Non supportato.</span><span class="sxs-lookup"><span data-stu-id="13d54-107">**Windows Installer 2.0:** Not supported.</span></span> <span data-ttu-id="13d54-108">Le patch applicate con una versione di Windows Installer precedente alla Windows Installer 3,0 non sono disinstallabili.</span><span class="sxs-lookup"><span data-stu-id="13d54-108">Patches applied using a version of Windows Installer that is earlier than Windows Installer 3.0 are not uninstallable.</span></span>

<span data-ttu-id="13d54-109">Quando si richiama una disinstallazione di una patch con uno dei metodi seguenti, il programma di installazione tenta di rimuovere la patch dal primo prodotto visibile all'applicazione o all'utente che ha richiesto la disinstallazione.</span><span class="sxs-lookup"><span data-stu-id="13d54-109">When you invoke an uninstallation of a patch by any of the following methods, the installer attempts to remove the patch from the first product visible to the application or user requesting the uninstallation.</span></span> <span data-ttu-id="13d54-110">Il programma di installazione cerca i prodotti con patch nell'ordine seguente: gestito dall'utente per utente, non gestito, per computer.</span><span class="sxs-lookup"><span data-stu-id="13d54-110">The installer searches for patched products in the following order: per-user managed, per-user unmanaged, per-machine.</span></span>

## <a name="uninstalling-a-patch-using-msipatchremove-on-a-command-line"></a><span data-ttu-id="13d54-111">Disinstallazione di una patch tramite MSIPATCHREMOVE in una riga di comando</span><span class="sxs-lookup"><span data-stu-id="13d54-111">Uninstalling a patch using MSIPATCHREMOVE on a command line</span></span>

<span data-ttu-id="13d54-112">È possibile disinstallare le patch da un comando usando msiexec.exe e le [Opzioni della riga di comando](command-line-options.md).</span><span class="sxs-lookup"><span data-stu-id="13d54-112">You can uninstall patches from a command by using msiexec.exe and the [Command Line Options](command-line-options.md).</span></span> <span data-ttu-id="13d54-113">La riga di comando di esempio seguente rimuove una [patch disinstallabile](uninstallable-patches.md), ad esempio msp, da un'applicazione example.msi, usando la proprietà [**MSIPATCHREMOVE**](msipatchremove.md) e l'opzione della riga di comando/i.</span><span class="sxs-lookup"><span data-stu-id="13d54-113">The following sample command line removes an [uninstallable patch](uninstallable-patches.md), example.msp, from an application, example.msi, using the [**MSIPATCHREMOVE**](msipatchremove.md) property and the /i command line option.</span></span> <span data-ttu-id="13d54-114">Quando si usa/i, l'applicazione con patch può essere identificata dal percorso del pacchetto dell'applicazione (file con estensione msi) o dal [codice del prodotto](product-codes.md)dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="13d54-114">When using /i, the patched application can be identified by the path to the application's package (.msi file) or the application's [product code](product-codes.md).</span></span> <span data-ttu-id="13d54-115">In questo esempio, il pacchetto di installazione dell'applicazione si trova in " \\ \\ \\ esempio di prodotti server share \\ \\ \\example.msi" e la proprietà [**ProductCode**](productcode.md) dell'applicazione è "{0C9840E7-7F0B-C648-10F0-4641926FE463}".</span><span class="sxs-lookup"><span data-stu-id="13d54-115">In this example, the application's installation package is located at "\\\\server\\share\\products\\example\\example.msi" and the application's [**ProductCode**](productcode.md) property is "{0C9840E7-7F0B-C648-10F0-4641926FE463}".</span></span> <span data-ttu-id="13d54-116">Il pacchetto di patch si trova in " \\ \\ server \\ share \\ Products \\ example \\ patches \\ example. msp" e il GUID del codice della patch è "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}".</span><span class="sxs-lookup"><span data-stu-id="13d54-116">The patch package is located at "\\\\server\\share\\products\\example\\patches\\example.msp" and the patch code GUID is "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}".</span></span>

<span data-ttu-id="13d54-117">**Msiexec/I {0C9840E7-7F0B-C648-10F0-4641926FE463} MSIPATCHREMOVE = {EB8C947C-78B2-85A0-644D-86CEEF8E07C0}/QB**</span><span class="sxs-lookup"><span data-stu-id="13d54-117">**Msiexec /I {0C9840E7-7F0B-C648-10F0-4641926FE463} MSIPATCHREMOVE={EB8C947C-78B2-85A0-644D-86CEEF8E07C0} /qb**</span></span>

## <a name="uninstalling-a-patch-using-the-standard-command-line-options"></a><span data-ttu-id="13d54-118">Disinstallazione di una patch usando le opzioni della riga di comando standard</span><span class="sxs-lookup"><span data-stu-id="13d54-118">Uninstalling a patch using the standard command line options</span></span>

<span data-ttu-id="13d54-119">A partire da Windows Installer versione 3,0, è possibile usare le [Opzioni della riga di comando standard](standard-installer-command-line-options.md) usate dagli aggiornamenti del sistema operativo Microsoft Windows (update.exe) per disinstallare Windows Installer patch da una riga di comando.</span><span class="sxs-lookup"><span data-stu-id="13d54-119">Beginning with Windows Installer version 3.0, you can use the [standard command line options](standard-installer-command-line-options.md) used by Microsoft Windows Operating System Updates (update.exe) to uninstall Windows Installer patches from a command line.</span></span>

<span data-ttu-id="13d54-120">La riga di comando seguente è l'equivalente della riga di comando standard della Windows Installer riga di comando usata per disinstallare una patch usando la proprietà [**MSIPATCHREMOVE**](msipatchremove.md) .</span><span class="sxs-lookup"><span data-stu-id="13d54-120">The following command line is the standard command line equivalent of the Windows Installer command line used to uninstall a patch using the [**MSIPATCHREMOVE**](msipatchremove.md) property.</span></span> <span data-ttu-id="13d54-121">L'opzione/uninstall usata con l'opzione/Package denota la disinstallazione di una patch.</span><span class="sxs-lookup"><span data-stu-id="13d54-121">The /uninstall option used with the /package option denotes the uninstallation of a patch.</span></span> <span data-ttu-id="13d54-122">È possibile fare riferimento alla patch con il percorso completo della patch o con il GUID del codice della patch.</span><span class="sxs-lookup"><span data-stu-id="13d54-122">The patch can be referenced by the full path to the patch or by the patch code GUID.</span></span>

<span data-ttu-id="13d54-123">**Msiexec/package {0C9840E7-7F0B-C648-10F0-4641926FE463}/Uninstall {EB8C947C-78B2-85A0-644D-86CEEF8E07C0}/passive**</span><span class="sxs-lookup"><span data-stu-id="13d54-123">**Msiexec /package {0C9840E7-7F0B-C648-10F0-4641926FE463} /uninstall {EB8C947C-78B2-85A0-644D-86CEEF8E07C0} /passive**</span></span>

> [!Note]  
> <span data-ttu-id="13d54-124">L'opzione/passive standard non è un equivalente esatto dell'opzione Windows Installer/QB.</span><span class="sxs-lookup"><span data-stu-id="13d54-124">The /passive standard option is not an exact equivalent of the Windows Installer /qb option.</span></span>

 

## <a name="uninstalling-a-patch-using-the-removepatches-method"></a><span data-ttu-id="13d54-125">Disinstallazione di una patch tramite il metodo RemovePatches</span><span class="sxs-lookup"><span data-stu-id="13d54-125">Uninstalling a patch using the RemovePatches method</span></span>

<span data-ttu-id="13d54-126">È possibile disinstallare patch da script usando l'interfaccia di [automazione](automation-interface.md)Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="13d54-126">You can uninstall patches from script by using the Windows Installer [Automation Interface](automation-interface.md).</span></span> <span data-ttu-id="13d54-127">Nell'esempio di script seguente viene rimossa una [patch disinstallabile](uninstallable-patches.md), ad esempio msp, da un'applicazione example.msi, utilizzando il metodo [**RemovePatches**](installer-removepatches.md) dell'oggetto [Installer](installer-object.md) .</span><span class="sxs-lookup"><span data-stu-id="13d54-127">The following scripting sample removes an [uninstallable patch](uninstallable-patches.md), example.msp, from an application, example.msi, using the [**RemovePatches**](installer-removepatches.md) method of the [Installer](installer-object.md) object.</span></span> <span data-ttu-id="13d54-128">Ogni patch da disinstallare può essere rappresentata dal percorso completo del pacchetto di patch o dal GUID del codice della patch.</span><span class="sxs-lookup"><span data-stu-id="13d54-128">Each patch being uninstalled can be represented by either the full path to the patch package or the patch code GUID.</span></span> <span data-ttu-id="13d54-129">In questo esempio, il pacchetto di installazione dell'applicazione si trova in " \\ \\ \\ esempio di prodotti server share \\ \\ \\example.msi" e la proprietà [**ProductCode**](productcode.md) dell'applicazione è "{0C9840E7-7F0B-C648-10F0-4641926FE463}".</span><span class="sxs-lookup"><span data-stu-id="13d54-129">In this example, the application's installation package is located at "\\\\server\\share\\products\\example\\example.msi" and the application's [**ProductCode**](productcode.md) property is "{0C9840E7-7F0B-C648-10F0-4641926FE463}".</span></span> <span data-ttu-id="13d54-130">Il pacchetto di patch si trova in " \\ \\ server \\ share \\ Products \\ example \\ patches \\ example. msp" e il GUID del codice della patch è "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}".</span><span class="sxs-lookup"><span data-stu-id="13d54-130">The patch package is located at "\\\\server\\share\\products\\example\\patches\\example.msp" and the patch code GUID is "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}".</span></span>


```VB
const msiInstallTypeSingleInstance = 2
const PatchList = "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}"
const Product = "{0C9840E7-7F0B-C648-10F0-4641926FE463}"

Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

installer.RemovePatches(PatchList, Product, msiInstallTypeSingleInstance, "")
```



## <a name="uninstalling-a-patch-using-addremove-programs"></a><span data-ttu-id="13d54-131">Disinstallazione di una patch con installazione applicazioni</span><span class="sxs-lookup"><span data-stu-id="13d54-131">Uninstalling a patch using Add/Remove Programs</span></span>

<span data-ttu-id="13d54-132">Con Windows XP, è possibile disinstallare le patch utilizzando Installazione applicazioni.</span><span class="sxs-lookup"><span data-stu-id="13d54-132">With Windows XP, you can uninstall patches using Add/Remove programs.</span></span>

## <a name="uninstalling-a-patch-using-the-msiremovepatches-function"></a><span data-ttu-id="13d54-133">Disinstallazione di una patch tramite la funzione MsiRemovePatches</span><span class="sxs-lookup"><span data-stu-id="13d54-133">Uninstalling a patch using the MsiRemovePatches function</span></span>

<span data-ttu-id="13d54-134">Le applicazioni possono disinstallare le patch da altre applicazioni usando le [funzioni Windows Installer](installer-functions.md).</span><span class="sxs-lookup"><span data-stu-id="13d54-134">Your applications can uninstall patches from other applications by using the [Windows Installer Functions](installer-functions.md).</span></span> <span data-ttu-id="13d54-135">Nell'esempio di codice seguente viene rimossa una [patch non installabile](uninstallable-patches.md), ad esempio msp, da un'applicazione example.msi, utilizzando la funzione [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) .</span><span class="sxs-lookup"><span data-stu-id="13d54-135">The following code example removes an [uninstallable patch](uninstallable-patches.md), example.msp, from an application, example.msi, using the [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) function.</span></span> <span data-ttu-id="13d54-136">È possibile fare riferimento a una patch tramite il percorso completo del pacchetto di patch o il GUID del codice della patch.</span><span class="sxs-lookup"><span data-stu-id="13d54-136">A patch can be referenced by the full path to the patch package or the patch code GUID.</span></span> <span data-ttu-id="13d54-137">In questo esempio, il pacchetto di installazione dell'applicazione si trova in " \\ \\ \\ esempio di prodotti server share \\ \\ \\example.msi" e la proprietà [**ProductCode**](productcode.md) dell'applicazione è "{0C9840E7-7F0B-C648-10F0-4641926FE463}".</span><span class="sxs-lookup"><span data-stu-id="13d54-137">In this example, the application's installation package is located at "\\\\server\\share\\products\\example\\example.msi" and the application's [**ProductCode**](productcode.md) property is "{0C9840E7-7F0B-C648-10F0-4641926FE463}".</span></span> <span data-ttu-id="13d54-138">Il pacchetto di patch si trova in " \\ \\ server \\ share \\ Products \\ example \\ patches \\ example. msp" e il GUID del codice della patch è "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}".</span><span class="sxs-lookup"><span data-stu-id="13d54-138">The patch package is located at "\\\\server\\share\\products\\example\\patches\\example.msp" and the patch code GUID is "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}".</span></span>


```C++
    UINT uiReturn = MsiRemovePatches(
          /*szPatchList=*/TEXT("\\server\\share\\products\\example\\patches\\example.msp"),
          /*szProductCode=*/  TEXT("{0C9840E7-7F0B-C648-10F0-4641926FE463}"),
          /*eUninstallType=*/ INSTALLTYPE_SINGLE_INSTANCE,
          /*szPropertyList=*/ NULL);
```



## <a name="uninstalling-a-patch-from-all-applications-using-msiremovepatches-function"></a><span data-ttu-id="13d54-139">Disinstallazione di una patch da tutte le applicazioni tramite la funzione MsiRemovePatches</span><span class="sxs-lookup"><span data-stu-id="13d54-139">Uninstalling a patch from all applications using MsiRemovePatches function</span></span>

<span data-ttu-id="13d54-140">Una singola patch può aggiornare più di un prodotto nel computer.</span><span class="sxs-lookup"><span data-stu-id="13d54-140">A single patch can update more than one product on the computer.</span></span> <span data-ttu-id="13d54-141">Un'applicazione può utilizzare [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) per enumerare tutti i prodotti nel computer e determinare se una patch è stata applicata a una particolare istanza del prodotto.</span><span class="sxs-lookup"><span data-stu-id="13d54-141">An application can use [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) to enumerate all the products on the computer and determine whether a patch has been applied to a particular instance of the product.</span></span> <span data-ttu-id="13d54-142">L'applicazione può quindi disinstallare la patch usando [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa).</span><span class="sxs-lookup"><span data-stu-id="13d54-142">The application can then uninstall the patch using [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa).</span></span> <span data-ttu-id="13d54-143">Ad esempio, una singola patch può aggiornare più prodotti se la patch aggiorna un file in un componente condiviso da più prodotti e la patch viene distribuita per aggiornare entrambi i prodotti.</span><span class="sxs-lookup"><span data-stu-id="13d54-143">For example, a single patch can update multiple products if the patch updates a file in a component that is shared by multiple products and the patch is distributed to update both products.</span></span>

<span data-ttu-id="13d54-144">Nell'esempio seguente viene illustrato come un'applicazione può utilizzare il Windows Installer per rimuovere una patch da tutte le applicazioni disponibili per l'utente.</span><span class="sxs-lookup"><span data-stu-id="13d54-144">The following example demonstrates how an application can use the Windows Installer to remove a patch from all applications that are available to the user.</span></span> <span data-ttu-id="13d54-145">Non rimuove la patch dalle applicazioni installate per utente per un altro utente.</span><span class="sxs-lookup"><span data-stu-id="13d54-145">It does not remove the patch from applications installed per-user for another user.</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif //UNICODE

#ifndef _WIN32_MSI
#define _WIN32_MSI 300
#endif //_WIN32_MSI

#include <stdio.h>
#include <windows.h>
#include <msi.h>

#pragma comment(lib, "msi.lib")

const int cchGUID = 38;

///////////////////////////////////////////////////////////////////
// RemovePatchFromAllVisibleapplications:
//
// Arguments:
//    wszPatchToRemove - GUID of patch to remove
//
///////////////////////////////////////////////////////////////////
//
UINT RemovePatchFromAllVisibleapplications(LPCWSTR wszPatchToRemove)
{
    if (!wszPatchToRemove)
        return ERROR_INVALID_PARAMETER;

    UINT uiStatus = ERROR_SUCCESS;
    DWORD dwIndex = 0;
    WCHAR wszapplicationCode[cchGUID+1] = {0};

    DWORD dwapplicationSearchContext = MSIINSTALLCONTEXT_ALL;
    MSIINSTALLCONTEXT dwInstallContext = MSIINSTALLCONTEXT_NONE;

    do
    {
        // Enumerate all visible applications in all contexts for the caller.
        // NULL for szUserSid defaults to using the caller's SID
        uiStatus = MsiEnumProductsEx(/*szapplicationCode*/NULL,
         /*szUserSid*/NULL,
         dwapplicationSearchContext,
         dwIndex,
         wszapplicationCode,
         &dwInstallContext,
         /*szSid*/NULL,
         /*pcchSid*/NULL);

        if (ERROR_SUCCESS == uiStatus)
        {
            // check to see if the provided patch is
            // registered for this application instance
            UINT uiPatchStatus = MsiGetPatchInfoEx(wszPatchToRemove,
             wszapplicationCode,
             /*szUserSid*/NULL,
             dwInstallContext,
             INSTALLPROPERTY_PATCHSTATE,
             NULL,
             NULL);

            if (ERROR_SUCCESS == uiPatchStatus)
            {
                // patch is registered to this application; remove patch
                wprintf(L"Removing patch %s from application %s...\n",
                 wszPatchToRemove, wszapplicationCode);
                                
                UINT uiRemoveStatus = MsiRemovePatches(
                 wszPatchToRemove,
                 wszapplicationCode,
                 INSTALLTYPE_SINGLE_INSTANCE,
                 L"");

                if (ERROR_SUCCESS != uiRemoveStatus)
                {
                    // This halts the enumeration and fails. Alternatively
                    // you could output an error and continue the
                    // enumeration
                     return ERROR_FUNCTION_FAILED;
                }
            }
            else if (ERROR_UNKNOWN_PATCH != uiPatchStatus)
            {
                // Some other error occurred during processing. This
                // halts the enumeration and fails. Alternatively you
                // could output an error and continue the enumeration
                 return ERROR_FUNCTION_FAILED;
            }
            // else patch was not applied to this application
            // (ERROR_UNKNOWN_PATCH returned)
        }

        dwIndex++;
    }
    while (uiStatus == ERROR_SUCCESS);

    if (ERROR_NO_MORE_ITEMS != uiStatus)
        return ERROR_FUNCTION_FAILED;

    return ERROR_SUCCESS;
}
```



## <a name="related-topics"></a><span data-ttu-id="13d54-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="13d54-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13d54-147">Sequenza di patch</span><span class="sxs-lookup"><span data-stu-id="13d54-147">Patch Sequencing</span></span>](sequencing-patches.md)
</dt> <dt>

[<span data-ttu-id="13d54-148">Rimozione di patch</span><span class="sxs-lookup"><span data-stu-id="13d54-148">Removing Patches</span></span>](removing-patches.md)
</dt> <dt>

[<span data-ttu-id="13d54-149">Patch disinstallabili</span><span class="sxs-lookup"><span data-stu-id="13d54-149">Uninstallable Patches</span></span>](uninstallable-patches.md)
</dt> <dt>

[<span data-ttu-id="13d54-150">Patch disinstallare azioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="13d54-150">Patch Uninstall Custom Actions</span></span>](patch-uninstall-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="13d54-151">**MSIPATCHREMOVE**</span><span class="sxs-lookup"><span data-stu-id="13d54-151">**MSIPATCHREMOVE**</span></span>](msipatchremove.md)
</dt> <dt>

[<span data-ttu-id="13d54-152">**MsiEnumapplicationsEx**</span><span class="sxs-lookup"><span data-stu-id="13d54-152">**MsiEnumapplicationsEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[<span data-ttu-id="13d54-153">**MsiGetPatchInfoEx**</span><span class="sxs-lookup"><span data-stu-id="13d54-153">**MsiGetPatchInfoEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[<span data-ttu-id="13d54-154">**MsiRemovePatches**</span><span class="sxs-lookup"><span data-stu-id="13d54-154">**MsiRemovePatches**</span></span>](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> </dl>

 

 



