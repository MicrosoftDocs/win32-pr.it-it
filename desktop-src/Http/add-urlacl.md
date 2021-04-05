---
title: add urlacl
description: Riserva l'URL specificato per gli utenti e gli account non amministratori.
ms.assetid: 5d89dec3-26e6-4db8-b4cc-e9b933ac60c5
keywords:
- Aggiungi urlacl HTTP
topic_type:
- apiref
api_name:
- add urlacl
api_type:
- NA
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/29/2020
ms.openlocfilehash: 16f6cb64c0c784f3a5400e2c97e212edbc50936c
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/10/2021
ms.locfileid: "103969289"
---
# <a name="add-urlacl"></a><span data-ttu-id="5ca8e-104">add urlacl</span><span class="sxs-lookup"><span data-stu-id="5ca8e-104">add urlacl</span></span>

<span data-ttu-id="5ca8e-105">Riserva l'URL specificato per gli utenti e gli account non amministratori.</span><span class="sxs-lookup"><span data-stu-id="5ca8e-105">Reserves the specified URL for non-administrator users and accounts.</span></span> <span data-ttu-id="5ca8e-106">È possibile specificare l'elenco di controllo di accesso discrezionale (DACL) utilizzando un nome di account con i parametri Listen e Delegate oppure utilizzando una stringa SDDL (Security Descriptor Definition Language).</span><span class="sxs-lookup"><span data-stu-id="5ca8e-106">The discretionary access control list (DACL) can be specified by using an account name with the listen and delegate parameters or by using a security descriptor definition language (SDDL) string.</span></span>

``` syntax
add urlacl [url=]string
           [[user=]string
           {[[listen={yes|no}] [delegate={yes|no}]] | [sddl=]string}

 
```

## <a name="parameters"></a><span data-ttu-id="5ca8e-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="5ca8e-107">Parameters</span></span>

<dl> <span data-ttu-id="5ca8e-108"><dt>

<span id="_url__string"></span><span id="_URL__STRING"></span>
**[URL =] stringa**
</dt> </span><span class="sxs-lookup"><span data-stu-id="5ca8e-108"><dt>

<span id="_url__string"></span><span id="_URL__STRING"></span>
**[url=] string**
</dt> </span></span><dd>

<span data-ttu-id="5ca8e-109">Specifica l'URL completo.</span><span class="sxs-lookup"><span data-stu-id="5ca8e-109">Specifies the fully qualified URL.</span></span>

<span data-ttu-id="5ca8e-110"></dd> <dt>

<span id="_user__string"></span><span id="_USER__STRING"></span>
**stringa [user =]**
</dt> </span><span class="sxs-lookup"><span data-stu-id="5ca8e-110"></dd> <dt>

<span id="_user__string"></span><span id="_USER__STRING"></span>
**[user=] string**
</dt> </span></span><dd>

<span data-ttu-id="5ca8e-111">Specifica il nome dell'utente o del gruppo di utenti.</span><span class="sxs-lookup"><span data-stu-id="5ca8e-111">Specifies the user or user group name.</span></span>

</dd> <dt>

<span data-ttu-id="5ca8e-112"><span id="_listen__yes_no__"></span><span id="_LISTEN__YES_NO__"></span>**\[ascolto = {Sì \| No}\]**</span><span class="sxs-lookup"><span data-stu-id="5ca8e-112"><span id="_listen__yes_no__"></span><span id="_LISTEN__YES_NO__"></span>**\[listen={yes\|no}\]**</span></span>
</dt> <dd>

<span data-ttu-id="5ca8e-113">Specifica uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="5ca8e-113">Specifies one of the following values:</span></span>

-   <span data-ttu-id="5ca8e-114">Sì: consente all'utente di registrare gli URL.</span><span class="sxs-lookup"><span data-stu-id="5ca8e-114">yes: Allows the user to register URLs.</span></span> <span data-ttu-id="5ca8e-115">Si tratta del valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="5ca8e-115">This is the default value.</span></span>
-   <span data-ttu-id="5ca8e-116">No: nega all'utente la registrazione degli URL.</span><span class="sxs-lookup"><span data-stu-id="5ca8e-116">no: Denies the user from registering URLs.</span></span>

</dd> <dt>

<span data-ttu-id="5ca8e-117"><span id="_delegate__yes_no__"></span><span id="_DELEGATE__YES_NO__"></span>**\[Delegato = {Yes \| No}\]**</span><span class="sxs-lookup"><span data-stu-id="5ca8e-117"><span id="_delegate__yes_no__"></span><span id="_DELEGATE__YES_NO__"></span>**\[delegate={yes\|no}\]**</span></span>
</dt> <dd>

<span data-ttu-id="5ca8e-118">Specifica uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="5ca8e-118">Specifies one of the following values:</span></span>

-   <span data-ttu-id="5ca8e-119">Sì: consente all'utente di delegare gli URL.</span><span class="sxs-lookup"><span data-stu-id="5ca8e-119">yes: Allows the user to delegate URLs.</span></span>
-   <span data-ttu-id="5ca8e-120">No: nega all'utente la delega degli URL.</span><span class="sxs-lookup"><span data-stu-id="5ca8e-120">no: Denies the user from delegating URLs.</span></span> <span data-ttu-id="5ca8e-121">Si tratta del valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="5ca8e-121">This is the default value.</span></span>

<span data-ttu-id="5ca8e-122"></dd> <dt>

<span id="_sddl__string"></span><span id="_SDDL__STRING"></span>
**[SDDL =] stringa**
</dt> </span><span class="sxs-lookup"><span data-stu-id="5ca8e-122"></dd> <dt>

<span id="_sddl__string"></span><span id="_SDDL__STRING"></span>
**[sddl=] string**
</dt> </span></span><dd>

<span data-ttu-id="5ca8e-123">Specifica la stringa SDDL che descrive l'elenco DACL.</span><span class="sxs-lookup"><span data-stu-id="5ca8e-123">Specifies the SDDL string that describes the DACL.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="5ca8e-124">Esempio</span><span class="sxs-lookup"><span data-stu-id="5ca8e-124">Examples</span></span>

* <span data-ttu-id="5ca8e-125">add urlacl url=https://+:80/MyUri user=DOMAIN\\ user</span><span class="sxs-lookup"><span data-stu-id="5ca8e-125">add urlacl url=https://+:80/MyUri user=DOMAIN\\user</span></span>

* <span data-ttu-id="5ca8e-126">add urlacl url=https://www.contoso.com:80/MyUri user=DOMAIN\\user listen=yes</span><span class="sxs-lookup"><span data-stu-id="5ca8e-126">add urlacl url=https://www.contoso.com:80/MyUri user=DOMAIN\\user listen=yes</span></span>

* <span data-ttu-id="5ca8e-127">add urlacl url=https://www.contoso.com:80/MyUri user=DOMAIN\\user delegate=no</span><span class="sxs-lookup"><span data-stu-id="5ca8e-127">add urlacl url=https://www.contoso.com:80/MyUri user=DOMAIN\\user delegate=no</span></span>

 
## <a name="see-also"></a><span data-ttu-id="5ca8e-128">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="5ca8e-128">See Also</span></span>

* [<span data-ttu-id="5ca8e-129">Comandi netsh per HTTP</span><span class="sxs-lookup"><span data-stu-id="5ca8e-129">Netsh http commands</span></span>](/windows-server/networking/technologies/netsh/netsh-http#add-urlacl)
 