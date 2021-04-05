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
# <a name="restoring-deleted-objects"></a>Ripristino di oggetti eliminati

Windows Server 2003 include la funzionalità "Ripristina oggetti eliminati".

Per abilitare il ripristino degli oggetti eliminati, è necessario che almeno un controller di dominio nel dominio sia in esecuzione in Windows Server 2003 o in una versione successiva di Windows. Per impostazione predefinita, solo gli amministratori di dominio possono ripristinare gli oggetti eliminati, anche se possono essere delegati ad altri.

Per il ripristino degli oggetti eliminati si applicano le limitazioni seguenti:

-   Non è possibile ripristinare un oggetto quando la durata della rimozione definitiva per l'oggetto è scaduta perché quando la durata della rimozione definitiva è scaduta, l'oggetto viene eliminato definitivamente.
-   Gli oggetti presenti nella radice del contesto dei nomi, ad esempio un dominio o una partizione di applicazione, non possono essere ripristinati.
-   Impossibile ripristinare gli oggetti dello schema. Gli oggetti dello schema non devono mai essere eliminati.
-   È possibile ripristinare i contenitori eliminati, ma il ripristino degli oggetti eliminati presenti nel contenitore prima dell'eliminazione è difficile perché la struttura ad albero sotto il contenitore deve essere ricostruita manualmente.

## <a name="permissions-required-to-restore-a-deleted-object"></a>Autorizzazioni necessarie per ripristinare un oggetto eliminato

Quando un oggetto viene eliminato, viene mantenuto il descrittore di sicurezza dell'oggetto. Sebbene il proprietario sia identificabile dal descrittore di sicurezza, per motivi di sicurezza, solo gli amministratori di dominio possono ripristinare gli oggetti eliminati. Gli amministratori di dominio possono concedere l'autorizzazione per il ripristino degli oggetti Delete ad altri utenti e gruppi concedendo all'utente o al gruppo il diritto di accesso al controllo "reanimate Tombstone". Alla radice del contesto dei nomi viene concesso il diritto di accesso del controllo "reanimato per la rimozione definitiva". Solo gli utenti che dispongono dell'autorizzazione di accesso in lettura per un oggetto e i relativi attributi sono autorizzati a leggere l'oggetto e gli attributi accessibili dopo l'eliminazione dell'oggetto.

> [!Note]  
> Concessione a un utente questa autorizzazione può costituire un rischio per la sicurezza perché potrebbe consentire all'utente di ripristinare un oggetto account che ha accesso alle risorse di cui l'utente non ha normalmente accesso. Tramite il ripristino di un account, l'utente acquisisce essenzialmente il controllo di questo account perché l'utente deve impostare la password iniziale per l'account quando viene ripristinato l'account.

 

Per ripristinare completamente un oggetto eliminato, l'utente deve:

-   Avere o essere un membro di un gruppo che dispone di, il diritto di accesso del controllo "reanimato per la rimozione definitiva".

-   Avere accesso in scrittura per ogni attributo obbligatorio che richiede l'aggiornamento.

-   Hanno accesso in scrittura al nome distinto relativo (RDN).

-   Avere accesso in scrittura a ogni attributo facoltativo che deve essere aggiornato.

-   Disporre dei diritti di creazione figlio sul contenitore di destinazione per la classe di oggetti dell'oggetto ripristinato.

    > [!Note]  
    > L'attributo **Indeleted** non viene verificato durante l'operazione di ripristino. Né verrà verificata l'autorizzazione Delete-Child per il contenitore "Deleted Objects".

     

## <a name="restoring-a-deleted-object"></a>Ripristino di un oggetto eliminato

Per ripristinare un oggetto eliminato, è innanzitutto necessario che l'oggetto si trovi nel contenitore degli oggetti eliminati. Per ulteriori informazioni sul recupero di oggetti eliminati, vedere [recupero di oggetti eliminati](retrieving-deleted-objects.md).

Quando l'oggetto è stato individuato, le operazioni seguenti devono essere completate in una singola operazione LDAP. Questa operazione richiede l'uso della funzione [**LDAP \_ Modify \_ ext \_ s**](/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_ext_s) con il [**server LDAP che mostra il controllo \_ \_ \_ \_ OID eliminato**](/previous-versions/windows/desktop/ldap/ldap-server-show-deleted-oid) .

-   Rimuovere il valore dell'attributo **Andeleted** . Il valore dell'attributo **undeleted** deve essere rimosso e non impostato su **false**.
-   Sostituire il nome distinto dell'oggetto in modo che venga spostato in un contenitore diverso dal contenitore degli oggetti eliminati. Può trattarsi di qualsiasi contenitore che in genere può contenere l'oggetto. Il nome distinto del contenitore precedente dell'oggetto può essere trovato nell'attributo **lastKnownParent** dell'oggetto eliminato. L'attributo **lastKnownParent** viene impostato solo se l'oggetto è stato eliminato in un controller di dominio Windows Server 2003. È pertanto possibile che il contenuto dell'attributo **lastKnownParent** non sia accurato.
-   Ripristinare gli attributi obbligatori per l'oggetto che sono stati cancellati durante l'eliminazione.

> [!Note]  
> L'attributo **objectCategory** può essere impostato anche quando l'oggetto viene ripristinato, ma non è obbligatorio. Se non viene specificato alcun valore **objectCategory** , viene utilizzato il **objectCategory** predefinito per **objectClass** dell'oggetto.

 

Dopo che l'oggetto è stato ripristinato, è possibile accedervi come prima dell'eliminazione. A questo punto, è necessario ripristinare tutti gli attributi facoltativi importanti. È necessario ripristinare anche tutti i riferimenti all'oggetto da altri oggetti nella directory.

Come misura di sicurezza, gli oggetti utente vengono disabilitati quando vengono ripristinati. Gli oggetti utente devono essere abilitati dopo il ripristino degli attributi facoltativi per consentire l'utilizzo dell'oggetto utente.

Per ulteriori informazioni e un esempio di codice che illustra come ripristinare un oggetto eliminato, vedere la funzione RestoreDeletedObject riportata di seguito.

## <a name="restoredeletedobject"></a>RestoreDeletedObject

Nell'esempio di codice C++ riportato di seguito viene illustrato come ripristinare un oggetto eliminato.


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



 

 