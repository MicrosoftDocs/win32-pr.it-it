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
# <a name="uninstalling-patches"></a>Disinstallazione di patch

A partire da Windows Installer 3,0, è possibile disinstallare alcune patch dalle applicazioni. La patch deve essere una [patch non installabile](uninstallable-patches.md). Quando si usa una versione di Windows Installer inferiore alla versione 3,0, la [rimozione delle patch](removing-patches.md) richiede la disinstallazione del prodotto patch e la reinstallazione del prodotto senza applicare la patch.

**Windows Installer 2,0:** Non supportato. Le patch applicate con una versione di Windows Installer precedente alla Windows Installer 3,0 non sono disinstallabili.

Quando si richiama una disinstallazione di una patch con uno dei metodi seguenti, il programma di installazione tenta di rimuovere la patch dal primo prodotto visibile all'applicazione o all'utente che ha richiesto la disinstallazione. Il programma di installazione cerca i prodotti con patch nell'ordine seguente: gestito dall'utente per utente, non gestito, per computer.

## <a name="uninstalling-a-patch-using-msipatchremove-on-a-command-line"></a>Disinstallazione di una patch tramite MSIPATCHREMOVE in una riga di comando

È possibile disinstallare le patch da un comando usando msiexec.exe e le [Opzioni della riga di comando](command-line-options.md). La riga di comando di esempio seguente rimuove una [patch disinstallabile](uninstallable-patches.md), ad esempio msp, da un'applicazione example.msi, usando la proprietà [**MSIPATCHREMOVE**](msipatchremove.md) e l'opzione della riga di comando/i. Quando si usa/i, l'applicazione con patch può essere identificata dal percorso del pacchetto dell'applicazione (file con estensione msi) o dal [codice del prodotto](product-codes.md)dell'applicazione. In questo esempio, il pacchetto di installazione dell'applicazione si trova in " \\ \\ \\ esempio di prodotti server share \\ \\ \\example.msi" e la proprietà [**ProductCode**](productcode.md) dell'applicazione è "{0C9840E7-7F0B-C648-10F0-4641926FE463}". Il pacchetto di patch si trova in " \\ \\ server \\ share \\ Products \\ example \\ patches \\ example. msp" e il GUID del codice della patch è "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}".

**Msiexec/I {0C9840E7-7F0B-C648-10F0-4641926FE463} MSIPATCHREMOVE = {EB8C947C-78B2-85A0-644D-86CEEF8E07C0}/QB**

## <a name="uninstalling-a-patch-using-the-standard-command-line-options"></a>Disinstallazione di una patch usando le opzioni della riga di comando standard

A partire da Windows Installer versione 3,0, è possibile usare le [Opzioni della riga di comando standard](standard-installer-command-line-options.md) usate dagli aggiornamenti del sistema operativo Microsoft Windows (update.exe) per disinstallare Windows Installer patch da una riga di comando.

La riga di comando seguente è l'equivalente della riga di comando standard della Windows Installer riga di comando usata per disinstallare una patch usando la proprietà [**MSIPATCHREMOVE**](msipatchremove.md) . L'opzione/uninstall usata con l'opzione/Package denota la disinstallazione di una patch. È possibile fare riferimento alla patch con il percorso completo della patch o con il GUID del codice della patch.

**Msiexec/package {0C9840E7-7F0B-C648-10F0-4641926FE463}/Uninstall {EB8C947C-78B2-85A0-644D-86CEEF8E07C0}/passive**

> [!Note]  
> L'opzione/passive standard non è un equivalente esatto dell'opzione Windows Installer/QB.

 

## <a name="uninstalling-a-patch-using-the-removepatches-method"></a>Disinstallazione di una patch tramite il metodo RemovePatches

È possibile disinstallare patch da script usando l'interfaccia di [automazione](automation-interface.md)Windows Installer. Nell'esempio di script seguente viene rimossa una [patch disinstallabile](uninstallable-patches.md), ad esempio msp, da un'applicazione example.msi, utilizzando il metodo [**RemovePatches**](installer-removepatches.md) dell'oggetto [Installer](installer-object.md) . Ogni patch da disinstallare può essere rappresentata dal percorso completo del pacchetto di patch o dal GUID del codice della patch. In questo esempio, il pacchetto di installazione dell'applicazione si trova in " \\ \\ \\ esempio di prodotti server share \\ \\ \\example.msi" e la proprietà [**ProductCode**](productcode.md) dell'applicazione è "{0C9840E7-7F0B-C648-10F0-4641926FE463}". Il pacchetto di patch si trova in " \\ \\ server \\ share \\ Products \\ example \\ patches \\ example. msp" e il GUID del codice della patch è "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}".


```VB
const msiInstallTypeSingleInstance = 2
const PatchList = "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}"
const Product = "{0C9840E7-7F0B-C648-10F0-4641926FE463}"

Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

installer.RemovePatches(PatchList, Product, msiInstallTypeSingleInstance, "")
```



## <a name="uninstalling-a-patch-using-addremove-programs"></a>Disinstallazione di una patch con installazione applicazioni

Con Windows XP, è possibile disinstallare le patch utilizzando Installazione applicazioni.

## <a name="uninstalling-a-patch-using-the-msiremovepatches-function"></a>Disinstallazione di una patch tramite la funzione MsiRemovePatches

Le applicazioni possono disinstallare le patch da altre applicazioni usando le [funzioni Windows Installer](installer-functions.md). Nell'esempio di codice seguente viene rimossa una [patch non installabile](uninstallable-patches.md), ad esempio msp, da un'applicazione example.msi, utilizzando la funzione [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) . È possibile fare riferimento a una patch tramite il percorso completo del pacchetto di patch o il GUID del codice della patch. In questo esempio, il pacchetto di installazione dell'applicazione si trova in " \\ \\ \\ esempio di prodotti server share \\ \\ \\example.msi" e la proprietà [**ProductCode**](productcode.md) dell'applicazione è "{0C9840E7-7F0B-C648-10F0-4641926FE463}". Il pacchetto di patch si trova in " \\ \\ server \\ share \\ Products \\ example \\ patches \\ example. msp" e il GUID del codice della patch è "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}".


```C++
    UINT uiReturn = MsiRemovePatches(
          /*szPatchList=*/TEXT("\\server\\share\\products\\example\\patches\\example.msp"),
          /*szProductCode=*/  TEXT("{0C9840E7-7F0B-C648-10F0-4641926FE463}"),
          /*eUninstallType=*/ INSTALLTYPE_SINGLE_INSTANCE,
          /*szPropertyList=*/ NULL);
```



## <a name="uninstalling-a-patch-from-all-applications-using-msiremovepatches-function"></a>Disinstallazione di una patch da tutte le applicazioni tramite la funzione MsiRemovePatches

Una singola patch può aggiornare più di un prodotto nel computer. Un'applicazione può utilizzare [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) per enumerare tutti i prodotti nel computer e determinare se una patch è stata applicata a una particolare istanza del prodotto. L'applicazione può quindi disinstallare la patch usando [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa). Ad esempio, una singola patch può aggiornare più prodotti se la patch aggiorna un file in un componente condiviso da più prodotti e la patch viene distribuita per aggiornare entrambi i prodotti.

Nell'esempio seguente viene illustrato come un'applicazione può utilizzare il Windows Installer per rimuovere una patch da tutte le applicazioni disponibili per l'utente. Non rimuove la patch dalle applicazioni installate per utente per un altro utente.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sequenza di patch](sequencing-patches.md)
</dt> <dt>

[Rimozione di patch](removing-patches.md)
</dt> <dt>

[Patch disinstallabili](uninstallable-patches.md)
</dt> <dt>

[Patch disinstallare azioni personalizzate](patch-uninstall-custom-actions.md)
</dt> <dt>

[**MSIPATCHREMOVE**](msipatchremove.md)
</dt> <dt>

[**MsiEnumapplicationsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> </dl>

 

 



