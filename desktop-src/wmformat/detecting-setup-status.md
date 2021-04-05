---
title: Rilevamento dello stato di installazione
description: Rilevamento dello stato di installazione
ms.assetid: d502a5d6-798b-4269-aef3-1412fc379819
keywords:
- Windows Media Format SDK, ridistribuzione software
- ASF (Advanced Systems Format), ridistribuzione del software
- ASF (formato avanzato dei sistemi), ridistribuzione del software
- Windows Media Format SDK, ridistribuzione
- ASF (Advanced Systems Format), ridistribuzione
- ASF (formato avanzato dei sistemi), ridistribuzione
- ridistribuzione del software, rilevamento dello stato di installazione
- ridistribuzione, rilevamento dello stato di installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6add696f2b2989de1e77d48504a1d540634213d8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714218"
---
# <a name="detecting-setup-status"></a><span data-ttu-id="b9785-111">Rilevamento dello stato di installazione</span><span class="sxs-lookup"><span data-stu-id="b9785-111">Detecting Setup Status</span></span>

<span data-ttu-id="b9785-112">Quando il file eseguibile di ridistribuzione viene eseguito in un computer, registra lo stato di installazione nel registro di sistema come valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b9785-112">When the redistribution executable runs on a computer, it records its installation status in the registry as an **HRESULT** value.</span></span> <span data-ttu-id="b9785-113">Lo stato dell'installazione viene archiviato nella voce del registro di sistema **InstallResult** nella sottochiave seguente:</span><span class="sxs-lookup"><span data-stu-id="b9785-113">The installation status is stored in the **InstallResult** registry entry under the following subkey:</span></span>

<span data-ttu-id="b9785-114">**Programma \_ di \_ \\ installazione di \\ Microsoft \\ MediaPlayer \\ per HKEY software utente corrente**</span><span class="sxs-lookup"><span data-stu-id="b9785-114">**HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\Setup**</span></span>

<span data-ttu-id="b9785-115">La voce del registro di sistema **InstallResult** ha il formato seguente.</span><span class="sxs-lookup"><span data-stu-id="b9785-115">The **InstallResult** registry entry has the following form.</span></span>



| <span data-ttu-id="b9785-116">Nome</span><span class="sxs-lookup"><span data-stu-id="b9785-116">Name</span></span>              | <span data-ttu-id="b9785-117">Type</span><span class="sxs-lookup"><span data-stu-id="b9785-117">Type</span></span>           | <span data-ttu-id="b9785-118">valore</span><span class="sxs-lookup"><span data-stu-id="b9785-118">Value</span></span>                                                                                                                   |
|-------------------|----------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9785-119">**InstallResult**</span><span class="sxs-lookup"><span data-stu-id="b9785-119">**InstallResult**</span></span> | <span data-ttu-id="b9785-120">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="b9785-120">**REG\_DWORD**</span></span> | <span data-ttu-id="b9785-121">**HRESULT** che indica se l'installazione di Windows Media Player è stata completata e se è necessario un riavvio.</span><span class="sxs-lookup"><span data-stu-id="b9785-121">An **HRESULT** that indicates whether Windows Media Player installation was successful and whether a restart is needed.</span></span> |



 

<span data-ttu-id="b9785-122">Il codice seguente imposta le variabili *fSucess* e *fRebootNeeded* su **true** o **false**, a seconda dei casi, in base al valore **HRESULT** scritto dal programma di installazione di Windows Media nel pacchetto di ridistribuzione dei componenti.</span><span class="sxs-lookup"><span data-stu-id="b9785-122">The following code will set the *fSucess* and *fRebootNeeded* variables to **True** or **False**, as appropriate, based on the **HRESULT** value written by Windows Media setup in the component redistribution package.</span></span>


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

    LONG lResult = RegOpenKeyEx( 
        HKEY_CURRENT_USER, 
        TEXT("Software\\Microsoft\\MediaPlayer\\Setup"), 
        0, 
        KEY_QUERY_VALUE, 
        &hKey 
        );

    if ( lResult == ERROR_SUCCESS )
    {
        DWORD dwRegType = 0;   // Registry value type.
        DWORD dwValue = 0;     // Registry value.
        DWORD cbValue = sizeof( dwValue );  // Size of the value in bytes.

        lResult = RegQueryValueEx( 
            hKey, 
            TEXT("InstallResult"), 
            NULL, 
            &dwRegType, 
            (LPBYTE)&dwValue, 
            &cbValue
            );

        if( lResult == ERROR_SUCCESS )
        {
            if (dwRegType == REG_DWORD)
            {
                fSuccess = SUCCEEDED( dwValue );
                fRebootNeeded = ( NS_S_REBOOT_REQUIRED == dwValue );
            }
        }

        RegCloseKey( hKey );
    }

    if( fSuccess )
    {
        printf( "Setup succeeded." );
    }
    else
    {
        printf( "Setup failed." );
    }

    if( fRebootNeeded )
    {
        printf( "A reboot IS required.\n" );
    }
    else
    {
        printf( "A reboot IS NOT required.\n" );
    }
 
    return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="b9785-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b9785-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9785-124">**Ridistribuzione del software**</span><span class="sxs-lookup"><span data-stu-id="b9785-124">**Software Redistribution**</span></span>](software-redistribution.md)
</dt> </dl>

 

 




