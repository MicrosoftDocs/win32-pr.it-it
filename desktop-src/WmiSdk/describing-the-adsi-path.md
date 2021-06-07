---
description: Il Lightweight Directory Access Protocol (LDAP) richiede l'uso di caratteri di escape per alcuni caratteri con una barra rovesciata ( quando vengono utilizzati in un percorso \) ADSI (Active Directory Service Interface) LDAP.
ms.assetid: bc04359c-4eda-4574-a9c2-f005a1d92dea
ms.tgt_platform: multiple
title: Descrizione del percorso ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e0ba1dafac273ab3564549a5caca44180161643
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387110"
---
# <a name="describing-the-adsi-path"></a><span data-ttu-id="e8d4d-103">Descrizione del percorso ADSI</span><span class="sxs-lookup"><span data-stu-id="e8d4d-103">Describing the ADSI Path</span></span>

<span data-ttu-id="e8d4d-104">Il Lightweight Directory Access Protocol (LDAP) richiede l'escape di alcuni caratteri con una barra rovesciata ( ) quando vengono utilizzati in un percorso \\ ADSI (Active Directory Service Interface) LDAP.</span><span class="sxs-lookup"><span data-stu-id="e8d4d-104">The Lightweight Directory Access Protocol (LDAP) requires that you escape some characters with a backslash (\\) character when you use them in an LDAP Active Directory Service Interfaces (ADSI) path.</span></span>

<span data-ttu-id="e8d4d-105">,=+<>\# ; \\ "</span><span class="sxs-lookup"><span data-stu-id="e8d4d-105">,=+<>\#;\\"</span></span>

<span data-ttu-id="e8d4d-106">Il carattere di escape è necessario solo per il **valore della proprietà ADSIPath.**</span><span class="sxs-lookup"><span data-stu-id="e8d4d-106">The escape character is only required for the **ADSIPath** property value.</span></span>

<span data-ttu-id="e8d4d-107">Nell'esempio seguente viene illustrato come definire **la proprietà ADSIPath.**</span><span class="sxs-lookup"><span data-stu-id="e8d4d-107">The following example shows how to define the **ADSIPath** property.</span></span> <span data-ttu-id="e8d4d-108">Si noti che \# il carattere nel valore della proprietà **CN** di abc \# è preceduto da un carattere di escape.</span><span class="sxs-lookup"><span data-stu-id="e8d4d-108">Note that the \# character in the **CN** property value of abc\# is escaped.</span></span>


```C++
// #include <windows.h> for this code to compile

BSTR strObjPath = 
    SysAllocString(L"ds_user.ADSIPath=\"LDAP://CN=abc\#,"
                   L"CN=Users,DC=dsprovider,DC=nttest,"
                   L"DC=microsoft,DC=com\"");

// Use strObjectPath here.

SysFreeString(strObjPath); // Free memory resources.
```



> [!Note]  
> <span data-ttu-id="e8d4d-109">Per altre informazioni sul supporto e sull'installazione di questo componente in un sistema operativo specifico, vedere Disponibilità del sistema [operativo dei componenti WMI.](operating-system-availability-of-wmi-components.md)</span><span class="sxs-lookup"><span data-stu-id="e8d4d-109">For more information about support and installation of this component on a specific operating system, see [Operating System Availability of WMI Components](operating-system-availability-of-wmi-components.md).</span></span>

 

 

 



