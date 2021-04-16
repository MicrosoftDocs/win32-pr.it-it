---
description: Windows 8, Windows Server 2012 e versioni successive includono una nuova funzionalità di gestione connessione che consente agli utenti di connettersi facilmente a Internet e ad altre reti, ad esempio le reti aziendali e domestiche.
ms.assetid: 6b2f5a50-fabd-4c80-acc8-a0883c939632
title: API dell'interfaccia utente wireless
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5814ea8daa55ab3ec1bf431543174cf57fdfa7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530295"
---
# <a name="wireless-user-interface-apis"></a>API dell'interfaccia utente wireless

Windows 8, Windows Server 2012 e versioni successive includono una nuova funzionalità di gestione connessione che consente agli utenti di connettersi facilmente a Internet e ad altre reti, ad esempio le reti aziendali e domestiche. Questa nuova funzionalità di gestione connessione sostituisce la **connessione precedente a una rete** e la gestione delle interfacce utente delle **reti wireless** incluse nelle versioni precedenti di Windows per la gestione delle connessioni Wi-Fi native.

In Windows 7, Windows Server 2008 e Windows Vista sono disponibili diverse interfacce utente (UI) utilizzate per la connessione o la configurazione di una rete wireless. Queste interfacce utente possono essere avviate in un'applicazione mediante le funzioni native Wi-Fi e Windows Shell. Queste interfacce utente non sono disponibili in Windows 8, Windows Server 2012 e versioni successive.

**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Non è possibile avviare alcuna interfaccia utente utilizzata per connettersi o configurare una rete wireless in un'applicazione a livello di codice.

## <a name="connect-to-a-network"></a>Connessione a una rete

In Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 e Windows Vista, è possibile utilizzare la procedura guidata **Connetti a una rete** per stabilire una connessione a una rete wireless. È possibile utilizzare la funzione [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) per avviare la procedura guidata **Connetti a una rete** .

Il codice seguente illustra una chiamata [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) che avvia la **connessione guidata a una rete** .


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



## <a name="manage-wireless-networks"></a>**Gestione delle reti wireless**

In Windows 7, Windows Server 2008 e Windows Vista, il pannello di controllo **Gestisci reti wireless** viene usato per gestire i profili di rete wireless. La funzione [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) può essere usata anche per avviare l'elemento **Gestisci reti wireless** . Il percorso da utilizzare quando si chiama **ShellExecute** in Windows 7 e Windows Vista è il seguente:

`shell:::{26EE0668-A00A-44D7-9371-BEB064C98683}\3\::{1fa9085f-25a2-489b-85d4-86326eedcd87}  `.

Nell'esempio di codice seguente viene illustrato come utilizzare [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) per avviare la procedura guidata **reti wireless gestite** da un'applicazione.


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



## <a name="advanced-settings-for-wireless-network-profiles"></a>Impostazioni avanzate per i profili di rete wireless

Windows Vista e versioni successive includono un'interfaccia utente avanzata utilizzata per visualizzare e modificare le impostazioni avanzate di un profilo di rete wireless. È possibile avviare questa interfaccia utente avanzata chiamando la funzione [**WlanUIEditProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanuieditprofile) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso del WiFi nativo](using-native-wifi.md)
</dt> <dt>

[Esempi di profili wireless](wireless-profile-samples.md)
</dt> <dt>

[**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea)
</dt> <dt>

[**WlanUIEditProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanuieditprofile)
</dt> </dl>

 

 
