---
title: Agente del sistema di directory
description: Il Directory System Agent (DSA) è una raccolta di servizi e processi eseguiti in ogni controller di dominio e fornisce l'accesso all'archivio dati.
ms.assetid: a921a822-6b2e-4a84-8112-0ae516443667
ms.tgt_platform: multiple
keywords:
- Directory System Agent Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df39d1670f6668f933c20bcd2b9a8771ce83ec56
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103872322"
---
# <a name="directory-system-agent"></a>Agente del sistema di directory

Il [*Directory System Agent*](/previous-versions/windows/desktop/legacy/ms681901(v=vs.85)) (DSA) è una raccolta di servizi e processi eseguiti in ogni controller di dominio e fornisce l'accesso all'archivio dati. L'archivio dati è l'archivio fisico dei dati della directory che si trovano su un disco rigido. In Active Directory Domain Services, il DSA fa parte del sottosistema di autorità di sistema locale (LSA). I client accedono alla directory usando uno dei meccanismi seguenti supportati da DSA:

-   I client LDAP si connettono al DSA usando Lightweight Directory Access Protocol (LDAP). Active Directory Domain Services supportano LDAP 3,0, definito da RFC 3377 e LDAP 2,0, definito da RFC 1777. I client Windows usano LDAP 3,0 per connettersi al DSA.
-   I client MAPI, ad esempio Microsoft Exchange Server, si connettono al DSA utilizzando l'interfaccia MAPI remote procedure call.
-   DSA in Active Directory Domain Services connettersi tra loro per eseguire la replica usando un'interfaccia di chiamata di procedura remota proprietaria.

 

 