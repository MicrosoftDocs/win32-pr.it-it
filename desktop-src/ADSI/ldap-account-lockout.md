---
title: Blocco account (provider LDAP)
description: Quando viene superato il numero di tentativi di accesso non riusciti, l'account utente viene bloccato per un periodo di tempo specificato dall'attributo lockoutDuration.
ms.assetid: bf86f6ac-8209-4306-8736-99ce53c93617
ms.tgt_platform: multiple
keywords:
- Blocco account (provider LDAP) ADSI
- Blocco account ADSI, provider LDAP
- Provider LDAP ADSI, esempi di gestione degli utenti, blocco degli account
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 697b7a25943debfd08469ce9a28463c88159ded9
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300450"
---
# <a name="account-lockout-ldap-provider"></a><span data-ttu-id="d4cac-106">Blocco account (provider LDAP)</span><span class="sxs-lookup"><span data-stu-id="d4cac-106">Account Lockout (LDAP Provider)</span></span>

<span data-ttu-id="d4cac-107">Quando viene superato il numero di tentativi di accesso non riusciti, l'account utente viene bloccato per un periodo di tempo specificato dall'attributo [**lockoutDuration**](/windows/desktop/ADSchema/a-lockoutduration) .</span><span class="sxs-lookup"><span data-stu-id="d4cac-107">When the number of failed logon attempts is exceeded, the user account is locked out for a time period specified by the [**lockoutDuration**](/windows/desktop/ADSchema/a-lockoutduration) attribute.</span></span> <span data-ttu-id="d4cac-108">La proprietà [**IADsUser. IsAccountLocked**](iadsuser-property-methods.md) sembra essere la proprietà da usare per leggere e modificare lo stato di blocco di un account utente, ma il provider ADSI LDAP non supporta accuratamente la proprietà **IsAccountLocked** .</span><span class="sxs-lookup"><span data-stu-id="d4cac-108">The [**IADsUser.IsAccountLocked**](iadsuser-property-methods.md) property appears to be the property to use to read and modify the lockout state of a user account, but the LDAP ADSI provider does not accurately support the **IsAccountLocked** property.</span></span> <span data-ttu-id="d4cac-109">Per ottenere e impostare dati di blocco degli account accurati, utilizzare il provider WinNT.</span><span class="sxs-lookup"><span data-stu-id="d4cac-109">To obtain and set accurate account lockout data, use the WinNT provider.</span></span> <span data-ttu-id="d4cac-110">Per ulteriori informazioni sull'utilizzo della proprietà **IsAccountLocked** con il provider WinNT, vedere [blocco account (provider WinNT)](winnt-account-lockout.md).</span><span class="sxs-lookup"><span data-stu-id="d4cac-110">For more information about using the **IsAccountLocked** property with the WinNT provider, see [Account Lockout (WinNT Provider)](winnt-account-lockout.md).</span></span>

 

 