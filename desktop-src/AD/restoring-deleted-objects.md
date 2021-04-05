---
title: Ripristino di oggetti eliminati
description: Windows Server 2003 include il \ 0034; Ripristina oggetti eliminati \ 0034; funzionalità.
ms.assetid: b64c5c91-fb76-4323-b78d-f692aa887c96
ms.tgt_platform: multiple
keywords:
- Ripristino di oggetti eliminati AD
- Active Directory, utilizzo, ripristino di oggetti eliminati
- oggetti AD, ripristino di oggetti eliminati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f8f1d3511bb4246826e677aa239ca594918127a
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104516702"
---
# <a name="restoring-deleted-objects"></a><span data-ttu-id="7b13f-106">Ripristino di oggetti eliminati</span><span class="sxs-lookup"><span data-stu-id="7b13f-106">Restoring Deleted Objects</span></span>

<span data-ttu-id="7b13f-107">Windows Server 2003 include la funzionalità "Ripristina oggetti eliminati".</span><span class="sxs-lookup"><span data-stu-id="7b13f-107">Windows Server 2003 includes the "restore deleted objects" feature.</span></span>

<span data-ttu-id="7b13f-108">Per abilitare il ripristino degli oggetti eliminati, è necessario che almeno un controller di dominio nel dominio sia in esecuzione in Windows Server 2003 o in una versione successiva di Windows.</span><span class="sxs-lookup"><span data-stu-id="7b13f-108">To enable deleted object restoration, at least one domain controller in the domain must be running on Windows Server 2003 or a later version of Windows.</span></span> <span data-ttu-id="7b13f-109">Per impostazione predefinita, solo gli amministratori di dominio possono ripristinare gli oggetti eliminati, anche se possono essere delegati ad altri.</span><span class="sxs-lookup"><span data-stu-id="7b13f-109">By default, only domain administrators can restore deleted objects, though this can be delegated to others.</span></span>

<span data-ttu-id="7b13f-110">Per il ripristino degli oggetti eliminati si applicano le limitazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="7b13f-110">The following limitations apply to restoring deleted objects:</span></span>

-   <span data-ttu-id="7b13f-111">Non è possibile ripristinare un oggetto quando la durata della rimozione definitiva per l'oggetto è scaduta perché quando la durata della rimozione definitiva è scaduta, l'oggetto viene eliminato definitivamente.</span><span class="sxs-lookup"><span data-stu-id="7b13f-111">An object cannot be restored when the tombstone lifetime for the object has expired because when the tombstone lifetime has expired, the object is permanently deleted.</span></span>
-   <span data-ttu-id="7b13f-112">Gli oggetti presenti nella radice del contesto dei nomi, ad esempio un dominio o una partizione di applicazione, non possono essere ripristinati.</span><span class="sxs-lookup"><span data-stu-id="7b13f-112">Objects that exist at the root of the naming context, such as a domain or application partition, cannot be restored.</span></span>
-   <span data-ttu-id="7b13f-113">Impossibile ripristinare gli oggetti dello schema.</span><span class="sxs-lookup"><span data-stu-id="7b13f-113">Schema objects cannot be restored.</span></span> <span data-ttu-id="7b13f-114">Gli oggetti dello schema non devono mai essere eliminati.</span><span class="sxs-lookup"><span data-stu-id="7b13f-114">Schema objects should never be deleted.</span></span>
-   <span data-ttu-id="7b13f-115">È possibile ripristinare i contenitori eliminati, ma il ripristino degli oggetti eliminati presenti nel contenitore prima dell'eliminazione è difficile perché la struttura ad albero sotto il contenitore deve essere ricostruita manualmente.</span><span class="sxs-lookup"><span data-stu-id="7b13f-115">It is possible to restore deleted containers, but the restoration of the deleted objects that were in the container before the deletion is difficult because the tree structure under the container must be manually reconstructed.</span></span>

## <a name="permissions-required-to-restore-a-deleted-object"></a><span data-ttu-id="7b13f-116">Autorizzazioni necessarie per ripristinare un oggetto eliminato</span><span class="sxs-lookup"><span data-stu-id="7b13f-116">Permissions Required to Restore a Deleted Object</span></span>

<span data-ttu-id="7b13f-117">Quando un oggetto viene eliminato, viene mantenuto il descrittore di sicurezza dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7b13f-117">When an object is deleted, the object security descriptor is retained.</span></span> <span data-ttu-id="7b13f-118">Sebbene il proprietario sia identificabile dal descrittore di sicurezza, per motivi di sicurezza, solo gli amministratori di dominio possono ripristinare gli oggetti eliminati.</span><span class="sxs-lookup"><span data-stu-id="7b13f-118">Although the owner is identifiable from the security descriptor, for security reasons, only domain administrators are allowed to restore deleted objects.</span></span> <span data-ttu-id="7b13f-119">Gli amministratori di dominio possono concedere l'autorizzazione per il ripristino degli oggetti Delete ad altri utenti e gruppi concedendo all'utente o al gruppo il diritto di accesso al controllo "reanimate Tombstone".</span><span class="sxs-lookup"><span data-stu-id="7b13f-119">Domain administrators can grant the permission to restore delete objects to other users and groups by granting the user or group the "Reanimate Tombstone" control access right.</span></span> <span data-ttu-id="7b13f-120">Alla radice del contesto dei nomi viene concesso il diritto di accesso del controllo "reanimato per la rimozione definitiva".</span><span class="sxs-lookup"><span data-stu-id="7b13f-120">The "Reanimate Tombstone" control access right is granted at the Naming Context root.</span></span> <span data-ttu-id="7b13f-121">Solo gli utenti che dispongono dell'autorizzazione di accesso in lettura per un oggetto e i relativi attributi sono autorizzati a leggere l'oggetto e gli attributi accessibili dopo l'eliminazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7b13f-121">Only users that had read access permission on an object and its attributes are permitted to read the object and accessible attributes after the object is deleted.</span></span>

> [!Note]  
> <span data-ttu-id="7b13f-122">Concessione a un utente questa autorizzazione può costituire un rischio per la sicurezza perché potrebbe consentire all'utente di ripristinare un oggetto account che ha accesso alle risorse di cui l'utente non ha normalmente accesso.</span><span class="sxs-lookup"><span data-stu-id="7b13f-122">Granting a user this permission can be a security risk because it could permit the user to restore an account object that has access to resources that the user would not normally have access to.</span></span> <span data-ttu-id="7b13f-123">Tramite il ripristino di un account, l'utente acquisisce essenzialmente il controllo di questo account perché l'utente deve impostare la password iniziale per l'account quando viene ripristinato l'account.</span><span class="sxs-lookup"><span data-stu-id="7b13f-123">By restoring an account, the user essentially gains control of this account because the user must set the initial password on the account when the account is restored.</span></span>

 

<span data-ttu-id="7b13f-124">Per ripristinare completamente un oggetto eliminato, l'utente deve:</span><span class="sxs-lookup"><span data-stu-id="7b13f-124">To completely restore a deleted object, the user must:</span></span>

-   <span data-ttu-id="7b13f-125">Avere o essere un membro di un gruppo che dispone di, il diritto di accesso del controllo "reanimato per la rimozione definitiva".</span><span class="sxs-lookup"><span data-stu-id="7b13f-125">Have, or be a member of a group that has, the "Reanimate Tombstone" control access right.</span></span>

-   <span data-ttu-id="7b13f-126">Avere accesso in scrittura per ogni attributo obbligatorio che richiede l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="7b13f-126">Have write access for each mandatory attribute that requires updating.</span></span>

-   <span data-ttu-id="7b13f-127">Hanno accesso in scrittura al nome distinto relativo (RDN).</span><span class="sxs-lookup"><span data-stu-id="7b13f-127">Have write access to the Relative Distinguished Name (RDN).</span></span>

-   <span data-ttu-id="7b13f-128">Avere accesso in scrittura a ogni attributo facoltativo che deve essere aggiornato.</span><span class="sxs-lookup"><span data-stu-id="7b13f-128">Have write access to each optional attribute that needs to be updated.</span></span>

-   <span data-ttu-id="7b13f-129">Disporre dei diritti di creazione figlio sul contenitore di destinazione per la classe di oggetti dell'oggetto ripristinato.</span><span class="sxs-lookup"><span data-stu-id="7b13f-129">Have child-creation rights on the destination container for the object class of restored object.</span></span>

    > [!Note]  
    > <span data-ttu-id="7b13f-130">L'attributo **Indeleted** non viene verificato durante l'operazione di ripristino.</span><span class="sxs-lookup"><span data-stu-id="7b13f-130">The **isDeleted** attribute is not verified during the restore operation.</span></span> <span data-ttu-id="7b13f-131">Né verrà verificata l'autorizzazione Delete-Child per il contenitore "Deleted Objects".</span><span class="sxs-lookup"><span data-stu-id="7b13f-131">Neither will the delete-child permission on the "Deleted Objects" container be verified.</span></span>

     

## <a name="restoring-a-deleted-object"></a><span data-ttu-id="7b13f-132">Ripristino di un oggetto eliminato</span><span class="sxs-lookup"><span data-stu-id="7b13f-132">Restoring a Deleted Object</span></span>

<span data-ttu-id="7b13f-133">Per ripristinare un oggetto eliminato, è innanzitutto necessario che l'oggetto si trovi nel contenitore degli oggetti eliminati.</span><span class="sxs-lookup"><span data-stu-id="7b13f-133">To restore a deleted object, the object must first be located in the Deleted Objects container.</span></span> <span data-ttu-id="7b13f-134">Per ulteriori informazioni sul recupero di oggetti eliminati, vedere [recupero di oggetti eliminati](retrieving-deleted-objects.md).</span><span class="sxs-lookup"><span data-stu-id="7b13f-134">For more information about retrieving deleted objects, see [Retrieving Deleted Objects](retrieving-deleted-objects.md).</span></span>

<span data-ttu-id="7b13f-135">Quando l'oggetto è stato individuato, le operazioni seguenti devono essere completate in una singola operazione LDAP.</span><span class="sxs-lookup"><span data-stu-id="7b13f-135">When the object has been located, the following operations must be completed in a single LDAP operation.</span></span> <span data-ttu-id="7b13f-136">Questa operazione richiede l'uso della funzione [**LDAP \_ Modify \_ ext \_ s**](/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_ext_s) con il [**server LDAP che mostra il controllo \_ \_ \_ \_ OID eliminato**](/previous-versions/windows/desktop/ldap/ldap-server-show-deleted-oid) .</span><span class="sxs-lookup"><span data-stu-id="7b13f-136">This requires the use of the [**ldap\_modify\_ext\_s**](/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_ext_s) function with the [**LDAP\_SERVER\_SHOW\_DELETED\_OID**](/previous-versions/windows/desktop/ldap/ldap-server-show-deleted-oid) control.</span></span>

-   <span data-ttu-id="7b13f-137">Rimuovere il valore dell'attributo **Andeleted** .</span><span class="sxs-lookup"><span data-stu-id="7b13f-137">Remove the **isDeleted** attribute value.</span></span> <span data-ttu-id="7b13f-138">Il valore dell'attributo **undeleted** deve essere rimosso e non impostato su **false**.</span><span class="sxs-lookup"><span data-stu-id="7b13f-138">The **isDeleted** attribute value must be removed, not set to **FALSE**.</span></span>
-   <span data-ttu-id="7b13f-139">Sostituire il nome distinto dell'oggetto in modo che venga spostato in un contenitore diverso dal contenitore degli oggetti eliminati.</span><span class="sxs-lookup"><span data-stu-id="7b13f-139">Replace the distinguished name of the object so that it is moved to a container other than the Deleted Objects container.</span></span> <span data-ttu-id="7b13f-140">Può trattarsi di qualsiasi contenitore che in genere può contenere l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7b13f-140">This can be any container that can normally contain the object.</span></span> <span data-ttu-id="7b13f-141">Il nome distinto del contenitore precedente dell'oggetto può essere trovato nell'attributo **lastKnownParent** dell'oggetto eliminato.</span><span class="sxs-lookup"><span data-stu-id="7b13f-141">The distinguished name of the previous container of the object can be found in the deleted object's **lastKnownParent** attribute.</span></span> <span data-ttu-id="7b13f-142">L'attributo **lastKnownParent** viene impostato solo se l'oggetto è stato eliminato in un controller di dominio Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="7b13f-142">The **lastKnownParent** attribute is only set if the object was deleted on a Windows Server 2003 domain controller.</span></span> <span data-ttu-id="7b13f-143">È pertanto possibile che il contenuto dell'attributo **lastKnownParent** non sia accurato.</span><span class="sxs-lookup"><span data-stu-id="7b13f-143">Thus, it is possible that the content of the **lastKnownParent** attribute is inaccurate.</span></span>
-   <span data-ttu-id="7b13f-144">Ripristinare gli attributi obbligatori per l'oggetto che sono stati cancellati durante l'eliminazione.</span><span class="sxs-lookup"><span data-stu-id="7b13f-144">Restore the mandatory attributes for the object that were cleared during deletion.</span></span>

> [!Note]  
> <span data-ttu-id="7b13f-145">L'attributo **objectCategory** può essere impostato anche quando l'oggetto viene ripristinato, ma non è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="7b13f-145">The **objectCategory** attribute can also be set when the object is restored, but is not required.</span></span> <span data-ttu-id="7b13f-146">Se non viene specificato alcun valore **objectCategory** , viene utilizzato il **objectCategory** predefinito per **objectClass** dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7b13f-146">If no **objectCategory** value is specified, the default **objectCategory** for the object's **objectClass** is used.</span></span>

 

<span data-ttu-id="7b13f-147">Dopo che l'oggetto è stato ripristinato, è possibile accedervi come prima dell'eliminazione.</span><span class="sxs-lookup"><span data-stu-id="7b13f-147">After the object is restored, it can be accessed as it was before it was deleted.</span></span> <span data-ttu-id="7b13f-148">A questo punto, è necessario ripristinare tutti gli attributi facoltativi importanti.</span><span class="sxs-lookup"><span data-stu-id="7b13f-148">At this point, any optional attributes that are important should be restored.</span></span> <span data-ttu-id="7b13f-149">È necessario ripristinare anche tutti i riferimenti all'oggetto da altri oggetti nella directory.</span><span class="sxs-lookup"><span data-stu-id="7b13f-149">Any references to the object from other objects in the directory must also be restored.</span></span>

<span data-ttu-id="7b13f-150">Come misura di sicurezza, gli oggetti utente vengono disabilitati quando vengono ripristinati.</span><span class="sxs-lookup"><span data-stu-id="7b13f-150">As a security measure, user objects are disabled when they are restored.</span></span> <span data-ttu-id="7b13f-151">Gli oggetti utente devono essere abilitati dopo il ripristino degli attributi facoltativi per consentire l'utilizzo dell'oggetto utente.</span><span class="sxs-lookup"><span data-stu-id="7b13f-151">User objects must be enabled after restoring the optional attributes to allow the user object to be used.</span></span>

<span data-ttu-id="7b13f-152">Per ulteriori informazioni e un esempio di codice che illustra come ripristinare un oggetto eliminato, vedere la funzione RestoreDeletedObject riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="7b13f-152">For more information and a code example that shows how to restore a deleted object, see the RestoreDeletedObject function below.</span></span>

## <a name="restoredeletedobject"></a><span data-ttu-id="7b13f-153">RestoreDeletedObject</span><span class="sxs-lookup"><span data-stu-id="7b13f-153">RestoreDeletedObject</span></span>

<span data-ttu-id="7b13f-154">Nell'esempio di codice C++ riportato di seguito viene illustrato come ripristinare un oggetto eliminato.</span><span class="sxs-lookup"><span data-stu-id="7b13f-154">The following C++ code example shows how to restore a deleted object.</span></span>


```C++
//***************************************************************************
//
//  RestoreDeletedObject()
//
//  Restores a deleted object. 
//
//  pwszDeletedDN - Contains the fully qualified distinguished name of the 
//  deleted object.
//
//  pwszDestContainerDN - Contains the fully qualified distinguished name of 
//  the folder that the deleted object should be moved to.
//
//  Returns S_OK if successful or an HRESULT or LDAP error code otherwise.
//
//***************************************************************************

HRESULT RestoreDeletedObject(LPCWSTR pwszDeletedDN, LPCWSTR pwszDestContainerDN)
{
    if((NULL == pwszDeletedDN) || (NULL == pwszDestContainerDN))
    {
        return E_POINTER;
    }
    
    HRESULT hr = E_FAIL;

    // Build the new distinguished name.
    LPWSTR pwszNewDN = new WCHAR[lstrlenW(pwszDeletedDN) + lstrlenW(pwszDestContainerDN) + 1];
    if(pwszNewDN)
    {
        wcscpy_s(pwszNewDN, pwszDeletedDN);

        // Search for the first 0x0A character. This is the delimiter in the deleted object name.
        LPWSTR pwszChar;
        for(pwszChar = pwszNewDN; *pwszChar; pwszChar = CharNextW(pwszChar))
        {
            if(('\\' == *pwszChar) && ('0' == *(pwszChar + 1)) && ('A' == *(pwszChar + 2)))
            {
                break;
            }
            
        }

        if(0 != *pwszChar)
        {
            // Truncate the name string at the delimiter.
            *pwszChar = 0;

            // Add the last known parent DN to complete the DN.
            wcscat_s(pwszNewDN, L",");
            wcscat_s(pwszNewDN, pwszDestContainerDN);

            PLDAP ld;

            // Initialize LDAP.
            ld = ldap_init(NULL, LDAP_PORT);
            if(NULL != ld) 
            {
                ULONG ulRC;
                ULONG version = LDAP_VERSION3;

                // Set the LDAP version.
                ulRC = ldap_set_option(ld, LDAP_OPT_PROTOCOL_VERSION, (void*)&version);
                if(LDAP_SUCCESS == ulRC)
                {
                    // Establish a connection with the server.
                    ulRC = ldap_connect(ld, NULL);
                    if(LDAP_SUCCESS == ulRC)
                    {                    
                        // Bind to the LDAP server.
                        ulRC = ldap_bind_s(ld, NULL, NULL, LDAP_AUTH_NEGOTIATE);
                        if(LDAP_SUCCESS == ulRC)
                        {
                            // Setup the new values.
                            LPWSTR rgNewVals[] = {pwszNewDN, NULL};

                            /*
                            Remove the isDeleted attribute. This cannot be set 
                            to FALSE or the restore operation will not work.
                            */
                            LDAPModW modIsDeleted = { LDAP_MOD_DELETE, L"isDeleted", NULL };

                            /*
                            Set the new DN, in effect, moving the deleted 
                            object to where it resided before the deletion.
                            */
                            LDAPModW modDN = { LDAP_MOD_REPLACE, L"distinguishedName", rgNewVals };
                            
                            // Initialize the LDAPMod structure.
                            PLDAPModW ldapMods[] = 
                            {
                                &modIsDeleted,
                                &modDN,
                                NULL
                            };

                            /*
                            Use the LDAP_SERVER_SHOW_DELETED_OID control to 
                            modify deleted objects.
                            */
                            LDAPControlW showDeletedControl;
                            showDeletedControl.ldctl_oid = LDAP_SERVER_SHOW_DELETED_OID_W;
                            showDeletedControl.ldctl_value.bv_len = 0;
                            showDeletedControl.ldctl_value.bv_val = NULL;
                            showDeletedControl.ldctl_iscritical = TRUE;

                            // Initialzie the LDAPControl structure
                            PLDAPControlW ldapControls[] = { &showDeletedControl, NULL };

                            /*
                            Modify the specified attributes. This must performed 
                            in one step, which is why the LDAP APIs must be used 
                            to restore a deleted object.
                            */
                            ulRC = ldap_modify_ext_sW(ld, (PWCHAR)pwszDeletedDN, ldapMods, ldapControls, NULL);
                            if(LDAP_SUCCESS == ulRC)
                            {
                                hr = S_OK;
                            }
                            else if(LDAP_ALREADY_EXISTS == ulRC)
                            {
                                /*
                                An object already exists with the specified name 
                                in the specified target container. At this point, 
                                a new name must be selected.
                                */
                            }
                        }
                    }
                }

                if(LDAP_SUCCESS != ulRC)
                {
                    hr = ulRC;
                    
                    OutputDebugString(ldap_err2string(ulRC));
                }

                // Release the LDAP session.
                ldap_unbind(ld);
            }
        }
        else
        {
            /*
            If the end of the string is reached before the delimiter is found, just 
            end and fail.
            */
            hr = E_INVALIDARG;
        }
    
        delete pwszNewDN;
    }
    else
    {
        hr = E_OUTOFMEMORY;
    }

    return hr;
}

```



 

 