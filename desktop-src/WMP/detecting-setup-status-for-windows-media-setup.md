---
title: Rilevamento dello stato di installazione per l'installazione di Windows Media
description: Rilevamento dello stato di installazione per l'installazione di Windows Media
ms.assetid: c3acc268-934b-4a10-aab5-4b1764cb4c87
keywords:
- Windows Media Player, rilevamento dello stato di installazione
- Windows Media Player, stato del programma di installazione
- Windows Media Player, ridistribuzione del software
- Media Player di Windows, ridistribuzione del software
- rilevamento dello stato di installazione
- stato dell'installazione
- ridistribuzione del software
- ridistribuzione del software
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e28a4df9b842a1b6491a0ec98ca0a3182630c389
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396719"
---
# <a name="detecting-setup-status-for-windows-media-setup"></a><span data-ttu-id="be178-111">Rilevamento dello stato di installazione per l'installazione di Windows Media</span><span class="sxs-lookup"><span data-stu-id="be178-111">Detecting Setup Status for Windows Media Setup</span></span>

<span data-ttu-id="be178-112">Il codice seguente può essere utilizzato con i pacchetti di ridistribuzione di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="be178-112">The following code can be used with the Windows Media Player redistribution packages.</span></span> <span data-ttu-id="be178-113">Lo stato dell'installazione viene archiviato nella voce del registro di sistema **InstallResult** nella sottochiave seguente:</span><span class="sxs-lookup"><span data-stu-id="be178-113">The installation status is stored in the **InstallResult** registry entry under the following subkey:</span></span>

<span data-ttu-id="be178-114">**Programma \_ di \_ \\ installazione di \\ Microsoft \\ MediaPlayer \\ per HKEY software utente corrente**</span><span class="sxs-lookup"><span data-stu-id="be178-114">**HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\Setup**</span></span>

<span data-ttu-id="be178-115">La voce del registro di sistema **InstallResult** ha il formato seguente.</span><span class="sxs-lookup"><span data-stu-id="be178-115">The **InstallResult** registry entry has the following form.</span></span>



| <span data-ttu-id="be178-116">Nome</span><span class="sxs-lookup"><span data-stu-id="be178-116">Name</span></span>              | <span data-ttu-id="be178-117">Type</span><span class="sxs-lookup"><span data-stu-id="be178-117">Type</span></span>           | <span data-ttu-id="be178-118">valore</span><span class="sxs-lookup"><span data-stu-id="be178-118">Value</span></span>                                                                                                                   |
|-------------------|----------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be178-119">**InstallResult**</span><span class="sxs-lookup"><span data-stu-id="be178-119">**InstallResult**</span></span> | <span data-ttu-id="be178-120">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="be178-120">**REG\_DWORD**</span></span> | <span data-ttu-id="be178-121">**HRESULT** che indica se l'installazione di Windows Media Player è stata completata e se è necessario un riavvio.</span><span class="sxs-lookup"><span data-stu-id="be178-121">An **HRESULT** that indicates whether Windows Media Player installation was successful and whether a restart is needed.</span></span> |



 

<span data-ttu-id="be178-122">Di seguito è riportato un esempio di codice C++ che può essere incorporato in un'applicazione di configurazione chiamante.</span><span class="sxs-lookup"><span data-stu-id="be178-122">Here is example C++ code that could be incorporated into a calling setup application.</span></span> <span data-ttu-id="be178-123">Questo codice imposterà `fSuccess` le `fRebootNeeded` variabili e su **true** o **false**, a seconda dei casi, in base al valore **HRESULT** scritto dal programma di installazione di Windows Media Player nel pacchetto di ridistribuzione dei componenti.</span><span class="sxs-lookup"><span data-stu-id="be178-123">This code will set the `fSuccess` and `fRebootNeeded` variables to **true** or **false**, as appropriate, based on the **HRESULT** value written by Windows Media Player Setup in the component redistribution package.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
 
// If NS_S_REBOOT_REQUIRED is undefined, use 0xD2AF9.
#ifndef NS_S_REBOOT_REQUIRED
#define NS_S_REBOOT_REQUIRED       0xd2af9
#endif
 
int main( void )
{
    HKEY hKey = NULL;
    BOOL fSuccess = FALSE;
    BOOL fRebootNeeded = FALSE;
 
if( ERROR_SUCCESS == RegOpenKeyExA( 
                         HKEY_CURRENT_USER, 
                         "Software\\Microsoft\\MediaPlayer\\Setup", 
                         0, KEY_QUERY_VALUE, &hKey ))
    {
        char szResult[64];
        DWORD dwResult = sizeof( szResult );
 
if( ERROR_SUCCESS == RegQueryValueExA( 
                         hKey, "InstallResult", NULL, NULL, 
                         (LPBYTE)szResult, &dwResult ) )
        {
            sscanf_s( szResult, "%x", &dwResult );
            fSuccess = SUCCEEDED( dwResult );
            fRebootNeeded = ( NS_S_REBOOT_REQUIRED == dwResult );
        }
 
        RegCloseKey( hKey );
    }
 
    if( fSuccess )
    {
        printf( "Setup Succeeded..." );
        if( fRebootNeeded )
            printf( "A restart IS required...\n" );
        else
            printf( "A restart IS NOT required...\n" );
    }
    else
    {
        printf( "Setup Failed..." );
        if( fRebootNeeded )
            printf( "A restart IS required...\n" );
        else
            printf( "A restart IS NOT required...\n" );
    }
 
    return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="be178-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="be178-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be178-125">**Ridistribuzione del software Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="be178-125">**Redistributing Windows Media Player Software**</span></span>](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




