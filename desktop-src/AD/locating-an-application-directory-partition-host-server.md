---
title: Individuazione di un server host partizione di directory applicativa
description: In questo argomento viene descritto come individuare un server host della partizione di directory applicativa.
ms.assetid: 636e8bc2-136c-42be-aa64-1b059dedf775
ms.tgt_platform: multiple
keywords:
- Individuazione di un'istanza di Active Directory Partition server host
- Directory dell'applicazione partizioni di Active Directory, individuazione di un server host
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5c9e8f80ccf4b1549af9a76e7b588685d38c297
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707606"
---
# <a name="locating-an-application-directory-partition-host-server"></a><span data-ttu-id="7bdab-105">Individuazione di un server host partizione di directory applicativa</span><span class="sxs-lookup"><span data-stu-id="7bdab-105">Locating an Application Directory Partition Host Server</span></span>

<span data-ttu-id="7bdab-106">Il servizio NetLogon registra l'elenco seguente di record SRV per una partizione di directory applicativa:</span><span class="sxs-lookup"><span data-stu-id="7bdab-106">The NetLogon service registers the following list of SRV records for an application directory partition:</span></span>

-   <span data-ttu-id="7bdab-107">\_LDAP. \_ TCP.<partition name></span><span class="sxs-lookup"><span data-stu-id="7bdab-107">\_ldap.\_tcp.<partition name></span></span>
-   <span data-ttu-id="7bdab-108">\_LDAP. \_ TCP. <site name> . \_ siti.<partition name></span><span class="sxs-lookup"><span data-stu-id="7bdab-108">\_ldap.\_tcp.<site name>.\_sites.<partition name></span></span>

<span data-ttu-id="7bdab-109">Per individuare un controller di dominio che ospita una replica di una partizione di directory applicativa specificata, chiamare la funzione [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea) con il parametro *DomainName* impostato sul nome DNS della partizione di directory applicativa e il flag **\_ solo DS \_ \_ necessario** impostato nel parametro *Flags* .</span><span class="sxs-lookup"><span data-stu-id="7bdab-109">To locate a domain controller that hosts a replica of a specified application directory partition, call the [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea) function with the *DomainName* parameter set to the DNS name of the application directory partition and the **DS\_ONLY\_LDAP\_NEEDED** flag set in the *Flags* parameter.</span></span> <span data-ttu-id="7bdab-110">Per ulteriori informazioni e un esempio di codice in cui viene illustrato, utilizzando la funzione **DsGetDcName** , come individuare un controller di dominio che ospita una replica di una partizione di directory applicativa, vedere il [codice di esempio per l'individuazione di un server host della partizione di directory applicativa](example-code-for-locating-an-application-directory-partition-host-server.md).</span><span class="sxs-lookup"><span data-stu-id="7bdab-110">For more information and a code example that shows, using the **DsGetDcName** function, how to locate a domain controller that hosts a replica of an application directory partition, see [Example Code for Locating an Application Directory Partition Host Server](example-code-for-locating-an-application-directory-partition-host-server.md).</span></span>

 

 




