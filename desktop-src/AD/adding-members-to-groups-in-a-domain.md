---
title: Aggiunta di membri a gruppi in un dominio
description: In questo argomento viene illustrato come aggiungere membri ai gruppi in un dominio.
ms.assetid: be65cd4e-df3e-416b-a673-774b71ab6996
ms.tgt_platform: multiple
keywords:
- Aggiunta di membri a gruppi in un dominio AD
- Groups AD , Adding Members to Groups in a Domain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21c9f0c85943752b42cf3d9d8b88d385aaba9e014b21aa9f538955cb49b1a750
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118024758"
---
# <a name="adding-members-to-groups-in-a-domain"></a>Aggiunta di membri a gruppi in un dominio

Un gruppo può contenere un numero qualsiasi di utenti, contatti o altri gruppi come membri. Nell'elenco seguente sono elencati gli attributi dell'oggetto gruppo che controllano l'appartenenza al gruppo.



| Attributo                                      | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Membro**](/windows/desktop/ADSchema/a-member)<br/>     | [**L'attributo**](/windows/desktop/ADSchema/a-member) member contiene i nomi distinti per gli oggetti che sono membri del gruppo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**memberOf**](/windows/desktop/ADSchema/a-memberof)<br/> | [**L'attributo memberOf**](/windows/desktop/ADSchema/a-memberof) contiene i nomi distinti dei gruppi che contengono il gruppo come membro diretto. **L'attributo memberOf** non contiene dati di appartenenza a gruppi ereditati. Ad esempio, se GroupA è un membro di GroupB e GroupB è un membro di GroupC, l'attributo **memberOf** per GroupA conterrà GroupB, ma non GroupC.<br/> Il server Active Directory gestisce questa proprietà. Quando un nome distinto viene aggiunto alla proprietà [**member**](/windows/desktop/ADSchema/a-member) di un altro gruppo, il nome distinto dell'altro gruppo viene aggiunto alla [**proprietà memberOf di questo**](/windows/desktop/ADSchema/a-memberof) gruppo.<br/> |



 

Ognuno dei metodi seguenti può essere usato per aggiungere un membro a un gruppo. È possibile aggiungere un membro usando il nome distinto del membro o l'associazione all'oggetto membro e quindi aggiungendo l'oggetto membro all'oggetto gruppo.

Per aggiungere un membro appartenente a un dominio di livello inferiore a un gruppo in un dominio di livello superiore, usare il formato associabile della stringa SID per il nome distinto. Per altre informazioni e un esempio di codice che illustra come convertire **un objectSid** in una stringa associabile, vedere la funzione di esempio **GetLDAPSidBindStringFromVariantSID** in Codice di esempio per la conversione di [un objectSid in una stringa associabile.](example-code-for-converting-an-objectsid-into-a-bindable-string-.md)

<dl> <dt>

<span id="Adding_Members_to_a_Group_by_Using_IADsGroup"></span><span id="adding_members_to_a_group_by_using_iadsgroup"></span><span id="ADDING_MEMBERS_TO_A_GROUP_BY_USING_IADSGROUP"></span>Aggiunta di membri a un gruppo tramite IADsGroup
</dt> <dd>

[**L'interfaccia IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) può essere usata per aggiungere membri a un gruppo usando il [**metodo IADsGroup.Add.**](/windows/desktop/api/iads/nf-iads-iadsgroup-add) Eseguire il binding a e ottenere **l'interfaccia IADsGroup** per l'oggetto gruppo. È quindi **possibile usare il metodo IADsGroup.Add** per aggiungere membri al gruppo.

</dd> <dt>

<span id="Adding_Members_to_a_Group_by_Using_IDirectoryObject"></span><span id="adding_members_to_a_group_by_using_idirectoryobject"></span><span id="ADDING_MEMBERS_TO_A_GROUP_BY_USING_IDIRECTORYOBJECT"></span>Aggiunta di membri a un gruppo tramite IDirectoryObject
</dt> <dd>

[**L'interfaccia IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) può essere usata per aggiungere membri a un gruppo usando il [](/windows/desktop/ADSchema/a-member) metodo [**IDirectoryObject::SetObjectAttributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-setobjectattributes) per modificare l'attributo del membro per il gruppo. Eseguire il binding a e ottenere **l'interfaccia IDirectoryObject** per l'oggetto gruppo. Usare quindi il **metodo IDirectoryObject::SetObjectAttributes** per modificare l'attributo **del** membro.

> [!Note]  
> Poiché [**l'attributo**](/windows/desktop/ADSchema/a-member) membro ha più valori, assicurarsi di usare il codice del controllo **\_ \_ ADS ATTR APPEND** per aggiungere un nome distinto all'attributo **del** membro. **L'uso del codice di controllo \_ \_ ADS ATTR UPDATE** causerà la sovrascrittura dei valori dei membri esistenti. 

 

[**L'interfaccia IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) può essere usata anche per aggiungere membri a un gruppo quando il gruppo viene creato specificando i membri nel *parametro pAttributeEntries* del metodo [**IDirectoryObject::CreateDSObject.**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject)

</dd> <dt>

<span id="Adding_Members_to_a_Group_by_Using_System.DirectoryServices"></span><span id="adding_members_to_a_group_by_using_system.directoryservices"></span><span id="ADDING_MEMBERS_TO_A_GROUP_BY_USING_SYSTEM.DIRECTORYSERVICES"></span>Aggiunta di membri a un gruppo tramite System.DirectoryServices
</dt> <dd>

È possibile usare lo spazio dei nomi [System.DirectoryServices](/dotnet/api/system.directoryservices) per aggiungere membri a un gruppo usando il **metodo PropertyValueCollection.Add** nella proprietà **membro** dell'oggetto gruppo. Per altre informazioni, vedere [Impostazione delle proprietà sugli oggetti directory.](/previous-versions/ms180860(v=vs.90))

</dd> <dt>

<span id="Adding_Members_to_a_Group_by_Using_the_LDAP_API"></span><span id="adding_members_to_a_group_by_using_the_ldap_api"></span><span id="ADDING_MEMBERS_TO_A_GROUP_BY_USING_THE_LDAP_API"></span>Aggiunta di membri a un gruppo tramite l'API LDAP
</dt> <dd>

È possibile [](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api) usare l Lightweight Directory Access Protocol API per aggiungere membri a un gruppo usando una delle [**funzioni ldap \_ modify. \***](/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_s) Per altre informazioni, vedere [Modifica di una voce di directory.](/previous-versions/windows/desktop/ldap/modifying-a-directory-entry)

</dd> </dl>

 

