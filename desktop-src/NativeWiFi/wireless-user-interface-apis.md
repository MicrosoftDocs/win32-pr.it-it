---
description: Windows 8, Windows Server 2012 e versioni successive includono una nuova funzionalità Gestione connessioni che consente agli utenti di connettersi facilmente a Internet e ad altre reti ,ad esempio reti aziendali e domestiche.
ms.assetid: 6b2f5a50-fabd-4c80-acc8-a0883c939632
title: API Interfaccia utente wireless
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e2b2af7faccc5452163ad89ed28d12e7de917f4b872011165e0cfb1760657dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118619928"
---
# <a name="wireless-user-interface-apis"></a>API Interfaccia utente wireless

Windows 8, Windows Server 2012 e versioni successive includono una nuova funzionalità Gestione connessioni che consente agli utenti di connettersi facilmente a Internet e ad altre reti ,ad esempio reti aziendali e domestiche. Questa nuova Gestione connessioni sostituisce le versioni precedenti **Connessione** a una rete e le interfacce utente di Gestione reti **wireless** incluse con le versioni precedenti di Windows per la gestione delle connessioni Wi-Fi native.

In Windows 7, Windows Server 2008 e Windows Vista sono disponibili alcune interfacce utente usate per connettersi o configurare una rete wireless. Queste interfaccia utente possono essere avviate in un'applicazione usando il Wi-Fi nativo e Windows shell. Queste informazioni utente non sono disponibili in Windows 8, Windows Server 2012 e versioni successive.

**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Non è possibile avviare alcuna interfaccia utente usata per connettersi o configurare una rete wireless in un'applicazione a livello di codice.

## <a name="connect-to-a-network"></a>Connessione a una rete

In Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 e Windows Vista, la procedura guidata **Connessione a una** rete può essere usata per stabilire una connessione a una rete wireless. È possibile usare la [**funzione ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) per avviare la **Connessione a una procedura guidata di** rete.

Il codice seguente illustra una [**chiamata ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) che avvia il Connessione **a una procedura guidata di** rete.


```C++
#ifndef UNICODE
#define UNICODE
#endif

#include <windows.h>
#include <shellapi.h>

// Need to link with shell32.lib
#pragma comment(lib, "shell32.lib")

void wmain()
{
   ShellExecute(
      NULL, 
      L"open", 
      L"shell:::{21EC2020-3AEA-1069-A2DD-08002B30309D}\\::{38a98528-6cbf-4ca9-8dc0-b1e1d10f7b1b}",
      NULL,
      NULL,
      SW_SHOWNORMAL);
}
```



## <a name="manage-wireless-networks"></a>**Gestire reti wireless**

In Windows 7, Windows Server 2008 e Windows Vista, l'elemento Manage **Wireless Networks** Pannello di controllo viene usato per gestire i profili di rete wireless. La [**funzione ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) può essere usata anche per avviare l'elemento **Gestisci reti wireless.** Il percorso da usare quando si chiama **ShellExecute** Windows 7 e Windows Vista è il seguente:

`shell:::{26EE0668-A00A-44D7-9371-BEB064C98683}\3\::{1fa9085f-25a2-489b-85d4-86326eedcd87}  `.

Il codice di esempio seguente illustra come usare [**ShellExecute per**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) avviare la **procedura guidata Reti wireless** gestite da un'applicazione.


```C++
#ifndef UNICODE
#define UNICODE
#endif

#include <windows.h>
#include <shellapi.h>
#include <stdio.h>

// Need to link with shell32.lib
#pragma comment(lib, "shell32.lib")

int wmain()
{

    //-----------------------------------------
    // Declare and initialize variables
    HINSTANCE nResult;

    PCWSTR lpOperation = L"open";    
    PCWSTR lpFile= 
        L"shell:::{26EE0668-A00A-44D7-9371-BEB064C98683}\\3\\::{1fa9085f-25a2-489b-85d4-86326eedcd87}";

    nResult = ShellExecute(
        NULL,   // Hwnd
        lpOperation, // do not request elevation unless needed
        lpFile,
        NULL, // no parameters 
        NULL, // use current working directory 
        SW_SHOWNORMAL);

    if((int)nResult == SE_ERR_ACCESSDENIED)
    {
        wprintf(L"ShellExecute returned access denied\n");
        wprintf(L"  Executing the ShellExecute command elevated\n"); 

        nResult = ShellExecute(
            NULL,
            L"runas", // Trick for requesting elevation
            lpFile,
            NULL, // no parameters 
            NULL, // use current working directory 
            SW_HIDE);
    }

    if ( (int) nResult < 32) {
        wprintf(L" ShellExecute failed with error %d\n", (int) nResult);
        return 1;
    }    
    else {    
        wprintf(L" ShellExecute succeeded and returned value %d\n", (int) nResult);
        return 0;
    }
}

```



## <a name="advanced-settings-for-wireless-network-profiles"></a>Impostazioni Impostazioni profili di rete wireless

Windows Vista e versioni successive includono un'interfaccia utente avanzata usata per visualizzare e modificare le impostazioni avanzate di un profilo di rete wireless. È possibile avviare questa interfaccia utente avanzata chiamando la [**funzione WlanUIEditProfile.**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanuieditprofile)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso del Wi-Fi nativo](using-native-wifi.md)
</dt> <dt>

[Esempi di profili wireless](wireless-profile-samples.md)
</dt> <dt>

[**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea)
</dt> <dt>

[**WlanUIEditProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanuieditprofile)
</dt> </dl>

 

 
