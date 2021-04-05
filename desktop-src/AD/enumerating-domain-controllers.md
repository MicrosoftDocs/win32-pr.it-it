---
title: Enumerazione dei controller di dominio
description: Nelle versioni precedenti di Windows, un'applicazione poteva ottenere un solo controller di dominio in un dominio chiamando DsGetDcName.
ms.assetid: bfc92777-6944-406a-8b93-949a1cf3e2c3
ms.tgt_platform: multiple
keywords:
- Esempi di Active Directory Active Directory, enumerazione dei controller di dominio Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94384bb8c62edb7b0d45328dabe7765a43e4e610
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707696"
---
# <a name="enumerating-domain-controllers"></a><span data-ttu-id="14c3c-104">Enumerazione dei controller di dominio</span><span class="sxs-lookup"><span data-stu-id="14c3c-104">Enumerating Domain Controllers</span></span>

<span data-ttu-id="14c3c-105">Nelle versioni precedenti di Windows, un'applicazione poteva ottenere un solo controller di dominio in un dominio chiamando [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea).</span><span class="sxs-lookup"><span data-stu-id="14c3c-105">In earlier versions of Windows, an application could only obtain a single domain controller in a domain by calling [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea).</span></span> <span data-ttu-id="14c3c-106">Non è stato possibile stimare quale controller di dominio verrebbe recuperato o ottenere un elenco dei controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="14c3c-106">There was no way to predict which domain controller would be retrieved or to obtain a list of the domain controllers.</span></span> <span data-ttu-id="14c3c-107">Windows consente a un'applicazione di enumerare i controller di dominio in un dominio utilizzando le funzioni [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena), [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta)e [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) .</span><span class="sxs-lookup"><span data-stu-id="14c3c-107">Windows enables an application to enumerate the domain controllers in a domain by using the [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena), [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta), and [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) functions.</span></span>

<span data-ttu-id="14c3c-108">Per enumerare un controller di dominio, chiamare [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena).</span><span class="sxs-lookup"><span data-stu-id="14c3c-108">To enumerate a domain controller, call [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena).</span></span> <span data-ttu-id="14c3c-109">Questa funzione accetta parametri che definiscono il dominio da enumerare e altre opzioni di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="14c3c-109">This function takes parameters that define the domain to enumerate and other enumeration options.</span></span> <span data-ttu-id="14c3c-110">**DsGetDcOpen** fornisce un handle di contesto dell'enumerazione di dominio usato per identificare l'operazione di enumerazione quando vengono chiamati [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) e [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) .</span><span class="sxs-lookup"><span data-stu-id="14c3c-110">**DsGetDcOpen** provides a domain enumeration context handle that is used to identify the enumeration operation when [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) and [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) are called.</span></span>

<span data-ttu-id="14c3c-111">La funzione [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) viene chiamata con l'handle di contesto dell'enumerazione di dominio per recuperare il controller di dominio successivo nell'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="14c3c-111">The [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) function is called with the domain enumeration context handle to retrieve the next domain controller in the enumeration.</span></span> <span data-ttu-id="14c3c-112">La prima volta che questa funzione viene chiamata, viene recuperato il primo controller di dominio nell'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="14c3c-112">The first time this function is called, the first domain controller in the enumeration is retrieved.</span></span> <span data-ttu-id="14c3c-113">La seconda volta che questa funzione viene chiamata, il secondo controller di dominio nell'enumerazione viene recuperato.</span><span class="sxs-lookup"><span data-stu-id="14c3c-113">The second time this function is called, the second domain controller in the enumeration is retrieved.</span></span> <span data-ttu-id="14c3c-114">Questo processo viene ripetuto fino  a quando **DsGetDcNext \_ non restituisce \_ più \_ elementi**, che indica la fine dell'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="14c3c-114">This process is repeated until **DsGetDcNext** returns **ERROR\_NO\_MORE\_ITEMS**, that indicates the end of the enumeration.</span></span>

<span data-ttu-id="14c3c-115">La funzione [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) enumera i controller di dominio in due gruppi.</span><span class="sxs-lookup"><span data-stu-id="14c3c-115">The [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) function will enumerate the domain controllers in two groups.</span></span> <span data-ttu-id="14c3c-116">Il primo gruppo contiene i controller di dominio che coprono il sito del computer in cui viene eseguita la funzione e il secondo gruppo contiene i controller di dominio che non coprono il sito del computer in cui viene eseguita la funzione.</span><span class="sxs-lookup"><span data-stu-id="14c3c-116">The first group contains the domain controllers that cover the site of the computer where the function is executed and the second group contains the domain controllers that do not cover the site of the computer where the function is executed.</span></span> <span data-ttu-id="14c3c-117">Se il **flag \_ DS \_ notify after \_ site \_ Records** viene specificato nel parametro *OptionFlags* in [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena), la funzione **DsGetDcNext** restituirà l' **errore \_ filemark \_ rilevato** dopo che sono stati recuperati tutti i controller di dominio specifici del sito.</span><span class="sxs-lookup"><span data-stu-id="14c3c-117">If the **DS\_NOTIFY\_AFTER\_SITE\_RECORDS** flag is specified in the *OptionFlags* parameter in [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena), the **DsGetDcNext** function will return **ERROR\_FILEMARK\_DETECTED** after all of the site-specific domain controllers have been retrieved.</span></span> <span data-ttu-id="14c3c-118">**DsGetDcNext** inizierà quindi a enumerare il secondo gruppo, che contiene tutti i controller di dominio nel dominio, inclusi i controller di dominio specifici del sito contenuti nel primo gruppo.</span><span class="sxs-lookup"><span data-stu-id="14c3c-118">**DsGetDcNext** will then begin enumerating the second group, which contains all domain controllers in the domain, including the site-specific domain controllers contained in the first group.</span></span>

<span data-ttu-id="14c3c-119">I controller di dominio che gestiscono il sito del computer in cui viene eseguita la funzione vengono enumerati per primi, seguiti dai controller di dominio che non coprono il sito del computer in cui viene eseguita la funzione.</span><span class="sxs-lookup"><span data-stu-id="14c3c-119">Domain controllers that handle the site of the computer where the function is executed are enumerated first followed by the domain controllers that do not cover the site of the computer where the function is executed.</span></span> <span data-ttu-id="14c3c-120">Un controller di dominio viene detto che copre un sito se il controller di dominio è configurato per risiedere in tale sito o se il controller di dominio risiede in un sito più vicino al sito in questione in termini di costo del collegamento tra siti configurati.</span><span class="sxs-lookup"><span data-stu-id="14c3c-120">A domain controller is said to cover a site if the domain controller is configured to reside in that site or if the domain controller resides in a site that is nearest to the site in question in terms of the configured inter-site link cost.</span></span> <span data-ttu-id="14c3c-121">Se sono presenti controller di dominio sia nel gruppo di controller di dominio che coprono che nel gruppo di controller di dominio che non coprono il sito del computer, i controller di dominio vengono restituiti all'interno del gruppo in ordine di priorità e pesi configurati specificati in DNS.</span><span class="sxs-lookup"><span data-stu-id="14c3c-121">If there are any domain controllers in both the group of domain controllers that cover and the group of domain controllers that do not cover the computer site, domain controllers are returned within the group in order of their configured priorities and weights that are specified in DNS.</span></span> <span data-ttu-id="14c3c-122">I controller di dominio con priorità numerica inferiore vengono restituiti prima in un gruppo.</span><span class="sxs-lookup"><span data-stu-id="14c3c-122">Domain controllers that have lower numeric priority are returned within a group first.</span></span> <span data-ttu-id="14c3c-123">Se all'interno di un gruppo correlato al sito è presente un sottogruppo di diversi controller di dominio con la stessa priorità, i controller di dominio vengono restituiti in un ordine casuale ponderato in cui i controller di dominio con un peso maggiore hanno una maggiore probabilità di essere restituiti per primi.</span><span class="sxs-lookup"><span data-stu-id="14c3c-123">If within a site-related group there is a subgroup of several domain controllers with the same priority, domain controllers are returned in a weighted random order where domain controllers with higher weight have more probability to be returned first.</span></span> <span data-ttu-id="14c3c-124">I siti, le priorità e i pesi sono configurati dall'amministratore di dominio per ottenere prestazioni effettive e bilanciamento del carico tra più controller di dominio disponibili nel dominio.</span><span class="sxs-lookup"><span data-stu-id="14c3c-124">The sites, priorities, and weights are configured by the domain administrator to achieve effective performance and load balancing among multiple domain controllers available in the domain.</span></span> <span data-ttu-id="14c3c-125">Per questo motivo, le applicazioni che usano [](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena)le / [](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) / funzioni [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) DsGetDcNext di DsGetDcOpen sfruttano automaticamente queste ottimizzazioni.</span><span class="sxs-lookup"><span data-stu-id="14c3c-125">Because of this, applications that use the [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena)/[**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta)/[**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) functions automatically take advantage of these optimizations.</span></span>

<span data-ttu-id="14c3c-126">Quando l'enumerazione è completa o non è più necessaria, l'enumerazione deve essere chiusa chiamando [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) con l'handle di contesto dell'enumerazione di dominio.</span><span class="sxs-lookup"><span data-stu-id="14c3c-126">When the enumeration is complete or is no longer required, the enumeration must be closed by calling [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) with the domain enumeration context handle.</span></span>

<span data-ttu-id="14c3c-127">Per reimpostare l'enumerazione, è necessario chiudere l'enumerazione corrente chiamando [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) e quindi riaprire l'enumerazione chiamando di nuovo [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena) .</span><span class="sxs-lookup"><span data-stu-id="14c3c-127">To reset the enumeration, it is necessary to close the current enumeration by calling [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) and then reopen the enumeration by calling [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena) again.</span></span>

## <a name="example"></a><span data-ttu-id="14c3c-128">Esempio</span><span class="sxs-lookup"><span data-stu-id="14c3c-128">Example</span></span>

<span data-ttu-id="14c3c-129">Nell'esempio di codice seguente viene illustrato come utilizzare queste funzioni per enumerare i controller di dominio nel dominio locale.</span><span class="sxs-lookup"><span data-stu-id="14c3c-129">The following code example shows how to use these functions to enumerate the domain controllers in the local domain.</span></span>


```C++
DWORD dwRet;
PDOMAIN_CONTROLLER_INFO pdcInfo;

// Get a domain controller for the domain this computer is on.
dwRet = DsGetDcName(NULL, NULL, NULL, NULL, 0, &pdcInfo);
if(ERROR_SUCCESS == dwRet)
{
    HANDLE hGetDc;
    
    // Open the enumeration.
    dwRet = DsGetDcOpen(    pdcInfo->DomainName,
                            DS_NOTIFY_AFTER_SITE_RECORDS,
                            NULL,
                            NULL,
                            NULL,
                            0,
                            &hGetDc);
    if(ERROR_SUCCESS == dwRet)
    {
        LPTSTR pszDnsHostName;

        /*
        Enumerate each domain controller and print its name to the 
        debug window.
        */
        while(TRUE)
        {
            ULONG ulSocketCount;
            LPSOCKET_ADDRESS rgSocketAddresses;

            dwRet = DsGetDcNext(
                hGetDc, 
                &ulSocketCount, 
                &rgSocketAddresses, 
                &pszDnsHostName);
            
            if(ERROR_SUCCESS == dwRet)
            {
                OutputDebugString(pszDnsHostName);
                OutputDebugString(TEXT("\n"));
                
                // Free the allocated string.
                NetApiBufferFree(pszDnsHostName);

                // Free the socket address array.
                LocalFree(rgSocketAddresses);
            }
            else if(ERROR_NO_MORE_ITEMS == dwRet)
            {
                // The end of the list has been reached.
                break;
            }
            else if(ERROR_FILEMARK_DETECTED == dwRet)
            {
                /*
                DS_NOTIFY_AFTER_SITE_RECORDS was specified in 
                DsGetDcOpen and the end of the site-specific 
                records was reached.
                */
                OutputDebugString(
                  TEXT("End of site-specific domain controllers\n"));
                continue;
            }
            else
            {
                // Some other error occurred.
                break;
            }
        }
        
        // Close the enumeration.
        DsGetDcClose(hGetDc);
    }
    
    // Free the DOMAIN_CONTROLLER_INFO structure. 
    NetApiBufferFree(pdcInfo);
}
```



 

 




