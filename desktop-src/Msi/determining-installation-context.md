---
description: Un'applicazione può chiamare le funzioni MsiEnumProducts o MsiEnumProductsEx per enumerare i prodotti installati o annunciati nel sistema.
ms.assetid: 162bda20-0c62-4eac-8c1f-fd107e42c528
title: Determinazione del contesto di installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89c3ea847a410c5d253061e93153da4462e3cdd8ae8da12b4b6b701812d37d89
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764261"
---
# <a name="determining-installation-context"></a>Determinazione del contesto di installazione

Un'applicazione può chiamare [**le funzioni MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa) o [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) per enumerare i prodotti installati o annunciati nel sistema. Questa funzione può enumerare tutti i prodotti installati nel contesto di installazione per [computer.](installation-context.md) Può enumerare i prodotti installati nel contesto per utente per l'utente corrente. L'applicazione può recuperare informazioni sul contesto di questi prodotti chiamando le [**funzioni MsiGetProductInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa) [**o MsiGetProductInfo.**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)

Il Windows installer può installare i prodotti per l'esecuzione con privilegi elevati (di sistema) per gli utenti non amministratori. Questa operazione richiede l'autorizzazione di un utente amministratore. Un prodotto installato con privilegi elevati è denominato "gestito". Vengono gestiti tutti i prodotti installati per computer. I prodotti installati per utente vengono gestiti solo se un agente di sistema locale esegue un annuncio durante la rappresentazione di un utente. Questo è il metodo usato dalla distribuzione software [tramite Criteri di gruppo](/previous-versions/windows/desktop/Policy/group-policy-start-page). Le applicazioni per utente installate mentre [i criteri AlwaysInstallElevated](alwaysinstallelevated.md) sono impostati non vengono considerate gestite. Chiamando [**MsiIsProductElevated,**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda)un'applicazione può controllare se un determinato prodotto è gestito.

L'esempio seguente illustra come un'applicazione determina il contesto usando [**MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa), [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)e [**MsiIsProductElevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda).


```C++
#ifndef UNICODE
#define UNICODE
#endif //UNICODE

#ifndef _WIN32_MSI
#define _WIN32_MSI 200
#endif //_WIN32_MSI

#include <stdio.h>
#include <windows.h>
#include <msi.h>
#pragma comment(lib, "msi.lib")

const int cchGUID = 38;

UINT DetermineContextForAllProducts()
{
    WCHAR wszProductCode[cchGUID+1] = {0};
    WCHAR wszAssignmentType[10] = {0};
    DWORD cchAssignmentType = 
            sizeof(wszAssignmentType)/sizeof(wszAssignmentType[0]);
    DWORD dwIndex = 0;

    DWORD cchProductName = MAX_PATH;
    WCHAR* lpProductName = new WCHAR[cchProductName];
    if (!lpProductName)
    {
        return ERROR_OUTOFMEMORY;
    }

    UINT uiStatus = ERROR_SUCCESS;

    // enumerate all visible products
    do
    {
        uiStatus = MsiEnumProducts(dwIndex,
                          wszProductCode);
        if (ERROR_SUCCESS == uiStatus)
        {
            cchAssignmentType = 
                sizeof(wszAssignmentType)/sizeof(wszAssignmentType[0]);
            BOOL fPerMachine = FALSE;
            BOOL fManaged = FALSE;

            // Determine assignment type of product
            // This indicates whether the product
            // instance is per-user or per-machine
            if (ERROR_SUCCESS == 
                MsiGetProductInfo(wszProductCode,INSTALLPROPERTY_ASSIGNMENTTYPE,wszAssignmentType,&cchAssignmentType))
            {
                if (L'1' == wszAssignmentType[0])
                    fPerMachine = TRUE;
            }
            else
            {
                // This halts the enumeration and fails. Alternatively the error
                // could be logged and enumeration continued for the
                // remainder of the products
                uiStatus = ERROR_FUNCTION_FAILED;
                break;
            }

            // determine the "managed" status of the product.
            // If fManaged is TRUE, product is installed managed
            // and runs with elevated privileges.
            // If fManaged is FALSE, product installation operations
            // run as the user.
            if (ERROR_SUCCESS != MsiIsProductElevated(wszProductCode,
                                         &fManaged))
            {
                // This halts the enumeration and fails. Alternatively the error
                // could be logged and enumeration continued for the
                // remainder of the products
                uiStatus = ERROR_FUNCTION_FAILED;
                break;
            }

            // obtain the user friendly name of the product
            UINT uiReturn = MsiGetProductInfo(wszProductCode,INSTALLPROPERTY_PRODUCTNAME,lpProductName,&cchProductName);
            if (ERROR_MORE_DATA == uiReturn)
            {
                // try again, but with a larger product name buffer
                delete [] lpProductName;

                // returned character count does not include
                // terminating NULL
                ++cchProductName;

                lpProductName = new WCHAR[cchProductName];
                if (!lpProductName)
                {
                    uiStatus = ERROR_OUTOFMEMORY;
                    break;
                }

                uiReturn = MsiGetProductInfo(wszProductCode,INSTALLPROPERTY_PRODUCTNAME,lpProductName,&cchProductName);
            }

            if (ERROR_SUCCESS != uiReturn)
            {
                // This halts the enumeration and fails. Alternatively the error
                // could be logged and enumeration continued for the
                // remainder of the products
                uiStatus = ERROR_FUNCTION_FAILED;
                break;
            }

            // output information
            wprintf(L" Product %s:\n", lpProductName);
            wprintf(L"\t%s\n", wszProductCode);
                        wprintf(L"\tInstalled %s %s\n", 
                fPerMachine ? L"per-machine" : L"per-user",
                fManaged ? L"managed" : L"non-managed");
        }
        dwIndex++;
    }
    while (ERROR_SUCCESS == uiStatus);

    if (lpProductName)
    {
        delete [] lpProductName;
        lpProductName = NULL;
    }

    return (ERROR_NO_MORE_ITEMS == uiStatus) ? ERROR_SUCCESS : uiStatus;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa)
</dt> <dt>

[**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)
</dt> <dt>

[**MsiGetProductInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa)
</dt> <dt>

[**MsiIsProductElevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda)
</dt> <dt>

[Installazione di un pacchetto con privilegi elevati per un utente non amministratore](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
</dt> <dt>

[Annuncio di Per-User'applicazione da installare con privilegi elevati](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md)
</dt> <dt>

[Contesto di installazione](installation-context.md)
</dt> </dl>

 

 
