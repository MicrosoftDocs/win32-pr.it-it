---
description: A partire da Windows Installer 3,0, è possibile applicare patch a un'applicazione installata in un contesto gestito per utente dopo la registrazione della patch con privilegi elevati.
ms.assetid: ebe5f447-9b74-48dc-8192-f2ac90dca490
title: Applicazione di patch Per-User applicazioni gestite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aa6a19933e5c8ab409d510d980b8ed634a630e1
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320912"
---
# <a name="patching-per-user-managed-applications"></a><span data-ttu-id="072b9-103">Applicazione di patch Per-User applicazioni gestite</span><span class="sxs-lookup"><span data-stu-id="072b9-103">Patching Per-User Managed Applications</span></span>

<span data-ttu-id="072b9-104">A partire da Windows Installer 3,0, è possibile applicare patch a un'applicazione installata in un contesto gestito per utente dopo la registrazione della patch con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="072b9-104">Beginning with Windows Installer 3.0, it is possible to apply patches to an application that has been installed in a per-user-managed context after the patch has been registered as having elevated privileges.</span></span>

<span data-ttu-id="072b9-105">**Windows Installer 2,0:** Non supportato.</span><span class="sxs-lookup"><span data-stu-id="072b9-105">**Windows Installer 2.0:** Not supported.</span></span> <span data-ttu-id="072b9-106">Non è possibile applicare patch alle applicazioni installate in un contesto gestito per utente usando versioni di Windows Installer precedenti Windows Installer 3,0.</span><span class="sxs-lookup"><span data-stu-id="072b9-106">You cannot apply patches to applications that are installed in a per-user managed context using versions of Windows Installer earlier than Windows Installer 3.0.</span></span>

<span data-ttu-id="072b9-107">Un'applicazione viene installata nello stato gestito per singolo utente nei casi seguenti.</span><span class="sxs-lookup"><span data-stu-id="072b9-107">An application is installed in the per-user-managed state in the following cases.</span></span>

-   <span data-ttu-id="072b9-108">L'installazione per utente dell'applicazione è stata eseguita utilizzando la distribuzione e [criteri di gruppo](/previous-versions/windows/desktop/Policy/group-policy-start-page).</span><span class="sxs-lookup"><span data-stu-id="072b9-108">The per-user installation of the application was performed using deployment and [Group Policy](/previous-versions/windows/desktop/Policy/group-policy-start-page).</span></span>
-   <span data-ttu-id="072b9-109">L'applicazione è stata annunciata a un utente specificato e installata dal metodo descritto in [annuncio di un'applicazione Per-User da installare con privilegi elevati](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md).</span><span class="sxs-lookup"><span data-stu-id="072b9-109">The application was advertised to a specified user and installed by the method described in [Advertising a Per-User Application To Be Installed with Elevated Privileges](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md).</span></span>

<span data-ttu-id="072b9-110">I privilegi sono necessari per installare un'applicazione nel contesto gestito per utente; di conseguenza, le reinstallazioni Windows Installer future o le riparazioni dell'applicazione vengono eseguite anche dal programma di installazione con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="072b9-110">Privileges are required to install an application in the per-user-managed context; therefore, future Windows Installer reinstallations or repairs of the application are also performed by the installer using elevated privileges.</span></span> <span data-ttu-id="072b9-111">Ciò significa che l'applicazione può applicare solo patch provenienti da origini attendibili.</span><span class="sxs-lookup"><span data-stu-id="072b9-111">This means that only patches from trusted sources can be applied to the application.</span></span>

<span data-ttu-id="072b9-112">A partire da Windows Installer 3,0, è possibile applicare una patch a un'applicazione gestita per utente dopo la registrazione della patch con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="072b9-112">Beginning with Windows Installer 3.0, you can apply a patch to a per-user managed application after the patch has been registered as having elevated privileges.</span></span> <span data-ttu-id="072b9-113">Per registrare una patch con privilegi elevati, usare la funzione [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) o il metodo [**SourceListAddSource**](patch-sourcelistaddsource.md) dell'oggetto [**patch**](patch-object.md) con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="072b9-113">To register a patch as having elevated privileges, use the [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) function or the [**SourceListAddSource**](patch-sourcelistaddsource.md) method of the [**Patch**](patch-object.md) object, with elevated privileges.</span></span> <span data-ttu-id="072b9-114">Dopo la registrazione della patch, è possibile applicare la patch usando le funzioni [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) o [**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa) , i metodi [**applypatch**](installer-applypatch.md) o [**ApplyMultiplePatches**](installer-applymultiplepatches.md) dell' [**oggetto Installer**](installer-object.md)o l'opzione della [riga di comando](command-line-options.md)/p.</span><span class="sxs-lookup"><span data-stu-id="072b9-114">After registering the patch, you can apply the patch using the [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) or [**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa) functions, [**ApplyPatch**](installer-applypatch.md) or [**ApplyMultiplePatches**](installer-applymultiplepatches.md) methods of the [**Installer Object**](installer-object.md), or the /p [command-line option](command-line-options.md).</span></span>

> [!Note]
> <span data-ttu-id="072b9-115">Una patch può essere registrata con privilegi elevati prima di installare l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="072b9-115">A patch can be registered as having elevated privileges before the application is installed.</span></span> <span data-ttu-id="072b9-116">Quando una patch è stata registrata, rimane registrata fino a quando non viene rimossa l'ultima applicazione registrata per questa patch.</span><span class="sxs-lookup"><span data-stu-id="072b9-116">When a patch has been registered, it remains registered until the last registered application for this patch is removed.</span></span>
> 
> <span data-ttu-id="072b9-117">Le patch applicate a un'applicazione gestita per utente non possono essere rimosse senza rimuovere l'intera applicazione.</span><span class="sxs-lookup"><span data-stu-id="072b9-117">Patches that have been applied to a per-user managed application cannot be removed without removing the entire application.</span></span> <span data-ttu-id="072b9-118">Le registrazioni delle patch per un'applicazione gestita per utente vengono rimosse durante la rimozione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="072b9-118">The patch registrations for a per-user managed application are removed on the removal of the application.</span></span>

<span data-ttu-id="072b9-119">È anche possibile usare questo metodo per consentire a un utente non amministratore di applicare una patch a un'applicazione per computer oppure usare l'applicazione di patch con privilegi minimi descritta nell'applicazione di [patch a controllo dell'account utente (UAC)](user-account-control--uac--patching.md).</span><span class="sxs-lookup"><span data-stu-id="072b9-119">You can also use this method to enable a non-administrator to patch a per-machine application, or you can use least-privilege patching described in [User Account Control (UAC) Patching](user-account-control--uac--patching.md).</span></span>

## <a name="example-1"></a><span data-ttu-id="072b9-120">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="072b9-120">Example 1</span></span>

<span data-ttu-id="072b9-121">Nell'esempio di scripting seguente viene utilizzato il metodo [**SourceListAddSource**](patch-sourcelistaddsource.md) per registrare un pacchetto di patch disponibile nell' \\ \\ esempio di patch dei prodotti server \\ share \\ \\ \\ . msp con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="072b9-121">The following scripting sample uses the [**SourceListAddSource**](patch-sourcelistaddsource.md) method to register a patch package located at \\\\server\\share\\products\\patches\\example.msp as having elevated privileges.</span></span> <span data-ttu-id="072b9-122">Tale patch è quindi pronta per essere applicata a un prodotto gestito per utente.</span><span class="sxs-lookup"><span data-stu-id="072b9-122">That patch is then ready to be applied to a per-user managed product.</span></span>

``` syntax
const msiInstallContextUserManaged = 1
const msiInstallSourceTypeNetwork = 1

const PatchCode = "{XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}"
const UserSid = "S-X-X-XX-XXXXXXXXX-XXXXXXXXX-XXXXXXXXX-XXXXXXX"
const PatchPath = "\\server\share\products\patches\"
const PatchPackageName = "example.msp"

Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

Set patch = installer.Patch(PatchCode, "", UserSid, msiInstallContextUserManaged)

patch.SourceListAddSource msiInstallSourceTypeNetwork, PatchPath, 0

patch.SourceListInfo("PackageName") = PatchPackageName
```

## <a name="example-2"></a><span data-ttu-id="072b9-123">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="072b9-123">Example 2</span></span>

<span data-ttu-id="072b9-124">Nell'esempio di codice seguente viene usata la funzione [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) per registrare un pacchetto di patch presente in \\ \\ patch di server \\ share \\ Products \\ \\ example. msp con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="072b9-124">The following code sample uses the [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) function to register a patch package located at \\\\server\\share\\products\\patches\\example.msp as having elevated privileges.</span></span> <span data-ttu-id="072b9-125">Tale patch è quindi pronta per essere applicata a un prodotto gestito per utente.</span><span class="sxs-lookup"><span data-stu-id="072b9-125">That patch is then ready to be applied to a per-user managed product.</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif    // UNICODE

#ifndef _WIN32_MSI
#define _WIN32_MSI
#endif    // _WIN32_MSI

#include <windows.h>
#include <msi.h>


/////////////////////////////////////////////////////////////////
// RegisterElevatedPatch
//
// Purpose: register a patch elevated from a network location
//
// Arguments:
//    wszPatchCode <entity type="ndash"/> GUID of patch to be registered
//    wszUserSid   - String SID that specifies the user account
//    wszPatchPath <entity type="ndash"/> Network location of patch
//    wszPatchPackageName <entity type="ndash"/> Package name of patch
//
/////////////////////////////////////////////////////////////////
UINT RegisterElevatedPatch(LPCWSTR wszPatchCode, 
LPCWSTR wszUserSid, 
LPCWSTR wszPatchPath, 
LPCWSTR wszPatchPackageName)
{
// wszUserSid can be NULL
// when wszUserSid is NULL, register patch for current user
// current user must be administrator
if (!wszPatchCode || !wszPatchPath || !wszPatchPackageName)
    return ERROR_INVALID_PARAMETER;

UINT uiReturn = ERROR_SUCCESS;

uiReturn = MsiSourceListAddSourceEx(
/*szPatchCode*/ wszPatchCode,
/*szUserSid*/ wszUserSid,
/*dwContext*/ MSIINSTALLCONTEXT_USERMANAGED,
/*dwOptions*/ MSISOURCETYPE_NETWORK+MSICODE_PATCH,
/*szSource*/ wszPatchPath,
/*dwIndex*/ 0);
if (ERROR_SUCCESS == uiReturn)
{
uiReturn = MsiSourceListSetInfo(
/*szPatchCode*/ wszPatchCode,
/*szUserSid*/ wszUserSid,
/*dwContext*/ MSIINSTALLCONTEXT_USERMANAGED,
/*dwOptions*/ MSISOURCETYPE_NETWORK+MSICODE_PATCH,
/*szProperty*/ L"PackageName",
/*szValue*/ wszPatchPackageName);
if (ERROR_SUCCESS != uiReturn)
{
// Function call failed, return error code
    return uiReturn;
}
}
else
{
// Function call failed, return error code
    return uiReturn;
}

return ERROR_SUCCESS;
}


```



 

 
