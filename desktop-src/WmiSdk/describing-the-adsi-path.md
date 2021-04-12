---
description: Il protocollo LDAP (Lightweight Directory Access Protocol) richiede l'escape di alcuni caratteri con una barra rovesciata ( \) carattere quando vengono usati in un percorso ADSI (ldap Active Directory Service Interfaces).
ms.assetid: bc04359c-4eda-4574-a9c2-f005a1d92dea
ms.tgt_platform: multiple
title: Descrizione del percorso ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51a6f3f28ffa5faa80dbd9f3d7906bba542e47e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528609"
---
# <a name="describing-the-adsi-path"></a><span data-ttu-id="c95a7-103">Descrizione del percorso ADSI</span><span class="sxs-lookup"><span data-stu-id="c95a7-103">Describing the ADSI Path</span></span>

<span data-ttu-id="c95a7-104">Il protocollo LDAP (Lightweight Directory Access Protocol) richiede l'escape di alcuni caratteri con una barra rovesciata ( \) carattere quando vengono usati in un percorso ADSI (ldap Active Directory Service Interfaces).</span><span class="sxs-lookup"><span data-stu-id="c95a7-104">The Lightweight Directory Access Protocol (LDAP) requires that you escape some characters with a backslash (\) character when you use them in an LDAP Active Directory Service Interfaces (ADSI) path.</span></span>

<span data-ttu-id="c95a7-105">, = +<>\# ; \\ "</span><span class="sxs-lookup"><span data-stu-id="c95a7-105">,=+<>\#;\\"</span></span>

<span data-ttu-id="c95a7-106">Il carattere di escape è necessario solo per il valore della proprietà **ADSIPath** .</span><span class="sxs-lookup"><span data-stu-id="c95a7-106">The escape character is only required for the **ADSIPath** property value.</span></span>

<span data-ttu-id="c95a7-107">Nell'esempio seguente viene illustrato come definire la proprietà **ADSIPath** .</span><span class="sxs-lookup"><span data-stu-id="c95a7-107">The following example shows how to define the **ADSIPath** property.</span></span> <span data-ttu-id="c95a7-108">Si noti che il \# carattere nel valore della proprietà **CN** di ABC è preceduto da un carattere di \# escape.</span><span class="sxs-lookup"><span data-stu-id="c95a7-108">Note that the \# character in the **CN** property value of abc\# is escaped.</span></span>


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
> <span data-ttu-id="c95a7-109">Per ulteriori informazioni sul supporto e l'installazione di questo componente in un sistema operativo specifico, vedere la pagina relativa alla [disponibilità del sistema operativo dei componenti WMI](operating-system-availability-of-wmi-components.md).</span><span class="sxs-lookup"><span data-stu-id="c95a7-109">For more information about support and installation of this component on a specific operating system, see [Operating System Availability of WMI Components](operating-system-availability-of-wmi-components.md).</span></span>

 

 

 



