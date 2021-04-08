---
title: Creazione di un utente
description: Per creare un utente in Active Directory Domain Services, creare un oggetto utente nel contenitore del dominio in cui si desidera inserire l'utente.
ms.assetid: fb51895f-71e1-45b6-b8bc-ed674e822734
ms.tgt_platform: multiple
keywords:
- Esempi di Active Directory Active Directory, creazione di un utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eea10d0142af650d58b61967b008b207abca2c11
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "103873045"
---
# <a name="creating-a-user"></a>Creazione di un utente

Per creare un utente in Active Directory Domain Services, creare un oggetto utente nel contenitore del dominio in cui si desidera inserire l'utente. Gli utenti possono essere creati alla radice del dominio, all'interno di un'unità organizzativa o all'interno di un contenitore.

Quando si crea un oggetto utente, è necessario impostare anche gli attributi, elencati nella tabella seguente, per impostare l'oggetto come utente valido riconosciuto da Active Directory Domain Services e dal sistema di sicurezza di Windows.



| Attributo                                       | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**cn**](/windows/desktop/ADSchema/a-cn)                         | Specifica il nome dell'oggetto utente nella directory. Si tratta del nome distinto relativo (RDN) dell'oggetto.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) | Specifica una stringa che rappresenta il nome utilizzato per supportare client e server di una versione precedente di Windows. Il valore di [**sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) deve essere composto da meno di 20 caratteri per supportare i client di una versione precedente di Windows.<br/> [**SAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) deve essere univoco tra tutti gli oggetti entità di sicurezza all'interno del dominio. È necessario eseguire una query sul dominio per verificare che **sAMAccountName** sia univoco all'interno del dominio.<br/> [**sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) è un attributo facoltativo. Il server creerà un valore **sAMAccountName** casuale se non ne viene specificato alcuno.<br/> |



 

È anche possibile impostare altri attributi. Gli attributi utente seguenti vengono impostati con i valori predefiniti se non vengono impostati in modo esplicito al momento della creazione.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Attributo</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/ADSchema/a-accountexpires"><strong>accountExpires</strong></a></td>
<td>Specifica la scadenza dell'account. Il valore predefinito è <strong>TIMEQ_FOREVER</strong>, che indica che l'account non scadrà mai.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/ADSchema/a-ntsecuritydescriptor"><strong>nTSecurityDescriptor</strong></a></td>
<td>Viene creato un descrittore di sicurezza in base a regole specifiche. Per ulteriori informazioni, vedere <a href="how-security-descriptors-are-set-on-new-directory-objects.md">la pagina relativa alla modalità di impostazione dei descrittori di sicurezza per i nuovi oggetti directory</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/ADSchema/a-objectcategory"><strong>objectCategory</strong></a></td>
<td>Specifica la categoria dell'utente. Il valore predefinito è &quot; Person &quot; .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/ADSchema/a-name"><strong>nome</strong></a></td>
<td>Specifica il nome utente. Il valore predefinito è il valore impostato per <a href="/windows/desktop/ADSchema/a-cn"><strong>CN</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/ADSchema/a-pwdlastset"><strong>pwdLastSet</strong></a></td>
<td>Specifica la data dell'ultima impostazione della password da parte dell'utente. Il valore predefinito è zero, che indica che l'utente deve modificare la password all'accesso successivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/ADSchema/a-useraccountcontrol"><strong>userAccountControl</strong></a></td>
<td>Contiene valori che determinano diverse funzionalità di accesso e account per l'utente.<br/> Per impostazione predefinita, vengono impostati i flag seguenti:<br/>
<ul>
<li><strong>UF_ACCOUNTDISABLE</strong> - L'account è disabilitato.</li>
<li><strong>UF_PASSWD_NOTREQD</strong> - Non è necessaria alcuna password.</li>
<li><strong>UF_NORMAL_ACCOUNT</strong> - Tipo di account predefinito che rappresenta un utente tipico.</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/ADSchema/a-memberof"><strong>memberOf</strong></a></td>
<td>Specifica il gruppo o i gruppi di cui l'utente è membro diretto. Il valore predefinito è &quot; Domain Users &quot; .<br/></td>
</tr>
</tbody>
</table>



 

Un utente viene creato mediante associazione al contenitore desiderato e quindi utilizzando uno dei metodi seguenti. È necessario impostare gli attributi [**CN**](/windows/desktop/ADSchema/a-cn) e [**sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) prima di eseguire il commit dell'utente nel server.



| Metodo                                                                       | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IADsContainer. Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create)                        | L'attributo [**CN**](/windows/desktop/ADSchema/a-cn) viene tratto dal parametro *bstrRelativeName* . È necessario eseguire il commit del nuovo utente chiamando [**IADs. SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) oppure l'oggetto non verrà creato. Per ulteriori informazioni, vedere [il codice di esempio per la creazione di un utente](example-code-for-creating-a-user.md).<br/>                                                                                            |
| [**IDirectoryObject::CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) | L'attributo [**CN**](/windows/desktop/ADSchema/a-cn) viene tratto dal parametro *pszRDNName* . Viene eseguito il commit del nuovo utente quando viene chiamato [**CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) . Per ulteriori informazioni, vedere [il codice di esempio per la creazione di un utente](example-code-for-creating-a-user.md).<br/>                                                                                                                |
| [DirectoryEntries. Add](/dotnet/api/system.directoryservices.directoryentries.add?view=dotnet-plat-ext-3.1)       | L'attributo [**CN**](/windows/desktop/ADSchema/a-cn) viene tratto dal parametro *Name* . È necessario eseguire il commit del nuovo oggetto utente chiamando [DirectoryEntry. CommitChanges](/dotnet/api/system.directoryservices.directoryentry.commitchanges#System_DirectoryServices_DirectoryEntry_CommitChanges) oppure l'oggetto non verrà creato. Per ulteriori informazioni, vedere [aggiunta di oggetti directory](/previous-versions/ms180851(v=vs.90)).<br/> |



 

È necessario eseguire il commit del nuovo utente nel server prima di poter modificare qualsiasi attributo diverso da [**CN**](/windows/desktop/ADSchema/a-cn) e [**sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) . Questo è dovuto al fatto che l'account utente non esiste in realtà fino a quando non viene eseguito il commit dell'utente. Se un attributo viene recuperato o modificato per un oggetto che non esiste nel server, si verificherà un errore. Ciò include la chiamata al metodo [**IADsUser. sepassword**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword) . Ad esempio, quando si crea un utente con [**IADsContainer. Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create), viene seguita la sequenza seguente:

1.  Chiamare [**IADsContainer. Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) per creare l'utente nella cache locale con il [**CN**](/windows/desktop/ADSchema/a-cn)specificato.
2.  Impostare l'attributo [**sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) sul valore desiderato con il metodo [**IADs. Put**](/windows/desktop/api/iads/nf-iads-iads-put) .
3.  Modificare ora altri attributi, ad esempio [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol). Questa restrizione si applica anche alle proprietà ADSI, ad esempio [**IADsUser. accountdisabled**](/windows/desktop/ADSI/iadsuser-property-methods), e ai metodi come [**IADsUser. password**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword).
4.  Chiamare [**IADs. SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) per eseguire il commit del nuovo utente nel server.

Quando viene creato un nuovo account utente, questo viene disabilitato per impostazione predefinita. L'account deve essere abilitato manualmente o a livello di codice. Per abilitare un account utente a livello di codice, rimuovere il flag **Ads \_ UF \_ ACCOUNTDISABLE** dall'attributo [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol) .

Quando viene creato un nuovo account utente, l'attributo [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol) per l'account include automaticamente il flag **UF \_ passwd \_ NOTREQD** , che indica che non è necessaria alcuna password per l'account. Se per i criteri di sicurezza del dominio in cui è stato creato l'account è richiesta una password per tutti gli account utente, è necessario rimuovere il flag **UF \_ passwd \_ NOTREQD** dall'attributo **userAccountControl** per l'account.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codice di esempio per la creazione di un utente](example-code-for-creating-a-user.md)
</dt> </dl>