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
# <a name="describing-the-adsi-path"></a>Descrizione del percorso ADSI

Il Lightweight Directory Access Protocol (LDAP) richiede l'escape di alcuni caratteri con una barra rovesciata ( ) quando vengono utilizzati in un percorso \\ ADSI (Active Directory Service Interface) LDAP.

,=+<>\# ; \\ "

Il carattere di escape è necessario solo per il **valore della proprietà ADSIPath.**

Nell'esempio seguente viene illustrato come definire **la proprietà ADSIPath.** Si noti che \# il carattere nel valore della proprietà **CN** di abc \# è preceduto da un carattere di escape.


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
> Per altre informazioni sul supporto e sull'installazione di questo componente in un sistema operativo specifico, vedere Disponibilità del sistema [operativo dei componenti WMI.](operating-system-availability-of-wmi-components.md)

 

 

 



