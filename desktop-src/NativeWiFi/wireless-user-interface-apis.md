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
# <a name="wireless-user-interface-apis"></a><span data-ttu-id="261d6-103">API dell'interfaccia utente wireless</span><span class="sxs-lookup"><span data-stu-id="261d6-103">Wireless User Interface APIs</span></span>

<span data-ttu-id="261d6-104">Windows 8, Windows Server 2012 e versioni successive includono una nuova funzionalità di gestione connessione che consente agli utenti di connettersi facilmente a Internet e ad altre reti, ad esempio le reti aziendali e domestiche.</span><span class="sxs-lookup"><span data-stu-id="261d6-104">Windows 8, Windows Server 2012, and later include a new Connection Manager feature that allows users to easily connect to the Internet and to other networks (work and home networks, for example).</span></span> <span data-ttu-id="261d6-105">Questa nuova funzionalità di gestione connessione sostituisce la **connessione precedente a una rete** e la gestione delle interfacce utente delle **reti wireless** incluse nelle versioni precedenti di Windows per la gestione delle connessioni Wi-Fi native.</span><span class="sxs-lookup"><span data-stu-id="261d6-105">This new Connection Manager feature replaces the older **Connect to a network** and **Manage Wireless Networks** user interfaces included with older versions of Windows for managing Native Wifi connections.</span></span>

<span data-ttu-id="261d6-106">In Windows 7, Windows Server 2008 e Windows Vista sono disponibili diverse interfacce utente (UI) utilizzate per la connessione o la configurazione di una rete wireless.</span><span class="sxs-lookup"><span data-stu-id="261d6-106">On Windows 7, Windows Server 2008, and Windows Vista, there are a number of user interfaces (UIs) used to connect to or configure a wireless network.</span></span> <span data-ttu-id="261d6-107">Queste interfacce utente possono essere avviate in un'applicazione mediante le funzioni native Wi-Fi e Windows Shell.</span><span class="sxs-lookup"><span data-stu-id="261d6-107">These UIs can be started in an application using Native Wifi and Windows Shell functions.</span></span> <span data-ttu-id="261d6-108">Queste interfacce utente non sono disponibili in Windows 8, Windows Server 2012 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="261d6-108">These UIs are not available on Windows 8, Windows Server 2012, and later.</span></span>

<span data-ttu-id="261d6-109">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Non è possibile avviare alcuna interfaccia utente utilizzata per connettersi o configurare una rete wireless in un'applicazione a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="261d6-109">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** You cannot start any UI used to connect to or configure a wireless network in an application programmatically.</span></span>

## <a name="connect-to-a-network"></a><span data-ttu-id="261d6-110">Connessione a una rete</span><span class="sxs-lookup"><span data-stu-id="261d6-110">Connect to a network</span></span>

<span data-ttu-id="261d6-111">In Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 e Windows Vista, è possibile utilizzare la procedura guidata **Connetti a una rete** per stabilire una connessione a una rete wireless.</span><span class="sxs-lookup"><span data-stu-id="261d6-111">On Windows 8, Windows Server 2012, Windows 7, Windows Server 2008, and Windows Vista, the **Connect to a network** wizard can be used to establish a connection to a wireless network.</span></span> <span data-ttu-id="261d6-112">È possibile utilizzare la funzione [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) per avviare la procedura guidata **Connetti a una rete** .</span><span class="sxs-lookup"><span data-stu-id="261d6-112">You can use the [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) function to start the **Connect to a network** wizard.</span></span>

<span data-ttu-id="261d6-113">Il codice seguente illustra una chiamata [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) che avvia la **connessione guidata a una rete** .</span><span class="sxs-lookup"><span data-stu-id="261d6-113">The following code shows a [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) call that starts the **Connect to a network** wizard.</span></span>


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



## <a name="manage-wireless-networks"></a><span data-ttu-id="261d6-114">**Gestione delle reti wireless**</span><span class="sxs-lookup"><span data-stu-id="261d6-114">**Manage Wireless Networks**</span></span>

<span data-ttu-id="261d6-115">In Windows 7, Windows Server 2008 e Windows Vista, il pannello di controllo **Gestisci reti wireless** viene usato per gestire i profili di rete wireless.</span><span class="sxs-lookup"><span data-stu-id="261d6-115">On Windows 7, Windows Server 2008, and Windows Vista, the **Manage Wireless Networks** Control Panel item is used to manage wireless network profiles.</span></span> <span data-ttu-id="261d6-116">La funzione [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) può essere usata anche per avviare l'elemento **Gestisci reti wireless** .</span><span class="sxs-lookup"><span data-stu-id="261d6-116">The [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) function can also be used to start the **Manage Wireless Networks** item.</span></span> <span data-ttu-id="261d6-117">Il percorso da utilizzare quando si chiama **ShellExecute** in Windows 7 e Windows Vista è il seguente:</span><span class="sxs-lookup"><span data-stu-id="261d6-117">The path to use when calling **ShellExecute** on Windows 7 and Windows Vista is the following:</span></span>

<span data-ttu-id="261d6-118">`shell:::{26EE0668-A00A-44D7-9371-BEB064C98683}\3\::{1fa9085f-25a2-489b-85d4-86326eedcd87}  `.</span><span class="sxs-lookup"><span data-stu-id="261d6-118">`shell:::{26EE0668-A00A-44D7-9371-BEB064C98683}\3\::{1fa9085f-25a2-489b-85d4-86326eedcd87}  `.</span></span>

<span data-ttu-id="261d6-119">Nell'esempio di codice seguente viene illustrato come utilizzare [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) per avviare la procedura guidata **reti wireless gestite** da un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="261d6-119">The following sample code shows how to use [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) to start the **Managed Wireless Networks** wizard from an application.</span></span>


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



## <a name="advanced-settings-for-wireless-network-profiles"></a><span data-ttu-id="261d6-120">Impostazioni avanzate per i profili di rete wireless</span><span class="sxs-lookup"><span data-stu-id="261d6-120">Advanced Settings for Wireless Network Profiles</span></span>

<span data-ttu-id="261d6-121">Windows Vista e versioni successive includono un'interfaccia utente avanzata utilizzata per visualizzare e modificare le impostazioni avanzate di un profilo di rete wireless.</span><span class="sxs-lookup"><span data-stu-id="261d6-121">Windows Vista and later include an advanced user interface that is used to view and edit advanced settings of a wireless network profile.</span></span> <span data-ttu-id="261d6-122">È possibile avviare questa interfaccia utente avanzata chiamando la funzione [**WlanUIEditProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanuieditprofile) .</span><span class="sxs-lookup"><span data-stu-id="261d6-122">You can start this advanced UI by calling the [**WlanUIEditProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanuieditprofile) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="261d6-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="261d6-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="261d6-124">Uso del WiFi nativo</span><span class="sxs-lookup"><span data-stu-id="261d6-124">Using Native Wifi</span></span>](using-native-wifi.md)
</dt> <dt>

[<span data-ttu-id="261d6-125">Esempi di profili wireless</span><span class="sxs-lookup"><span data-stu-id="261d6-125">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> <dt>

[<span data-ttu-id="261d6-126">**ShellExecute**</span><span class="sxs-lookup"><span data-stu-id="261d6-126">**ShellExecute**</span></span>](/windows/win32/api/shellapi/nf-shellapi-shellexecutea)
</dt> <dt>

[<span data-ttu-id="261d6-127">**WlanUIEditProfile**</span><span class="sxs-lookup"><span data-stu-id="261d6-127">**WlanUIEditProfile**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanuieditprofile)
</dt> </dl>

 

 
