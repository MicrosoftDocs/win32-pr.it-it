---
title: Proprietà utente personalizzate WinNT
description: Il provider WinNT rende disponibili le seguenti proprietà personalizzate per la classe utente. È possibile accedervi tramite i metodi IADs. Get e IADs. Put. Per ulteriori informazioni, vedere la \_ struttura User info \_ 3.
ms.assetid: 3b122424-ff24-4de7-bdaf-693fb4529b09
ms.tgt_platform: multiple
keywords:
- Proprietà utente personalizzate WinNT ADSI
- ADSI del provider WinNT, oggetto utente, proprietà personalizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95230de6f7bb5bd848d7a8a047c0ec1966e5a67e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103963459"
---
# <a name="winnt-custom-user-properties"></a><span data-ttu-id="e32f6-107">Proprietà utente personalizzate WinNT</span><span class="sxs-lookup"><span data-stu-id="e32f6-107">WinNT Custom User Properties</span></span>

<span data-ttu-id="e32f6-108">Il provider WinNT rende disponibili le seguenti proprietà personalizzate per la classe utente.</span><span class="sxs-lookup"><span data-stu-id="e32f6-108">The WinNT provider makes available the following custom properties for the User class.</span></span> <span data-ttu-id="e32f6-109">È possibile accedervi tramite i metodi [**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) e [**IADs. Put**](/windows/desktop/api/Iads/nf-iads-iads-put) .</span><span class="sxs-lookup"><span data-stu-id="e32f6-109">They may be accessed through the [**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) and [**IADs.Put**](/windows/desktop/api/Iads/nf-iads-iads-put) methods.</span></span> <span data-ttu-id="e32f6-110">Per ulteriori informazioni, vedere la struttura [**User \_ info \_ 3**](/windows/desktop/api/lmaccess/ns-lmaccess-user_info_3) .</span><span class="sxs-lookup"><span data-stu-id="e32f6-110">For more information, see the [**USER\_INFO\_3**](/windows/desktop/api/lmaccess/ns-lmaccess-user_info_3) structure.</span></span>



| <span data-ttu-id="e32f6-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e32f6-111">Property</span></span>            | <span data-ttu-id="e32f6-112">Type</span><span class="sxs-lookup"><span data-stu-id="e32f6-112">Type</span></span>         | <span data-ttu-id="e32f6-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e32f6-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                                   |
|---------------------|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e32f6-114">**HomeDirDrive**</span><span class="sxs-lookup"><span data-stu-id="e32f6-114">**HomeDirDrive**</span></span>    | <span data-ttu-id="e32f6-115">string</span><span class="sxs-lookup"><span data-stu-id="e32f6-115">String</span></span>       | <span data-ttu-id="e32f6-116">Unità Home directory dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e32f6-116">Home Directory Drive of the user.</span></span> <span data-ttu-id="e32f6-117">Si tratta di un puntatore a una stringa Unicode che specifica il percorso della Home Directory.</span><span class="sxs-lookup"><span data-stu-id="e32f6-117">This is a pointer to a Unicode string that specifies the path of the home directory.</span></span> <span data-ttu-id="e32f6-118">La stringa può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="e32f6-118">The string can be **null**.</span></span> <span data-ttu-id="e32f6-119">Vedere l'esempio in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="e32f6-119">See example in this topic.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="e32f6-120">**ObjectSID**</span><span class="sxs-lookup"><span data-stu-id="e32f6-120">**ObjectSID**</span></span>       | <span data-ttu-id="e32f6-121">Stringa ottetto</span><span class="sxs-lookup"><span data-stu-id="e32f6-121">Octet String</span></span> | <span data-ttu-id="e32f6-122">SID oggetto dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e32f6-122">Object SID of the user.</span></span> <span data-ttu-id="e32f6-123">Per un esempio di come recuperare il SID dell'oggetto utilizzando il provider WinNT, vedere [oggetto SID (provider WinNT)](object-sid.md)</span><span class="sxs-lookup"><span data-stu-id="e32f6-123">For an example of how to retrieve the Object SID using the WinNT Provider, see [Object SID (WinNT Provider)](object-sid.md)</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="e32f6-124">**Parametri**</span><span class="sxs-lookup"><span data-stu-id="e32f6-124">**Parameters**</span></span>      | <span data-ttu-id="e32f6-125">string</span><span class="sxs-lookup"><span data-stu-id="e32f6-125">String</span></span>       | <span data-ttu-id="e32f6-126">Parametri dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e32f6-126">Parameters of the user.</span></span> <span data-ttu-id="e32f6-127">Punta a una stringa Unicode riservata per l'utilizzo da parte delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="e32f6-127">Points to a Unicode string that is set aside for use by applications.</span></span> <span data-ttu-id="e32f6-128">Questa stringa può essere una stringa null oppure può contenere un numero qualsiasi di caratteri prima del carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="e32f6-128">This string can be a null string, or it can have any number of characters before the terminating null character.</span></span> <span data-ttu-id="e32f6-129">I prodotti Microsoft usano questo membro per archiviare i dati di configurazione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e32f6-129">Microsoft products use this member to store user configuration data.</span></span> <span data-ttu-id="e32f6-130">Questa proprietà può essere modificata solo da un'applicazione durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="e32f6-130">This property can only be modified by an application during installation.</span></span> |
| <span data-ttu-id="e32f6-131">**Password**</span><span class="sxs-lookup"><span data-stu-id="e32f6-131">**PasswordAge**</span></span>     | <span data-ttu-id="e32f6-132">Tempo</span><span class="sxs-lookup"><span data-stu-id="e32f6-132">Time</span></span>         | <span data-ttu-id="e32f6-133">Durata dell'intervallo di tempo per la password in uso.</span><span class="sxs-lookup"><span data-stu-id="e32f6-133">Time duration of the password in use.</span></span> <span data-ttu-id="e32f6-134">Questa proprietà indica il numero di secondi trascorsi dall'Ultima modifica della password.</span><span class="sxs-lookup"><span data-stu-id="e32f6-134">This property indicates the number of seconds that have elapsed since the password was last changed.</span></span>                                                                                                                                                                                                                    |
| <span data-ttu-id="e32f6-135">**PasswordExpired**</span><span class="sxs-lookup"><span data-stu-id="e32f6-135">**PasswordExpired**</span></span> | <span data-ttu-id="e32f6-136">Integer</span><span class="sxs-lookup"><span data-stu-id="e32f6-136">Integer</span></span>      | <span data-ttu-id="e32f6-137">Indica quando la password è scaduta.</span><span class="sxs-lookup"><span data-stu-id="e32f6-137">Tells when the password was expired.</span></span> <span data-ttu-id="e32f6-138">Quando si usa Get, viene restituito zero se la password non è scaduta o è diverso da zero se è scaduta.</span><span class="sxs-lookup"><span data-stu-id="e32f6-138">When you use Get, it will return zero is the password has not expired, or nonzero if it has expired.</span></span> <span data-ttu-id="e32f6-139">Vedere l'esempio in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="e32f6-139">See example in this topic.</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="e32f6-140">**PrimaryGroupID**</span><span class="sxs-lookup"><span data-stu-id="e32f6-140">**PrimaryGroupID**</span></span>  | <span data-ttu-id="e32f6-141">Integer</span><span class="sxs-lookup"><span data-stu-id="e32f6-141">Integer</span></span>      | <span data-ttu-id="e32f6-142">ID gruppo primario dell'utente, ad esempio ID gruppo utenti di dominio.</span><span class="sxs-lookup"><span data-stu-id="e32f6-142">User's primary group ID, for example, domain user group ID.</span></span> <span data-ttu-id="e32f6-143">Vedere l'esempio in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="e32f6-143">See example in this topic.</span></span>                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="e32f6-144">**UserFlags**</span><span class="sxs-lookup"><span data-stu-id="e32f6-144">**UserFlags**</span></span>       | <span data-ttu-id="e32f6-145">Integer</span><span class="sxs-lookup"><span data-stu-id="e32f6-145">Integer</span></span>      | <span data-ttu-id="e32f6-146">Flag utente definito nell' [**\_ enumerazione del \_ flag \_ utente ADS**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum).</span><span class="sxs-lookup"><span data-stu-id="e32f6-146">User Flag defined in [**ADS\_USER\_FLAG\_ENUM**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum).</span></span> <span data-ttu-id="e32f6-147">Per un esempio di come usare UserFlags, vedere [Nessuna scadenza password (provider WinNT)](winnt-password-never-expires.md)</span><span class="sxs-lookup"><span data-stu-id="e32f6-147">For an example of how to use UserFlags, see [Password Never Expires (WinNT Provider)](winnt-password-never-expires.md)</span></span>                                                                                                                                                             |



 

<span data-ttu-id="e32f6-148">Questo esempio illustra come impostare la directory dell'unità principale di un utente.</span><span class="sxs-lookup"><span data-stu-id="e32f6-148">This example shows how to set a user's Home Drive Directory.</span></span>


```VB
Dim usr As Object

Set usr = GetObject("WinNT://Fabrikam/jsmith,user") 
usr.HomeDirectory = "UserHomeDirHere"
usr.HomeDirDrive = "HomeDirDriveHere"
usr.SetInfo
```



<span data-ttu-id="e32f6-149">Questo esempio illustra come usare PasswordExpired per forzare l'utente a modificare la password all'accesso successivo.</span><span class="sxs-lookup"><span data-stu-id="e32f6-149">This example shows how to use PasswordExpired to force a user to change the password at the next logon.</span></span>


```VB
Dim usr As Object

Set usr = GetObject("WinNT://Fabrikam/jsmith,user")
usr.Put "PasswordExpired", CLng(1)
usr.SetInfo 

'--- Clear this flag so that the user does not have to change the password at next logon.

usr.Put "PasswordExpired", CLng(0)
usr.SetInfo
```



<span data-ttu-id="e32f6-150">Questo esempio illustra come ottenere il gruppo primario dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e32f6-150">This example shows how to get the user's primary group.</span></span>


```VB
Dim usr As Object
Dim grpPrimaryID As Object

Set usr = GetObject("WinNT://Fabrikam/jsmith,user") 
grpPrimaryID = usr.Get("PrimaryGroupID")
```



 

 