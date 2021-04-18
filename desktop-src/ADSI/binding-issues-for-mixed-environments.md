---
title: Problemi di binding per ambienti misti
description: Problemi di binding per ambienti misti
ms.assetid: d9f9a6bc-7733-4269-99c8-61a84b37d487
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, utilizzo, associazione di problemi per ambienti misti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a65135e0562f387ee9b70e2395d807b639a48e37
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300420"
---
# <a name="binding-issues-for-mixed-environments"></a><span data-ttu-id="93cc5-104">Problemi di binding per ambienti misti</span><span class="sxs-lookup"><span data-stu-id="93cc5-104">Binding Issues for Mixed Environments</span></span>

<span data-ttu-id="93cc5-105">Per gli ambienti in cui il dominio che contiene Active Directory dispone di una relazione di trust con un dominio di Windows NT 4,0, potrebbe essersi verificato un problema nell'utilizzo del binding senza server per l'associazione agli oggetti Active Directory.</span><span class="sxs-lookup"><span data-stu-id="93cc5-105">For environments in which the domain that contains Active Directory has a trust relationship with a Windows NT 4.0 domain, there may be a problem with using serverless binding to bind to Active Directory objects.</span></span>

<span data-ttu-id="93cc5-106">In alcuni ambienti di rete sono state configurate relazioni di trust tra controller di dominio contenenti Active Directory e server Windows NT 4,0 allo scopo di consentire l'autenticazione tra domini.</span><span class="sxs-lookup"><span data-stu-id="93cc5-106">In some networking environments, trust relationships have been set up between domain controllers that contain Active Directory and Windows NT 4.0 servers for the purpose of allowing authentication between domains.</span></span> <span data-ttu-id="93cc5-107">In questi ambienti misti, se un utente che è membro di Windows NT 4,0, il dominio tenta di usare un'associazione senza server per eseguire l'associazione a un oggetto Active Directory in un dominio trusted, l'associazione non riuscirà e verrà restituito un errore.</span><span class="sxs-lookup"><span data-stu-id="93cc5-107">In these mixed environments, if a user, who is a member of the Windows NT 4.0, domain attempts to use serverless binding to bind to an Active Directory object on a trusted domain, then the bind will fail and an error is returned.</span></span> <span data-ttu-id="93cc5-108">Ciò è dovuto al fatto che un'associazione senza server utilizza la funzione [**DsGetDcName**](/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea) per eseguire l'associazione all'oggetto in Active Directory, che dipende dal DNS appropriato.</span><span class="sxs-lookup"><span data-stu-id="93cc5-108">This is because a serverless bind uses the [**DsGetDcName**](/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea) function to bind to the object in Active Directory, which is dependent upon the proper DNS.</span></span>

<span data-ttu-id="93cc5-109">In questo scenario, è necessario che l'utente di Windows NT fornisca il nome di un dominio specifico a cui eseguire l'associazione.</span><span class="sxs-lookup"><span data-stu-id="93cc5-109">In this scenario, the Windows NT user must provide the name of a specific domain to bind to.</span></span> <span data-ttu-id="93cc5-110">Di seguito è riportato un esempio.</span><span class="sxs-lookup"><span data-stu-id="93cc5-110">The following is an example.</span></span>

``` syntax
LDAP://fabrikam.com/OU=Sales
```

 

 