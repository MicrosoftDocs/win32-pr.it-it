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
# <a name="enumerating-domain-controllers"></a>Enumerazione dei controller di dominio

Nelle versioni precedenti di Windows, un'applicazione poteva ottenere un solo controller di dominio in un dominio chiamando [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea). Non è stato possibile stimare quale controller di dominio verrebbe recuperato o ottenere un elenco dei controller di dominio. Windows consente a un'applicazione di enumerare i controller di dominio in un dominio utilizzando le funzioni [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena), [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta)e [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) .

Per enumerare un controller di dominio, chiamare [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena). Questa funzione accetta parametri che definiscono il dominio da enumerare e altre opzioni di enumerazione. **DsGetDcOpen** fornisce un handle di contesto dell'enumerazione di dominio usato per identificare l'operazione di enumerazione quando vengono chiamati [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) e [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) .

La funzione [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) viene chiamata con l'handle di contesto dell'enumerazione di dominio per recuperare il controller di dominio successivo nell'enumerazione. La prima volta che questa funzione viene chiamata, viene recuperato il primo controller di dominio nell'enumerazione. La seconda volta che questa funzione viene chiamata, il secondo controller di dominio nell'enumerazione viene recuperato. Questo processo viene ripetuto fino  a quando **DsGetDcNext \_ non restituisce \_ più \_ elementi**, che indica la fine dell'enumerazione.

La funzione [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) enumera i controller di dominio in due gruppi. Il primo gruppo contiene i controller di dominio che coprono il sito del computer in cui viene eseguita la funzione e il secondo gruppo contiene i controller di dominio che non coprono il sito del computer in cui viene eseguita la funzione. Se il **flag \_ DS \_ notify after \_ site \_ Records** viene specificato nel parametro *OptionFlags* in [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena), la funzione **DsGetDcNext** restituirà l' **errore \_ filemark \_ rilevato** dopo che sono stati recuperati tutti i controller di dominio specifici del sito. **DsGetDcNext** inizierà quindi a enumerare il secondo gruppo, che contiene tutti i controller di dominio nel dominio, inclusi i controller di dominio specifici del sito contenuti nel primo gruppo.

I controller di dominio che gestiscono il sito del computer in cui viene eseguita la funzione vengono enumerati per primi, seguiti dai controller di dominio che non coprono il sito del computer in cui viene eseguita la funzione. Un controller di dominio viene detto che copre un sito se il controller di dominio è configurato per risiedere in tale sito o se il controller di dominio risiede in un sito più vicino al sito in questione in termini di costo del collegamento tra siti configurati. Se sono presenti controller di dominio sia nel gruppo di controller di dominio che coprono che nel gruppo di controller di dominio che non coprono il sito del computer, i controller di dominio vengono restituiti all'interno del gruppo in ordine di priorità e pesi configurati specificati in DNS. I controller di dominio con priorità numerica inferiore vengono restituiti prima in un gruppo. Se all'interno di un gruppo correlato al sito è presente un sottogruppo di diversi controller di dominio con la stessa priorità, i controller di dominio vengono restituiti in un ordine casuale ponderato in cui i controller di dominio con un peso maggiore hanno una maggiore probabilità di essere restituiti per primi. I siti, le priorità e i pesi sono configurati dall'amministratore di dominio per ottenere prestazioni effettive e bilanciamento del carico tra più controller di dominio disponibili nel dominio. Per questo motivo, le applicazioni che usano [](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena)le / [](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) / funzioni [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) DsGetDcNext di DsGetDcOpen sfruttano automaticamente queste ottimizzazioni.

Quando l'enumerazione è completa o non è più necessaria, l'enumerazione deve essere chiusa chiamando [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) con l'handle di contesto dell'enumerazione di dominio.

Per reimpostare l'enumerazione, è necessario chiudere l'enumerazione corrente chiamando [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) e quindi riaprire l'enumerazione chiamando di nuovo [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena) .

## <a name="example"></a>Esempio

Nell'esempio di codice seguente viene illustrato come utilizzare queste funzioni per enumerare i controller di dominio nel dominio locale.


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



 

 




