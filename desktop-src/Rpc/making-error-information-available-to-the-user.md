---
title: Rendere disponibili all'utente informazioni sull'errore
description: Quando un chiamante riceve un errore ed è necessario notificare all'utente l'errore, la presenza di informazioni estese sugli errori deve essere controllata e, se trovata, il chiamante deve rendere disponibili all'utente le informazioni risultanti.
ms.assetid: 18689280-7124-46e4-9341-ad8d0c1705db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18386dbebd443aced4f5680922549c0ecb0eba55
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103857022"
---
# <a name="making-error-information-available-to-the-user"></a><span data-ttu-id="b8342-103">Rendere disponibili all'utente informazioni sull'errore</span><span class="sxs-lookup"><span data-stu-id="b8342-103">Making Error Information Available to the User</span></span>

<span data-ttu-id="b8342-104">Quando un chiamante riceve un errore ed è necessario notificare all'utente l'errore, la presenza di informazioni estese sugli errori deve essere controllata e, se trovata, il chiamante deve rendere disponibili all'utente le informazioni risultanti.</span><span class="sxs-lookup"><span data-stu-id="b8342-104">When a caller receives an error and needs to notify the user of the error, the presence of extended error information should be checked, and if found, the caller should make the resulting information available to the user.</span></span> <span data-ttu-id="b8342-105">Il frammento di codice seguente è un esempio di rendere disponibili queste informazioni all'utente:</span><span class="sxs-lookup"><span data-stu-id="b8342-105">The following code fragment is an example of making this information available to the user:</span></span>


```C++
// Make an API
status = //...
if (status)
    {
    RPC_STATUS Status2;
    RPC_ERROR_ENUM_HANDLE EnumHandle;

    Status2 = RpcErrorStartEnumeration(&EnumHandle);
    if (Status2 == RPC_S_ENTRY_NOT_FOUND)
        {
        //...
        }
    else if (Status2 != RPC_S_OK)
        {
        PrintToConsole("Couldn't get EEInfo: %d\n", Status2);
        //...
        }
    else
        {
        RPC_EXTENDED_ERROR_INFO ErrorInfo;
        int Records;
        BOOL Result;
        BOOL CopyStrings = TRUE;
        BOOL fUseFileTime = TRUE;
        SYSTEMTIME *SystemTimeToUse;
        SYSTEMTIME SystemTimeBuffer;

        while (Status2 == RPC_S_OK)
            {
            ErrorInfo.Version = RPC_EEINFO_VERSION;
            ErrorInfo.Flags = 0;
            ErrorInfo.NumberOfParameters = 4;
            if (fUseFileTime)
                {
                ErrorInfo.Flags |= EEInfoUseFileTime;
                }

            Status2 = RpcErrorGetNextRecord(&EnumHandle, CopyStrings, &ErrorInfo);
            if (Status2 == RPC_S_ENTRY_NOT_FOUND)
                {
                break;
                }
            else if (Status2 != RPC_S_OK)
                {
                PrintToConsole("Couldn't finish enumeration: %d\n", Status2);
                break;
                }
            else
                {
                int i;

                if (ErrorInfo.ComputerName)
                    {
                    PrintToConsole("ComputerName is %S\n", ErrorInfo.ComputerName);
                    if (CopyStrings)
                        {
                        Result = HeapFree(GetProcessHeap(), 0, ErrorInfo.ComputerName);
                        ASSERT(Result);
                        }
                    }
                PrintToConsole("ProcessID is %d\n", ErrorInfo.ProcessID);
                if (fUseFileTime)
                    {
                    Result = FileTimeToSystemTime(&ErrorInfo.u.FileTime, 
                        &SystemTimeBuffer);
                    ASSERT(Result);
                    SystemTimeToUse = &SystemTimeBuffer;
                    }
                else
                    SystemTimeToUse = &ErrorInfo.u.SystemTime;

                PrintToConsole("System Time is: %d/%d/%d %d:%d:%d:%d\n", 
                    SystemTimeToUse->wMonth,
                    SystemTimeToUse->wDay,
                    SystemTimeToUse->wYear,
                    SystemTimeToUse->wHour,
                    SystemTimeToUse->wMinute,
                    SystemTimeToUse->wSecond,
                    SystemTimeToUse->wMilliseconds);
                PrintToConsole("Generating component is %d\n", 
                    ErrorInfo.GeneratingComponent);
                PrintToConsole("Status is %d\n", ErrorInfo.Status);
                PrintToConsole("Detection location is %d\n", 
                    (int)ErrorInfo.DetectionLocation);
                PrintToConsole("Flags is %d\n", ErrorInfo.Flags);
                PrintToConsole("NumberOfParameters is %d\n", 
                    ErrorInfo.NumberOfParameters);
                for (i = 0; i < ErrorInfo.NumberOfParameters; i ++)
                    {
                    switch(ErrorInfo.Parameters[i].ParameterType)
                        {
                        case eeptAnsiString:
                            PrintToConsole("Ansi string: %s\n", 
                                ErrorInfo.Parameters[i].u.AnsiString);
                            if (CopyStrings)
                                {
                                Result = HeapFree(GetProcessHeap(), 0, 
                                    ErrorInfo.Parameters[i].u.AnsiString);
                                ASSERT(Result);
                                }
                            break;

                        case eeptUnicodeString:
                            PrintToConsole("Unicode string: %S\n", 
                                ErrorInfo.Parameters[i].u.UnicodeString);
                            if (CopyStrings)
                                {
                                Result = HeapFree(GetProcessHeap(), 0, 
                                    ErrorInfo.Parameters[i].u.UnicodeString);
                                ASSERT(Result);
                                }
                            break;

                        case eeptLongVal:
                            PrintToConsole("Long val: %d\n", 
                                ErrorInfo.Parameters[i].u.LVal);
                            break;

                        case eeptShortVal:
                            PrintToConsole("Short val: %d\n", 
                                (int)ErrorInfo.Parameters[i].u.SVal);
                            break;

                        case eeptPointerVal:
                            PrintToConsole("Pointer val: %d\n", 
                                ErrorInfo.Parameters[i].u.PVal);
                            break;

                        case eeptNone:
                            PrintToConsole("Truncated\n");
                            break;

                        default:
                            PrintToConsole("Invalid type: %d\n", 
                                ErrorInfo.Parameters[i].ParameterType);
                        }
                    }
                }
            }
        RpcErrorEndEnumeration(&EnumHandle);
        }
    }
```



<span data-ttu-id="b8342-106">In questo esempio le informazioni estese sull'errore vengono scaricate nella console di, ma il componente può renderlo disponibile per l'utente in qualsiasi altro modo.</span><span class="sxs-lookup"><span data-stu-id="b8342-106">In this example the extended error information is dumped to the console, but your component can make it available to the user in any other way.</span></span> <span data-ttu-id="b8342-107">Se il componente sceglie di salvare le informazioni nell'archivio permanente e di visualizzarle in un secondo momento, è spesso più facile usare il formato binario reso disponibile dalle chiamate di funzione [**RpcErrorSaveErrorInfo**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcerrorsaveerrorinfo) e [**RpcErrorLoadErrorInfo**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcerrorloaderrorinfo) .</span><span class="sxs-lookup"><span data-stu-id="b8342-107">If your component chooses to save the information in persistent storage and show it later, it is often easier to use the binary format made available by the [**RpcErrorSaveErrorInfo**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcerrorsaveerrorinfo) and [**RpcErrorLoadErrorInfo**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcerrorloaderrorinfo) function calls.</span></span>

 

 




