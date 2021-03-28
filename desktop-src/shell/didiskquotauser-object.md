---
description: Consente a un client di gestire le impostazioni di quota disco globale del volume NTFS. Questo oggetto rende disponibili le funzionalità essenziali dell'interfaccia DIDiskQuotaUser per gli script e le applicazioni basate su Microsoft Visual Basic.
title: Oggetto DIDiskQuotaUser
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 0cdf3293-3dcf-44e7-a80d-4eacf9d09fbf
ms.openlocfilehash: 5699ad9d15b0fa31c92f7d88df194f9012fa679d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977231"
---
# <a name="didiskquotauser-object"></a><span data-ttu-id="3e652-104">Oggetto DIDiskQuotaUser</span><span class="sxs-lookup"><span data-stu-id="3e652-104">DIDiskQuotaUser object</span></span>

<span data-ttu-id="3e652-105">Consente a un client di gestire le impostazioni di quota disco globale del volume NTFS.</span><span class="sxs-lookup"><span data-stu-id="3e652-105">Allows a client to manage an NTFS volume's global disk quota settings.</span></span> <span data-ttu-id="3e652-106">Questo oggetto rende disponibili le funzionalità essenziali dell'interfaccia **DIDiskQuotaUser** per gli script e le applicazioni basate su Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="3e652-106">This object makes the essential functionality of the **DIDiskQuotaUser** interface available to scripting and Microsoft Visual Basic-based applications.</span></span>

## <a name="members"></a><span data-ttu-id="3e652-107">Membri</span><span class="sxs-lookup"><span data-stu-id="3e652-107">Members</span></span>

<span data-ttu-id="3e652-108">L'oggetto **DIDiskQuotaUser** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3e652-108">The **DIDiskQuotaUser** object has these types of members:</span></span>

-   [<span data-ttu-id="3e652-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="3e652-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="3e652-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3e652-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3e652-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="3e652-111">Methods</span></span>

<span data-ttu-id="3e652-112">L'oggetto **DIDiskQuotaUser** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="3e652-112">The **DIDiskQuotaUser** object has these methods.</span></span>



| <span data-ttu-id="3e652-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="3e652-113">Method</span></span>                                           | <span data-ttu-id="3e652-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3e652-114">Description</span></span>                                             |
|:-------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="3e652-115">**Invalidate**</span><span class="sxs-lookup"><span data-stu-id="3e652-115">**Invalidate**</span></span>](didiskquotauser-invalidate.md) | <span data-ttu-id="3e652-116">Cancella le informazioni utente memorizzate nella cache dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3e652-116">Clears the object's cached user information.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="3e652-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3e652-117">Properties</span></span>

<span data-ttu-id="3e652-118">L'oggetto **DIDiskQuotaUser** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="3e652-118">The **DIDiskQuotaUser** object has these properties.</span></span>



| <span data-ttu-id="3e652-119">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3e652-119">Property</span></span>                                                                        | <span data-ttu-id="3e652-120">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="3e652-120">Access type</span></span>           | <span data-ttu-id="3e652-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3e652-121">Description</span></span>                                                                                          |
|:--------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3e652-122">**AccountContainerName**</span><span class="sxs-lookup"><span data-stu-id="3e652-122">**AccountContainerName**</span></span>](didiskquotauser-accountcontainername.md)<br/> | <span data-ttu-id="3e652-123">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="3e652-123">Read-only</span></span><br/>  | <span data-ttu-id="3e652-124">Ottiene il nome del contenitore di account dell'utente.</span><span class="sxs-lookup"><span data-stu-id="3e652-124">Gets the name of the user's account container.</span></span><br/>                                            |
| [<span data-ttu-id="3e652-125">**AccountStatus**</span><span class="sxs-lookup"><span data-stu-id="3e652-125">**AccountStatus**</span></span>](didiskquotauser-accountstatus.md)<br/>               | <span data-ttu-id="3e652-126">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="3e652-126">Read-only</span></span><br/>  | <span data-ttu-id="3e652-127">Ottiene lo stato dell'account dell'utente.</span><span class="sxs-lookup"><span data-stu-id="3e652-127">Gets the status of the user's account.</span></span><br/>                                                    |
| [<span data-ttu-id="3e652-128">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="3e652-128">**DisplayName**</span></span>](didiskquotauser-displayname.md)<br/>                   | <span data-ttu-id="3e652-129">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="3e652-129">Read-only</span></span><br/>  | <span data-ttu-id="3e652-130">Ottiene il nome visualizzato dell'utente.</span><span class="sxs-lookup"><span data-stu-id="3e652-130">Gets the user's display name.</span></span><br/>                                                             |
| [<span data-ttu-id="3e652-131">**ID**</span><span class="sxs-lookup"><span data-stu-id="3e652-131">**ID**</span></span>](didiskquotauser-id.md)<br/>                                     | <span data-ttu-id="3e652-132">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="3e652-132">Read-only</span></span><br/>  | <span data-ttu-id="3e652-133">Ottiene un ID che identifica in modo univoco l'utente.</span><span class="sxs-lookup"><span data-stu-id="3e652-133">Gets an ID that uniquely identifies the user.</span></span><br/>                                             |
| [<span data-ttu-id="3e652-134">**LoginName**</span><span class="sxs-lookup"><span data-stu-id="3e652-134">**LogonName**</span></span>](didiskquotauser-logonname.md)<br/>                       | <span data-ttu-id="3e652-135">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="3e652-135">Read-only</span></span><br/>  | <span data-ttu-id="3e652-136">Ottiene il nome dell'account di accesso dell'utente.</span><span class="sxs-lookup"><span data-stu-id="3e652-136">Gets the user's logon account name.</span></span><br/>                                                       |
| [<span data-ttu-id="3e652-137">**QuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="3e652-137">**QuotaLimit**</span></span>](didiskquotauser-quotalimit.md)<br/>                     | <span data-ttu-id="3e652-138">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="3e652-138">Read/write</span></span><br/> | <span data-ttu-id="3e652-139">Imposta o ottiene il [**limite di quota**](diskquotacontrol-object.md)corrente dell'utente.</span><span class="sxs-lookup"><span data-stu-id="3e652-139">Sets or gets the user's current [**quota limit**](diskquotacontrol-object.md).</span></span><br/>           |
| [<span data-ttu-id="3e652-140">**QuotaLimitText**</span><span class="sxs-lookup"><span data-stu-id="3e652-140">**QuotaLimitText**</span></span>](didiskquotauser-quotalimittext.md)<br/>             | <span data-ttu-id="3e652-141">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="3e652-141">Read-only</span></span><br/>  | <span data-ttu-id="3e652-142">Ottiene il [**limite di quota**](diskquotacontrol-object.md) corrente dell'utente come stringa di testo.</span><span class="sxs-lookup"><span data-stu-id="3e652-142">Gets the user's current [**quota limit**](diskquotacontrol-object.md) as a text string.</span></span> <br/> |
| [<span data-ttu-id="3e652-143">**QuotaThreshold**</span><span class="sxs-lookup"><span data-stu-id="3e652-143">**QuotaThreshold**</span></span>](didiskquotauser-quotathreshold.md)<br/>             | <span data-ttu-id="3e652-144">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="3e652-144">Read/write</span></span><br/> | <span data-ttu-id="3e652-145">Imposta o ottiene la soglia di avviso dell'utente, in byte.</span><span class="sxs-lookup"><span data-stu-id="3e652-145">Sets or gets the user's warning threshold, in bytes.</span></span><br/>                                      |
| [<span data-ttu-id="3e652-146">**QuotaThresholdText**</span><span class="sxs-lookup"><span data-stu-id="3e652-146">**QuotaThresholdText**</span></span>](didiskquotauser-quotathresholdtext.md)<br/>     | <span data-ttu-id="3e652-147">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="3e652-147">Read-only</span></span><br/>  | <span data-ttu-id="3e652-148">Ottiene la soglia di avviso dell'utente come una stringa di testo.</span><span class="sxs-lookup"><span data-stu-id="3e652-148">Gets the user's warning threshold as a text string.</span></span><br/>                                       |
| [<span data-ttu-id="3e652-149">**QuotaUsed**</span><span class="sxs-lookup"><span data-stu-id="3e652-149">**QuotaUsed**</span></span>](didiskquotauser-quotaused.md)<br/>                       | <span data-ttu-id="3e652-150">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="3e652-150">Read-only</span></span><br/>  | <span data-ttu-id="3e652-151">Ottiene l'utilizzo del disco corrente dell'utente, in byte.</span><span class="sxs-lookup"><span data-stu-id="3e652-151">Gets the user's current disk usage, in bytes.</span></span><br/>                                             |
| [<span data-ttu-id="3e652-152">**QuotaUsedText**</span><span class="sxs-lookup"><span data-stu-id="3e652-152">**QuotaUsedText**</span></span>](didiskquotauser-quotausedtext.md)<br/>               | <span data-ttu-id="3e652-153">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="3e652-153">Read-only</span></span><br/>  | <span data-ttu-id="3e652-154">Ottiene l'utilizzo del disco corrente dell'utente come stringa di testo.</span><span class="sxs-lookup"><span data-stu-id="3e652-154">Gets the user's current disk usage as a text string.</span></span><br/>                                      |



 

## <a name="remarks"></a><span data-ttu-id="3e652-155">Commenti</span><span class="sxs-lookup"><span data-stu-id="3e652-155">Remarks</span></span>

<span data-ttu-id="3e652-156">A ogni utente del volume gestito dall'oggetto [**DiskQuotaControl**](diskquotacontrol-object.md) è associato un oggetto **DIDiskQuotaUser** .</span><span class="sxs-lookup"><span data-stu-id="3e652-156">Each user on the volume that is managed by the [**DiskQuotaControl**](diskquotacontrol-object.md) object has a **DIDiskQuotaUser** object associated with it.</span></span> <span data-ttu-id="3e652-157">Questo oggetto consente a un client di gestire le impostazioni di un singolo utente.</span><span class="sxs-lookup"><span data-stu-id="3e652-157">This object allows a client to manage an individual user's settings.</span></span> <span data-ttu-id="3e652-158">Sono disponibili diversi modi per ottenere un oggetto **DIDiskQuotaUser** dell'utente:</span><span class="sxs-lookup"><span data-stu-id="3e652-158">There are several ways to obtain a user's **DIDiskQuotaUser** object:</span></span>

-   <span data-ttu-id="3e652-159">Gli oggetti **DIDiskQuotaUser** per tutti gli utenti con quote nel volume vengono esposti come raccolta e possono essere enumerati.</span><span class="sxs-lookup"><span data-stu-id="3e652-159">The **DIDiskQuotaUser** objects for all users with quotas on the volume are exposed as a collection and can be enumerated.</span></span> <span data-ttu-id="3e652-160">Di seguito è riportata una descrizione dell'enumerazione degli oggetti **DIDiskQuotaUser** .</span><span class="sxs-lookup"><span data-stu-id="3e652-160">A discussion of how to enumerate **DIDiskQuotaUser** objects is found below.</span></span>
-   <span data-ttu-id="3e652-161">Quando si aggiunge un nuovo utente, il metodo [**adduser**](diskquotacontrol-adduser.md) restituisce l'oggetto **DIDiskQuotaUser** dell'utente.</span><span class="sxs-lookup"><span data-stu-id="3e652-161">When you add a new user, the [**AddUser**](diskquotacontrol-adduser.md) method returns the user's **DIDiskQuotaUser** object.</span></span>
-   <span data-ttu-id="3e652-162">Se si ha il nome dell'utente, il metodo [**FindUser**](diskquotacontrol-finduser.md) restituisce l'oggetto **DIDiskQuotaUser** dell'utente.</span><span class="sxs-lookup"><span data-stu-id="3e652-162">If you have the user's name, the [**FindUser**](diskquotacontrol-finduser.md) method returns the user's **DIDiskQuotaUser** object.</span></span>

### <a name="enumerating-disk-quota-users"></a><span data-ttu-id="3e652-163">Enumerazione degli utenti delle quote disco</span><span class="sxs-lookup"><span data-stu-id="3e652-163">Enumerating Disk Quota Users</span></span>

<span data-ttu-id="3e652-164">Gli oggetti **DIDiskQuotaUser** per tutti gli utenti con una quota nel volume vengono esposti come raccolta.</span><span class="sxs-lookup"><span data-stu-id="3e652-164">The **DIDiskQuotaUser** objects for all users with a quota on the volume are exposed as a collection.</span></span> <span data-ttu-id="3e652-165">L'oggetto [**DiskQuotaControl**](diskquotacontrol-object.md) esporta un metodo enumeratore standard che consente di enumerare la raccolta di oggetti **DIDiskQuotaUser** .</span><span class="sxs-lookup"><span data-stu-id="3e652-165">The [**DiskQuotaControl**](diskquotacontrol-object.md) object exports a standard enumerator method that allows you to enumerate the collection of **DIDiskQuotaUser** objects.</span></span> <span data-ttu-id="3e652-166">Nella procedura seguente viene illustrato come eseguire l'enumerazione con Microsoft JScript (compatibile con la specifica del linguaggio ECMA 262).</span><span class="sxs-lookup"><span data-stu-id="3e652-166">The following procedure illustrates how to perform the enumeration with Microsoft JScript (compatible with ECMA 262 language specification).</span></span> <span data-ttu-id="3e652-167">È possibile utilizzare una procedura simile con Visual Basic o Microsoft Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="3e652-167">You can use a similar procedure with Visual Basic or Microsoft Visual Basic Scripting Edition (VBScript).</span></span>

1.  <span data-ttu-id="3e652-168">Creare un nuovo oggetto [**DiskQuotaControl**](diskquotacontrol-object.md) .</span><span class="sxs-lookup"><span data-stu-id="3e652-168">Create a new [**DiskQuotaControl**](diskquotacontrol-object.md) object.</span></span>
2.  <span data-ttu-id="3e652-169">Inizializzarlo con [**Initialize**](diskquotacontrol-initialize.md).</span><span class="sxs-lookup"><span data-stu-id="3e652-169">Initialize it with [**Initialize**](diskquotacontrol-initialize.md).</span></span>
3.  <span data-ttu-id="3e652-170">Creare un nuovo oggetto **enumeratore** JScript.</span><span class="sxs-lookup"><span data-stu-id="3e652-170">Create a new JScript **Enumerator** object.</span></span>
4.  <span data-ttu-id="3e652-171">Usare un ciclo **for** per enumerare gli oggetti **DIDiskQuotaUser** .</span><span class="sxs-lookup"><span data-stu-id="3e652-171">Use a **for** loop to enumerate the **DIDiskQuotaUser** objects.</span></span> <span data-ttu-id="3e652-172">Non è necessario impostare un valore iniziale.</span><span class="sxs-lookup"><span data-stu-id="3e652-172">There is no need to set a starting value.</span></span> <span data-ttu-id="3e652-173">Il metodo **MoveNext** dell'oggetto enumeratore invia una notifica al metodo **Item** per restituire l'oggetto **DIDiskQuotaUser** successivo.</span><span class="sxs-lookup"><span data-stu-id="3e652-173">The enumerator object's **moveNext** method notifies the **item** method to return the next **DIDiskQuotaUser** object.</span></span> <span data-ttu-id="3e652-174">Il metodo **atEnd** restituisce **false** quando si raggiunge la fine dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="3e652-174">The **atEnd** method returns **false** when you reach the end of the list.</span></span>
5.  <span data-ttu-id="3e652-175">Se necessario, usare l'oggetto **DIDiskQuotaUser** restituito dal metodo **Item** dell'enumeratore per recuperare o impostare una o più proprietà della quota disco dell'utente associato.</span><span class="sxs-lookup"><span data-stu-id="3e652-175">As needed, use the **DIDiskQuotaUser** object returned by the enumerator's **item** method to retrieve or set one or more of the associated user's disk quota properties.</span></span>

<span data-ttu-id="3e652-176">Nel frammento di codice seguente viene illustrato come enumerare gli oggetti **DIDiskQuotaUser** con JScript.</span><span class="sxs-lookup"><span data-stu-id="3e652-176">The following code fragment illustrates how to enumerate **DIDiskQuotaUser** objects with JScript.</span></span> <span data-ttu-id="3e652-177">L'argomento dell' **\_ etichetta del volume** passato alla funzione **EnumUsers** è un valore stringa contenente un'etichetta di volume, ad esempio "C: \\ \\ ".</span><span class="sxs-lookup"><span data-stu-id="3e652-177">The **Volume\_Label** argument that is passed to the **EnumUsers** function is a string value containing a volume label such as "C:\\\\".</span></span>


```
function EnumUsers(Volume_Label)
{
    var Volume;
    var QuotaUsers;
    var QuotaUser;

    Volume = new ActiveXObject("Microsoft.DiskQuota.1");
    Volume.Initialize(Volume_Label, 1);

    QuotaUsers = new Enumerator(Volume);
    for (;!Users.atEnd(); Users.moveNext())
    {
       QuotaUser = QuotaUsers.item();

     //Use the QuotaUser object to retrieve or set one or more
     //of the user's disk quota properties
     ...
    }
}
```



## <a name="requirements"></a><span data-ttu-id="3e652-178">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3e652-178">Requirements</span></span>



| <span data-ttu-id="3e652-179">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e652-179">Requirement</span></span> | <span data-ttu-id="3e652-180">Valore</span><span class="sxs-lookup"><span data-stu-id="3e652-180">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e652-181">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e652-181">Minimum supported client</span></span><br/> | <span data-ttu-id="3e652-182">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3e652-182">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3e652-183">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e652-183">Minimum supported server</span></span><br/> | <span data-ttu-id="3e652-184">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3e652-184">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="3e652-185">DLL</span><span class="sxs-lookup"><span data-stu-id="3e652-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e652-186"><dt>Shell32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="3e652-186"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e652-187">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3e652-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e652-188">**Oggetto Shell**</span><span class="sxs-lookup"><span data-stu-id="3e652-188">**Shell Object**</span></span>](shell.md)
</dt> </dl>

 

 




