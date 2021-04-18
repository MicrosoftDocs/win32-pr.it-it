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
# <a name="patching-per-user-managed-applications"></a>Applicazione di patch Per-User applicazioni gestite

A partire da Windows Installer 3,0, è possibile applicare patch a un'applicazione installata in un contesto gestito per utente dopo la registrazione della patch con privilegi elevati.

**Windows Installer 2,0:** Non supportato. Non è possibile applicare patch alle applicazioni installate in un contesto gestito per utente usando versioni di Windows Installer precedenti Windows Installer 3,0.

Un'applicazione viene installata nello stato gestito per singolo utente nei casi seguenti.

-   L'installazione per utente dell'applicazione è stata eseguita utilizzando la distribuzione e [criteri di gruppo](/previous-versions/windows/desktop/Policy/group-policy-start-page).
-   L'applicazione è stata annunciata a un utente specificato e installata dal metodo descritto in [annuncio di un'applicazione Per-User da installare con privilegi elevati](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md).

I privilegi sono necessari per installare un'applicazione nel contesto gestito per utente; di conseguenza, le reinstallazioni Windows Installer future o le riparazioni dell'applicazione vengono eseguite anche dal programma di installazione con privilegi elevati. Ciò significa che l'applicazione può applicare solo patch provenienti da origini attendibili.

A partire da Windows Installer 3,0, è possibile applicare una patch a un'applicazione gestita per utente dopo la registrazione della patch con privilegi elevati. Per registrare una patch con privilegi elevati, usare la funzione [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) o il metodo [**SourceListAddSource**](patch-sourcelistaddsource.md) dell'oggetto [**patch**](patch-object.md) con privilegi elevati. Dopo la registrazione della patch, è possibile applicare la patch usando le funzioni [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) o [**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa) , i metodi [**applypatch**](installer-applypatch.md) o [**ApplyMultiplePatches**](installer-applymultiplepatches.md) dell' [**oggetto Installer**](installer-object.md)o l'opzione della [riga di comando](command-line-options.md)/p.

> [!Note]
> Una patch può essere registrata con privilegi elevati prima di installare l'applicazione. Quando una patch è stata registrata, rimane registrata fino a quando non viene rimossa l'ultima applicazione registrata per questa patch.
> 
> Le patch applicate a un'applicazione gestita per utente non possono essere rimosse senza rimuovere l'intera applicazione. Le registrazioni delle patch per un'applicazione gestita per utente vengono rimosse durante la rimozione dell'applicazione.

È anche possibile usare questo metodo per consentire a un utente non amministratore di applicare una patch a un'applicazione per computer oppure usare l'applicazione di patch con privilegi minimi descritta nell'applicazione di [patch a controllo dell'account utente (UAC)](user-account-control--uac--patching.md).

## <a name="example-1"></a>Esempio 1

Nell'esempio di scripting seguente viene utilizzato il metodo [**SourceListAddSource**](patch-sourcelistaddsource.md) per registrare un pacchetto di patch disponibile nell' \\ \\ esempio di patch dei prodotti server \\ share \\ \\ \\ . msp con privilegi elevati. Tale patch è quindi pronta per essere applicata a un prodotto gestito per utente.

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

## <a name="example-2"></a>Esempio 2

Nell'esempio di codice seguente viene usata la funzione [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) per registrare un pacchetto di patch presente in \\ \\ patch di server \\ share \\ Products \\ \\ example. msp con privilegi elevati. Tale patch è quindi pronta per essere applicata a un prodotto gestito per utente.


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



 

 
