---
title: Creazione di un utente
description: Per creare un utente in Active Directory Domain Services, creare un oggetto utente nel contenitore di dominio del dominio in cui si vuole inserire l'utente.
ms.assetid: fb51895f-71e1-45b6-b8bc-ed674e822734
ms.tgt_platform: multiple
keywords:
- Esempi di Active Directory Active Directory, creazione di un utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3422d269351ae29fd15d12585ca02b91a4b9c23
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469228"
---
# <a name="creating-a-user"></a>Creazione di un utente

Per creare un utente in Active Directory Domain Services, creare un oggetto utente nel contenitore di dominio del dominio in cui si vuole inserire l'utente. Gli utenti possono essere creati nella radice del dominio, all'interno di un'unità organizzativa o all'interno di un contenitore.

Quando si crea un oggetto utente, è necessario impostare anche gli attributi elencati nella tabella seguente per impostare l'oggetto come utente legale riconosciuto da Active Directory Domain Services e dal sistema Sicurezza di Windows.



| Attributo                                       | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**cn**](/windows/desktop/ADSchema/a-cn)                         | Specifica il nome dell'oggetto utente nella directory. Si tratta del nome distinto relativo (RDN) dell'oggetto.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) | Specifica una stringa che rappresenta il nome utilizzato per supportare client e server da una versione precedente di Windows. [**SAMAccountName deve**](/windows/desktop/ADSchema/a-samaccountname) contenere meno di 20 caratteri per supportare i client di una versione precedente di Windows.<br/> [**SAMAccountName deve essere**](/windows/desktop/ADSchema/a-samaccountname) univoco tra tutti gli oggetti entità di sicurezza all'interno del dominio. È necessario eseguire una query sul dominio per verificare che **sAMAccountName** sia univoco all'interno del dominio.<br/> [**sAMAccountName è**](/windows/desktop/ADSchema/a-samaccountname) un attributo facoltativo. Il server creerà un valore **sAMAccountName casuale** se non ne viene specificato nessuno.<br/> |



 

È anche possibile impostare altri attributi. Gli attributi utente seguenti vengono impostati con valori predefiniti se non vengono impostati in modo esplicito al momento della creazione.




| Attributo | Descrizione | 
|-----------|-------------|
| <a href="/windows/desktop/ADSchema/a-accountexpires"><strong>accountExpires</strong></a> | Specifica quando l'account scadrà. Il valore predefinito <strong>TIMEQ_FOREVER</strong>, che indica che l'account non scadrà mai.<br /> | 
| <a href="/windows/desktop/ADSchema/a-ntsecuritydescriptor"><strong>Ntsecuritydescriptor</strong></a> | Un descrittore di sicurezza viene creato in base a regole specifiche. Per altre informazioni, vedere <a href="how-security-descriptors-are-set-on-new-directory-objects.md">How Security Descriptors are Set on New Directory Objects</a>.<br /> | 
| <a href="/windows/desktop/ADSchema/a-objectcategory"><strong>objectCategory</strong></a> | Specifica la categoria utente. Il valore predefinito è "Person".<br /> | 
| <a href="/windows/desktop/ADSchema/a-name"><strong>Nome</strong></a> | Specifica il nome utente. Il valore predefinito è il valore impostato per <a href="/windows/desktop/ADSchema/a-cn"><strong>cn</strong></a>.<br /> | 
| <a href="/windows/desktop/ADSchema/a-pwdlastset"><strong>pwdLastSet</strong></a> | Specifica quando l'utente ha impostato la password per l'ultima volta. Il valore predefinito è zero, che indica che l'utente deve modificare la password all'accesso successivo.<br /> | 
| <a href="/windows/desktop/ADSchema/a-useraccountcontrol"><strong>userAccountControl</strong></a> | Contiene valori che determinano diverse funzionalità di accesso e account per l'utente.<br /> Per impostazione predefinita, vengono impostati i flag seguenti:<br /><ul><li><strong>UF_ACCOUNTDISABLE:</strong> l'account è disabilitato.</li><li><strong>UF_PASSWD_NOTREQD:</strong> non è richiesta alcuna password.</li><li><strong>UF_NORMAL_ACCOUNT:</strong> tipo di account predefinito che rappresenta un utente tipico.</li></ul> | 
| <a href="/windows/desktop/ADSchema/a-memberof"><strong>memberOf</strong></a> | Specifica il gruppo o i gruppi di cui l'utente è membro diretto. Il valore predefinito è "Domain Users".<br /> | 




 

Un utente viene creato tramite l'associazione al contenitore desiderato e quindi usando uno dei metodi seguenti. Gli [**attributi cn**](/windows/desktop/ADSchema/a-cn) e [**sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) devono essere impostati prima che venga eseguito il commit dell'utente nel server.



| Metodo                                                                       | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IADsContainer.Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create)                        | [**L'attributo cn**](/windows/desktop/ADSchema/a-cn) deriva dal *parametro bstrRelativeName.* È necessario eseguire il commit del nuovo utente chiamando [**IADs.SetInfo,**](/windows/desktop/api/iads/nf-iads-iads-setinfo) in caso non verrà creato l'oggetto. Per altre informazioni, vedere [Codice di esempio per la creazione di un utente.](example-code-for-creating-a-user.md)<br/>                                                                                            |
| [**IDirectoryObject::CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) | [**L'attributo cn**](/windows/desktop/ADSchema/a-cn) viene derivato dal *parametro pszRDNName.* Il commit del nuovo utente viene eseguito [**quando viene chiamato CreateDSObject.**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) Per altre informazioni, vedere [Codice di esempio per la creazione di un utente.](example-code-for-creating-a-user.md)<br/>                                                                                                                |
| [DirectoryEntries.Add](/dotnet/api/system.directoryservices.directoryentries.add?view=dotnet-plat-ext-3.1)       | [**L'attributo cn**](/windows/desktop/ADSchema/a-cn) deriva dal *parametro name.* Il commit del nuovo oggetto utente deve essere eseguito chiamando [DirectoryEntry.CommitChanges,](/dotnet/api/system.directoryservices.directoryentry.commitchanges#System_DirectoryServices_DirectoryEntry_CommitChanges) in caso non verrà creato l'oggetto. Per altre informazioni, vedere [Aggiunta di oggetti directory.](/previous-versions/ms180851(v=vs.90))<br/> |



 

Per poter modificare gli attributi diversi da [**cn**](/windows/desktop/ADSchema/a-cn) e [**sAMAccountName,**](/windows/desktop/ADSchema/a-samaccountname) è necessario eseguire il commit del nuovo utente nel server. Ciò è dovuto al fatto che l'account utente non esiste fino a quando non viene eseguito il commit dell'utente. Se un attributo viene recuperato o modificato per un oggetto che non esiste nel server, si verificherà un errore. Ciò include la chiamata [**al metodo IADsUser.SetPassword.**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword) Ad esempio, la sequenza seguente viene seguita quando si crea un utente con [**IADsContainer.Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create):

1.  Chiamare [**IADsContainer.Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) per creare l'utente nella cache locale con il [**cn specificato.**](/windows/desktop/ADSchema/a-cn)
2.  Impostare [**l'attributo sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) sul valore desiderato con il [**metodo IADs.Put.**](/windows/desktop/api/iads/nf-iads-iads-put)
3.  Modificare ora altri attributi, ad esempio [**userAccountControl.**](/windows/desktop/ADSchema/a-useraccountcontrol) Questa restrizione si applica anche alle proprietà ADSI, ad esempio [**IADsUser.AccountDisabled**](/windows/desktop/ADSI/iadsuser-property-methods), e ai metodi come [**IADsUser.SetPassword**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword).
4.  Chiamare [**IADs.SetInfo per**](/windows/desktop/api/iads/nf-iads-iads-setinfo) eseguire il commit del nuovo utente nel server.

Quando viene creato, un nuovo account utente viene disabilitato per impostazione predefinita. L'account deve essere abilitato manualmente o a livello di codice. Per abilitare un account utente a livello di codice, rimuovere il flag **\_ ADS UF \_ ACCOUNTDISABLE** [**dall'attributo userAccountControl.**](/windows/desktop/ADSchema/a-useraccountcontrol)

Quando viene creato un nuovo account utente, l'attributo [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol) per l'account ha automaticamente il flag **UF \_ PASSWD \_ NOTREQD** impostato, che indica che non è necessaria alcuna password per l'account. Se i criteri di sicurezza del dominio in cui viene creato l'account richiedono una password per tutti gli account utente, il flag **\_ UF PASSWD \_ NOTREQD** deve essere rimosso dall'attributo **userAccountControl** per l'account.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codice di esempio per la creazione di un utente](example-code-for-creating-a-user.md)
</dt> </dl>
