---
description: Un'applicazione può chiamare le funzioni MsiEnumProducts o MsiEnumProductsEx per enumerare i prodotti installati o annunciati nel sistema.
ms.assetid: 162bda20-0c62-4eac-8c1f-fd107e42c528
title: Determinazione del contesto di installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24367e2367f845dfef2e4947a32d9dec84d644cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314288"
---
# <a name="determining-installation-context"></a><span data-ttu-id="b000c-103">Determinazione del contesto di installazione</span><span class="sxs-lookup"><span data-stu-id="b000c-103">Determining Installation Context</span></span>

<span data-ttu-id="b000c-104">Un'applicazione può chiamare le funzioni [**MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa) o [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) per enumerare i prodotti installati o annunciati nel sistema.</span><span class="sxs-lookup"><span data-stu-id="b000c-104">An application can call the [**MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa) or [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) functions to enumerate products that are installed or advertised on the system.</span></span> <span data-ttu-id="b000c-105">Questa funzione può enumerare tutti i prodotti installati nel [contesto di installazione](installation-context.md)per computer.</span><span class="sxs-lookup"><span data-stu-id="b000c-105">This function can enumerate all the products installed in the per-machine [installation context](installation-context.md).</span></span> <span data-ttu-id="b000c-106">Può enumerare i prodotti installati nel contesto per utente per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="b000c-106">It can enumerate the products installed in the per-user context for the current user.</span></span> <span data-ttu-id="b000c-107">L'applicazione può recuperare informazioni sul contesto di questi prodotti chiamando le funzioni [**MsiGetProductInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa) o [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa) .</span><span class="sxs-lookup"><span data-stu-id="b000c-107">The application can retrieve information about the context of these products by calling the [**MsiGetProductInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa) or [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa) functions.</span></span>

<span data-ttu-id="b000c-108">Il Windows Installer può installare i prodotti per l'esecuzione con privilegi elevati (di sistema) per gli utenti non amministratori.</span><span class="sxs-lookup"><span data-stu-id="b000c-108">The Windows Installer can install products to run with elevated (system) privileges for non-administrator users.</span></span> <span data-ttu-id="b000c-109">Questa operazione richiede l'autorizzazione di un utente amministratore.</span><span class="sxs-lookup"><span data-stu-id="b000c-109">This requires the permission of an administrator user.</span></span> <span data-ttu-id="b000c-110">Un prodotto installato con privilegi elevati è denominato "gestito".</span><span class="sxs-lookup"><span data-stu-id="b000c-110">A product that is installed with elevated privileges is called "managed."</span></span> <span data-ttu-id="b000c-111">Tutti i prodotti installati per computer vengono gestiti.</span><span class="sxs-lookup"><span data-stu-id="b000c-111">All products installed per-machine are managed.</span></span> <span data-ttu-id="b000c-112">I prodotti installati per utente vengono gestiti solo se un agente di sistema locale esegue un annuncio durante la rappresentazione di un utente.</span><span class="sxs-lookup"><span data-stu-id="b000c-112">Products installed per-user are only managed if a local system agent performs an advertisement while impersonating a user.</span></span> <span data-ttu-id="b000c-113">Questo è il metodo usato dalla distribuzione software tramite [criteri di gruppo](/previous-versions/windows/desktop/Policy/group-policy-start-page).</span><span class="sxs-lookup"><span data-stu-id="b000c-113">This is the method used by software deployment through [Group Policy](/previous-versions/windows/desktop/Policy/group-policy-start-page).</span></span> <span data-ttu-id="b000c-114">Le applicazioni per utente installate mentre i criteri [AlwaysInstallElevated](alwaysinstallelevated.md) sono impostati non vengono considerati gestiti.</span><span class="sxs-lookup"><span data-stu-id="b000c-114">Per-user applications installed while the [AlwaysInstallElevated](alwaysinstallelevated.md) policies are set are not considered managed.</span></span> <span data-ttu-id="b000c-115">Chiamando [**MsiIsProductElevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda), un'applicazione può verificare se un determinato prodotto è gestito.</span><span class="sxs-lookup"><span data-stu-id="b000c-115">By calling [**MsiIsProductElevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda), an application can check whether a particular product is managed.</span></span>

<span data-ttu-id="b000c-116">Nell'esempio seguente viene illustrato il modo in cui un'applicazione determina il contesto utilizzando [**MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa), [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)e [**MsiIsProductElevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda).</span><span class="sxs-lookup"><span data-stu-id="b000c-116">The following sample demonstrates how an application determines context by using [**MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa), [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa), and [**MsiIsProductElevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="b000c-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b000c-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b000c-118">**MsiEnumProducts**</span><span class="sxs-lookup"><span data-stu-id="b000c-118">**MsiEnumProducts**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumproductsa)
</dt> <dt>

[<span data-ttu-id="b000c-119">**MsiGetProductInfo**</span><span class="sxs-lookup"><span data-stu-id="b000c-119">**MsiGetProductInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)
</dt> <dt>

[<span data-ttu-id="b000c-120">**MsiGetProductInfoEx**</span><span class="sxs-lookup"><span data-stu-id="b000c-120">**MsiGetProductInfoEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa)
</dt> <dt>

[<span data-ttu-id="b000c-121">**MsiIsProductElevated**</span><span class="sxs-lookup"><span data-stu-id="b000c-121">**MsiIsProductElevated**</span></span>](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda)
</dt> <dt>

[<span data-ttu-id="b000c-122">Installazione di un pacchetto con privilegi elevati per un amministratore non</span><span class="sxs-lookup"><span data-stu-id="b000c-122">Installing a Package with Elevated Privileges for a Non-Admin</span></span>](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
</dt> <dt>

[<span data-ttu-id="b000c-123">Annuncio di un'applicazione Per-User da installare con privilegi elevati</span><span class="sxs-lookup"><span data-stu-id="b000c-123">Advertising a Per-User Application To Be Installed with Elevated Privileges</span></span>](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md)
</dt> <dt>

[<span data-ttu-id="b000c-124">Contesto di installazione</span><span class="sxs-lookup"><span data-stu-id="b000c-124">Installation Context</span></span>](installation-context.md)
</dt> </dl>

 

 
