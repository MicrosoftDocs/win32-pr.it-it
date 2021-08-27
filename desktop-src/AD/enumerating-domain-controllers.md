---
title: Enumerazione dei controller di dominio
description: Nelle versioni precedenti di Windows, un'applicazione poteva ottenere un solo controller di dominio in un dominio chiamando DsGetDcName.
ms.assetid: bfc92777-6944-406a-8b93-949a1cf3e2c3
ms.tgt_platform: multiple
keywords:
- Esempi di Active Directory Active Directory , enumerazione dei controller di dominio Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54234301ad843708fd4e9b20e38f2b4fd8391e1134a78cea8b0d45a001d701d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118695149"
---
# <a name="enumerating-domain-controllers"></a>Enumerazione dei controller di dominio

Nelle versioni precedenti di Windows, un'applicazione poteva ottenere un solo controller di dominio in un dominio chiamando [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea). Non era possibile stimare quale controller di dominio sarebbe stato recuperato o ottenere un elenco dei controller di dominio. Windows consente a un'applicazione di enumerare i controller di dominio in un dominio usando le funzioni [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena), [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta)e [**DsGetDcClose.**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew)

Per enumerare un controller di dominio, chiamare [**DsGetDcOpen.**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena) Questa funzione accetta parametri che definiscono il dominio da enumerare e altre opzioni di enumerazione. **DsGetDcOpen** fornisce un handle di contesto di enumerazione di dominio usato per identificare l'operazione di enumerazione quando vengono chiamati [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) e [**DsGetDcClose.**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew)

La [**funzione DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) viene chiamata con l'handle del contesto di enumerazione del dominio per recuperare il controller di dominio successivo nell'enumerazione. La prima volta che viene chiamata questa funzione, viene recuperato il primo controller di dominio nell'enumerazione . La seconda volta che questa funzione viene chiamata, viene recuperato il secondo controller di dominio nell'enumerazione . Questo processo viene ripetuto fino a **quando DsGetDcNext** non restituisce **ERROR NO MORE \_ \_ \_ ITEMS**, che indica la fine dell'enumerazione.

La [**funzione DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) enumera i controller di dominio in due gruppi. Il primo gruppo contiene i controller di dominio che coprono il sito del computer in cui viene eseguita la funzione e il secondo gruppo contiene i controller di dominio che non coprono il sito del computer in cui viene eseguita la funzione. Se il flag **DS \_ NOTIFY AFTER \_ SITE \_ \_ RECORDS** è specificato nel parametro *OptionFlags* in [**DsGetDcOpen,**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena)la funzione **DsGetDcNext** restituirà **ERROR \_ FILEMARK \_ DETECTED** dopo il recupero di tutti i controller di dominio specifici del sito. **DsGetDcNext** inizierà quindi l'enumerazione del secondo gruppo, che contiene tutti i controller di dominio nel dominio, inclusi i controller di dominio specifici del sito contenuti nel primo gruppo.

I controller di dominio che gestiscono il sito del computer in cui viene eseguita la funzione vengono enumerati prima di tutto, seguiti dai controller di dominio che non coprono il sito del computer in cui viene eseguita la funzione. Un controller di dominio viene detto per coprire un sito se il controller di dominio è configurato per risiedere in tale sito o se il controller di dominio risiede in un sito più vicino al sito in questione in termini di costo del collegamento tra siti configurato. Se sono presenti controller di dominio sia nel gruppo di controller di dominio che coprono che nel gruppo di controller di dominio che non coprono il sito del computer, i controller di dominio vengono restituiti all'interno del gruppo in base alle priorità e ai pesi configurati specificati in DNS. I controller di dominio con priorità numerica inferiore vengono restituiti prima all'interno di un gruppo. Se all'interno di un gruppo correlato al sito è presente un sottogruppo di più controller di dominio con la stessa priorità, i controller di dominio vengono restituiti in un ordine casuale ponderato in cui i controller di dominio con peso maggiore hanno maggiore probabilità di essere restituiti per primi. I siti, le priorità e i pesi vengono configurati dall'amministratore di dominio per ottenere prestazioni efficaci e bilanciamento del carico tra più controller di dominio disponibili nel dominio. Per questo scopo, le applicazioni che usano le funzioni [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena) / [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) / [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) sfruttano automaticamente queste ottimizzazioni.

Quando l'enumerazione è completa o non è più necessaria, l'enumerazione deve essere chiusa chiamando [**DsGetDcClose con**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) l'handle del contesto di enumerazione del dominio.

Per reimpostare l'enumerazione, è necessario chiudere l'enumerazione corrente chiamando [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) e quindi riaprire l'enumerazione chiamando [**di nuovo DsGetDcOpen.**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena)

## <a name="example"></a>Esempio

Nell'esempio di codice seguente viene illustrato come usare queste funzioni per enumerare i controller di dominio nel dominio locale.


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



 

 




