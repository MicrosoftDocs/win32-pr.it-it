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
# <a name="directory-system-agent"></a><span data-ttu-id="e98e1-104">Agente del sistema di directory</span><span class="sxs-lookup"><span data-stu-id="e98e1-104">Directory System Agent</span></span>

<span data-ttu-id="e98e1-105">Il [*Directory System Agent*](/previous-versions/windows/desktop/legacy/ms681901(v=vs.85)) (DSA) è una raccolta di servizi e processi eseguiti in ogni controller di dominio e fornisce l'accesso all'archivio dati.</span><span class="sxs-lookup"><span data-stu-id="e98e1-105">The [*directory system agent*](/previous-versions/windows/desktop/legacy/ms681901(v=vs.85)) (DSA) is a collection of services and processes that run on each domain controller and provides access to the data store.</span></span> <span data-ttu-id="e98e1-106">L'archivio dati è l'archivio fisico dei dati della directory che si trovano su un disco rigido.</span><span class="sxs-lookup"><span data-stu-id="e98e1-106">The data store is the physical store of directory data located on a hard disk.</span></span> <span data-ttu-id="e98e1-107">In Active Directory Domain Services, il DSA fa parte del sottosistema di autorità di sistema locale (LSA).</span><span class="sxs-lookup"><span data-stu-id="e98e1-107">In Active Directory Domain Services, the DSA is part of the local system authority (LSA) subsystem.</span></span> <span data-ttu-id="e98e1-108">I client accedono alla directory usando uno dei meccanismi seguenti supportati da DSA:</span><span class="sxs-lookup"><span data-stu-id="e98e1-108">Clients access the directory using one of the following mechanisms supported by the DSA:</span></span>

-   <span data-ttu-id="e98e1-109">I client LDAP si connettono al DSA usando Lightweight Directory Access Protocol (LDAP).</span><span class="sxs-lookup"><span data-stu-id="e98e1-109">LDAP clients connect to the DSA using the Lightweight Directory Access Protocol (LDAP).</span></span> <span data-ttu-id="e98e1-110">Active Directory Domain Services supportano LDAP 3,0, definito da RFC 3377 e LDAP 2,0, definito da RFC 1777.</span><span class="sxs-lookup"><span data-stu-id="e98e1-110">Active Directory Domain Services support LDAP 3.0, defined by RFC 3377, and LDAP 2.0, defined by RFC 1777.</span></span> <span data-ttu-id="e98e1-111">I client Windows usano LDAP 3,0 per connettersi al DSA.</span><span class="sxs-lookup"><span data-stu-id="e98e1-111">Windows clients use LDAP 3.0 to connect to the DSA.</span></span>
-   <span data-ttu-id="e98e1-112">I client MAPI, ad esempio Microsoft Exchange Server, si connettono al DSA utilizzando l'interfaccia MAPI remote procedure call.</span><span class="sxs-lookup"><span data-stu-id="e98e1-112">MAPI clients such as Microsoft Exchange Server connect to the DSA using the MAPI remote procedure call interface.</span></span>
-   <span data-ttu-id="e98e1-113">DSA in Active Directory Domain Services connettersi tra loro per eseguire la replica usando un'interfaccia di chiamata di procedura remota proprietaria.</span><span class="sxs-lookup"><span data-stu-id="e98e1-113">The DSAs in Active Directory Domain Services connect to each other to perform replication using a proprietary remote procedure call interface.</span></span>

 

 