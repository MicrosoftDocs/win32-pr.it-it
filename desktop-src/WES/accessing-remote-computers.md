---
title: Accesso ai computer remoti
description: È possibile usare l Windows aPI registro eventi per accedere ai dati nel computer locale o in un computer remoto.
ms.assetid: df789981-0e1c-4d68-9bd5-5d054f1724d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a64bf1b3bded6ba1c72231e85bc78fa7f486739741fea1391c869ad79b457e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032581"
---
# <a name="accessing-remote-computers"></a>Accesso ai computer remoti

È possibile usare l Windows aPI registro eventi per accedere ai dati nel computer locale o in un computer remoto. Per accedere ai dati in un computer remoto, è necessario chiamare la [**funzione EvtOpenSession**](/windows/desktop/api/WinEvt/nf-winevt-evtopensession) per creare un contesto di sessione remota. Quando si chiama questa funzione, specificare il nome del computer remoto a cui ci si vuole connettere, le credenziali utente da utilizzare per stabilire la connessione e il tipo di autenticazione da usare per autenticare l'utente. Per specificare l'utente corrente, impostare i membri Domain, User e Password su **NULL.**

Quando si chiama Windows aPI registro eventi, si passa l'handle al contesto della sessione remota restituito dalla [**funzione EvtOpenSession.**](/windows/desktop/api/WinEvt/nf-winevt-evtopensession) Per accedere ai dati nel computer locale, passare **NULL** per specificare la sessione predefinita. Per accedere ai dati nel computer remoto, il computer remoto deve abilitare l'eccezione "Gestione registro eventi remoti" Windows firewall; In caso contrario, quando si tenta di utilizzare l'handle di sessione, la chiamata restituirà un errore con RPC \_ S \_ SERVER \_ UNAVAILABLE. Il computer a cui ci si connette deve eseguire Windows Vista o versione successiva.

Nell'esempio seguente viene illustrato come connettersi a un computer remoto.


```C++
#include <windows.h>
#include <stdio.h>
#include <winevt.h>

#pragma comment(lib, "wevtapi.lib")

EVT_HANDLE ConnectToRemote(LPWSTR lpwszRemote);
void EnumProviders(EVT_HANDLE hRemote);

void main(void)
{
    EVT_HANDLE hRemote = NULL;
    LPWSTR pwsComputerName = L"<name of the remote computer goes here>";
    

    // Enumerate the registered providers on the local computer.
    wprintf(L"Registered providers on the local computer\n\n");
    EnumProviders(hRemote);

    hRemote = ConnectToRemote(pwsComputerName);
    if (NULL == hRemote)
    {
        wprintf(L"Failed to connect to remote computer. Error code is %d.\n", GetLastError());
        goto cleanup;
    }

    // Enumerate the registered providers on the remote computer.
    // To access a remote computer, the remote computer must enable 
    // Remote Event Log Management as an exception in the firewall;
    // otherwise, the remote call fails with RPC_S_SERVER_UNAVAILABLE.
    wprintf(L"\n\nRegistered providers on the remote computer\n\n");
    EnumProviders(hRemote);

cleanup:

    if (hRemote)
        EvtClose(hRemote);
}

// Create a session conext for the remote computer. Set the 
// Domain, User, and Password member to NULL to specify
// the current user.
EVT_HANDLE ConnectToRemote(LPWSTR lpwszRemote)
{
    EVT_HANDLE hRemote = NULL;
    EVT_RPC_LOGIN Credentials;

    RtlZeroMemory(&Credentials, sizeof(EVT_RPC_LOGIN));
    Credentials.Server = lpwszRemote;
    Credentials.Domain = NULL; 
    Credentials.User = NULL; 
    Credentials.Password = NULL; 
    Credentials.Flags = EvtRpcLoginAuthNegotiate; 

    // This call creates a remote session context; it does not actually
    // create a connection to the remote computer. The connection to
    // the remote computer happens when you use the context.
    hRemote = EvtOpenSession(EvtRpcLogin, &Credentials, 0, 0);

    SecureZeroMemory(&Credentials, sizeof(EVT_RPC_LOGIN));

    return hRemote;
}

// Enumerate the registered providers on the computer.
void EnumProviders(EVT_HANDLE hRemote)
{
    EVT_HANDLE hPublishers = NULL;
    WCHAR wszPublisherName[255 + 1];
    DWORD dwBufferUsed = 0;
    DWORD status = ERROR_SUCCESS;

    hPublishers = EvtOpenPublisherEnum(hRemote, 0);
    if (NULL == hPublishers)
    {
        wprintf(L"EvtOpenPublisherEnum failed with %d\n", GetLastError());
        goto cleanup;
    }

    while (true)
    {
        if (EvtNextPublisherId(hPublishers, sizeof(wszPublisherName)/sizeof(WCHAR), wszPublisherName, &dwBufferUsed))
        {
            wprintf(L"%s\n", wszPublisherName);
        }
        else
        {
            status = GetLastError();
            if (ERROR_NO_MORE_ITEMS == status)
            {
                break;
            }
            else
            {
                wprintf(L"EvtNextPublisherId failed with 0x%ud\n", GetLastError());
            }
        }
    }

cleanup:

    if (hPublishers)
        EvtClose(hPublishers);
}
```
