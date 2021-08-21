---
title: Ripristino di oggetti eliminati
description: Windows Server 2003 include \ 0034; ripristinare gli oggetti eliminati \ 0034; Funzionalità.
ms.assetid: b64c5c91-fb76-4323-b78d-f692aa887c96
ms.tgt_platform: multiple
keywords:
- Ripristino degli oggetti eliminati ad Active Directory
- Active Directory, uso, ripristino di oggetti eliminati
- oggetti AD , ripristino di oggetti eliminati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 431bcddcbd15366a6accf9b8368fa8d34377b27af923fb102803b6316462634e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025119"
---
# <a name="restoring-deleted-objects"></a>Ripristino di oggetti eliminati

Windows Server 2003 include la funzionalità "Ripristina oggetti eliminati".

Per abilitare il ripristino degli oggetti eliminati, è necessario che almeno un controller di dominio nel dominio sia in esecuzione in Windows Server 2003 o una versione successiva di Windows. Per impostazione predefinita, solo gli amministratori di dominio possono ripristinare gli oggetti eliminati, anche se questa operazione può essere delegata ad altri utenti.

Al ripristino degli oggetti eliminati si applicano le limitazioni seguenti:

-   Non è possibile ripristinare un oggetto quando la durata di rimozione definitiva per l'oggetto è scaduta perché, quando la durata di rimozione definitiva è scaduta, l'oggetto viene eliminato definitivamente.
-   Gli oggetti presenti nella radice del contesto dei nomi, ad esempio un dominio o una partizione applicativa, non possono essere ripristinati.
-   Gli oggetti dello schema non possono essere ripristinati. Gli oggetti dello schema non devono mai essere eliminati.
-   È possibile ripristinare i contenitori eliminati, ma il ripristino degli oggetti eliminati presenti nel contenitore prima dell'eliminazione è difficile perché la struttura ad albero nel contenitore deve essere ricostruita manualmente.

## <a name="permissions-required-to-restore-a-deleted-object"></a>Autorizzazioni necessarie per ripristinare un oggetto eliminato

Quando un oggetto viene eliminato, il descrittore di sicurezza dell'oggetto viene mantenuto. Anche se il proprietario è identificabile dal descrittore di sicurezza, per motivi di sicurezza, solo gli amministratori di dominio sono autorizzati a ripristinare gli oggetti eliminati. Gli amministratori di dominio possono concedere l'autorizzazione per ripristinare oggetti di eliminazione ad altri utenti e gruppi concedendo all'utente o al gruppo il diritto di controllo "Rianimate Tombstone". Il diritto di accesso di controllo "Reanimate Tombstone" viene concesso nella radice del contesto di denominazione. Solo gli utenti che avevano l'autorizzazione di accesso in lettura per un oggetto e i relativi attributi sono autorizzati a leggere l'oggetto e gli attributi accessibili dopo l'eliminazione dell'oggetto.

> [!Note]  
> La concessione di questa autorizzazione a un utente può essere un rischio per la sicurezza perché potrebbe consentire all'utente di ripristinare un oggetto account che abbia accesso alle risorse a cui l'utente normalmente non ha accesso. Ripristinando un account, l'utente ottiene essenzialmente il controllo di questo account perché deve impostare la password iniziale per l'account quando l'account viene ripristinato.

 

Per ripristinare completamente un oggetto eliminato, l'utente deve:

-   Avere o essere un membro di un gruppo che dispone del diritto di accesso "Rianimate Tombstone".

-   Avere accesso in scrittura per ogni attributo obbligatorio che richiede l'aggiornamento.

-   Avere accesso in scrittura al nome distinto relativo (RDN).

-   Avere accesso in scrittura a ogni attributo facoltativo che deve essere aggiornato.

-   Disporre dei diritti di creazione figlio per il contenitore di destinazione per la classe di oggetti dell'oggetto ripristinato.

    > [!Note]  
    > **L'attributo isDeleted** non viene verificato durante l'operazione di ripristino. Né l'autorizzazione delete-child per il contenitore "Deleted Objects" verrà verificata.

     

## <a name="restoring-a-deleted-object"></a>Ripristino di un oggetto eliminato

Per ripristinare un oggetto eliminato, è necessario innanzitutto che l'oggetto si trovi nel contenitore Oggetti eliminati. Per altre informazioni sul recupero di oggetti eliminati, vedere [Recupero di oggetti eliminati.](retrieving-deleted-objects.md)

Dopo aver individuato l'oggetto, è necessario completare le operazioni seguenti in una singola operazione LDAP. Questa operazione richiede l'uso della [**funzione ldap \_ modify \_ ext \_ s**](/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_ext_s) con il [**controllo OID LDAP \_ SERVER SHOW \_ \_ DELETED. \_**](/previous-versions/windows/desktop/ldap/ldap-server-show-deleted-oid)

-   Rimuovere il **valore dell'attributo isDeleted.** Il **valore dell'attributo isDeleted** deve essere rimosso, non impostato su **FALSE.**
-   Sostituire il nome distinto dell'oggetto in modo che sia spostato in un contenitore diverso dal contenitore Oggetti eliminati. Può trattarsi di qualsiasi contenitore che in genere può contenere l'oggetto . Il nome distinto del contenitore precedente dell'oggetto è disponibile nell'attributo **lastKnownParent** dell'oggetto eliminato. **L'attributo lastKnownParent** viene impostato solo se l'oggetto è stato eliminato in un controller di dominio Windows Server 2003. Di conseguenza, è possibile che il contenuto **dell'attributo lastKnownParent** non sia accurato.
-   Ripristinare gli attributi obbligatori per l'oggetto cancellati durante l'eliminazione.

> [!Note]  
> **L'attributo objectCategory** può essere impostato anche quando l'oggetto viene ripristinato, ma non è obbligatorio. Se non viene specificato alcun valore **objectCategory,** viene usato **il valore objectCategory predefinito** per **objectClass** dell'oggetto.

 

Dopo il ripristino, l'oggetto è accessibile come prima dell'eliminazione. A questo punto, tutti gli attributi facoltativi importanti devono essere ripristinati. È necessario ripristinare anche tutti i riferimenti all'oggetto da altri oggetti nella directory.

Come misura di sicurezza, gli oggetti utente vengono disabilitati quando vengono ripristinati. Gli oggetti utente devono essere abilitati dopo il ripristino degli attributi facoltativi per consentire l'utilizzo dell'oggetto utente.

Per altre informazioni e un esempio di codice che illustra come ripristinare un oggetto eliminato, vedere la funzione RestoreDeletedObject riportata di seguito.

## <a name="restoredeletedobject"></a>RestoreDeletedObject

Nell'esempio di codice C++ seguente viene illustrato come ripristinare un oggetto eliminato.


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



 

 