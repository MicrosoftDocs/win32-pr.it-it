---
title: Abilitazione di una funzionalità di accessibilità incorporata
ms.assetid: f97a445d-f93d-4462-bce5-d853f5076b9c
description: 'Altre informazioni su: abilitazione di una funzionalità di accessibilità predefinita'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d860b1410e48f5824923b8b16babb6bcd1527ec9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234324"
---
# <a name="enabling-a-built-in-accessibility-feature"></a><span data-ttu-id="28aa1-103">Abilitazione di una funzionalità di accessibilità incorporata</span><span class="sxs-lookup"><span data-stu-id="28aa1-103">Enabling a Built-in Accessibility Feature</span></span>

<span data-ttu-id="28aa1-104">Il frammento di codice seguente usa la funzione [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) per abilitare la funzionalità filtro tasti:</span><span class="sxs-lookup"><span data-stu-id="28aa1-104">The following code fragment uses the [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) function to enable the FilterKeys feature:</span></span>


```C++
FILTERKEYS fk; 
BOOL bSuccess; 
 
// Fill in the members of the FILTERKEYS structure.  
 
fk.cbSize = sizeof(FILTERKEYS); 
fk.dwFlags = (FKF_FILTERKEYSON | FKF_HOTKEYACTIVE | 
                       FKF_AVAILABLE | FKF_HOTKEYSOUND |
FKF_CLICKON); 
fk.iWaitMSec = 1000; 
fk.iDelayMSec = 1000; 
fk.iRepeatMSec = 500; 
fk.iBounceMSec = 0; 
 
// Call SystemParametersInfo with the SPI_SETFILTERKEYS flag.  
 
bSuccess = SystemParametersInfo(SPI_SETFILTERKEYS, 0, (LPVOID)
&fk, 0); 
```



 

 
