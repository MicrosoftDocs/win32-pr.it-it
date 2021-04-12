---
title: Aggiunta di membri a gruppi in un dominio
description: In questo argomento viene illustrato come aggiungere membri ai gruppi in un dominio.
ms.assetid: be65cd4e-df3e-416b-a673-774b71ab6996
ms.tgt_platform: multiple
keywords:
- Aggiunta di membri a gruppi in un dominio Active Directory
- Gruppi AD, aggiunta di membri a gruppi in un dominio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bbd454348dc3eb519d03a7c5574746025c79a3f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472710"
---
# <a name="adding-members-to-groups-in-a-domain"></a>Aggiunta di membri a gruppi in un dominio

Un gruppo può contenere un numero qualsiasi di utenti, contatti o altri gruppi come membri. Nell'elenco seguente sono elencati gli attributi dell'oggetto gruppo che controllano l'appartenenza al gruppo.



| Attributo                                      | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**membro**](/windows/desktop/ADSchema/a-member)<br/>     | L'attributo [**member**](/windows/desktop/ADSchema/a-member) contiene i nomi distinti per gli oggetti che sono membri del gruppo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**memberOf**](/windows/desktop/ADSchema/a-memberof)<br/> | L'attributo [**membro**](/windows/desktop/ADSchema/a-memberof) contiene i nomi distinti dei gruppi che contengono il gruppo come membro diretto. L'attributo **membro** non contiene dati di appartenenza a gruppi ereditati. Ad esempio, se GroupA è un membro di GroupB e GroupB è un membro di GroupC, l'attributo **membro** per GroupA conterrà groupb, ma non GroupC.<br/> Il server Active Directory gestisce questa proprietà. Quando un nome distinto viene aggiunto alla proprietà [**member**](/windows/desktop/ADSchema/a-member) di un altro gruppo, il nome distinto di un altro gruppo viene aggiunto alla proprietà [**member**](/windows/desktop/ADSchema/a-memberof) di questo gruppo.<br/> |



 

Ognuno dei metodi seguenti può essere utilizzato per aggiungere un membro a un gruppo. È possibile aggiungere un membro utilizzando il nome distinto del membro o l'associazione all'oggetto membro e quindi aggiungendo l'oggetto membro all'oggetto gruppo.

Per aggiungere un membro che appartiene a un dominio di livello inferiore a un gruppo in un dominio di livello superiore, utilizzare il formato associabile della stringa SID per il nome distinto. Per ulteriori informazioni e un esempio di codice che illustra come convertire un **objectSID** in una stringa associabile, vedere la funzione di esempio **GetLDAPSidBindStringFromVariantSID** nel [codice di esempio per la conversione di un objectSID in una stringa associabile](example-code-for-converting-an-objectsid-into-a-bindable-string-.md).

<dl> <dt>

<span id="Adding_Members_to_a_Group_by_Using_IADsGroup"></span><span id="adding_members_to_a_group_by_using_iadsgroup"></span><span id="ADDING_MEMBERS_TO_A_GROUP_BY_USING_IADSGROUP"></span>Aggiunta di membri a un gruppo tramite IADsGroup
</dt> <dd>

L'interfaccia [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) può essere utilizzata per aggiungere membri a un gruppo tramite il metodo [**IADsGroup. Add**](/windows/desktop/api/iads/nf-iads-iadsgroup-add) . Associare e ottenere l'interfaccia **IADsGroup** per l'oggetto gruppo. Il metodo **IADsGroup. Add** può quindi essere utilizzato per aggiungere membri al gruppo.

</dd> <dt>

<span id="Adding_Members_to_a_Group_by_Using_IDirectoryObject"></span><span id="adding_members_to_a_group_by_using_idirectoryobject"></span><span id="ADDING_MEMBERS_TO_A_GROUP_BY_USING_IDIRECTORYOBJECT"></span>Aggiunta di membri a un gruppo tramite IDirectoryObject
</dt> <dd>

L'interfaccia [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) può essere usata per aggiungere membri a un gruppo usando il metodo [**IDirectoryObject:: SetObjectAttributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-setobjectattributes) per modificare l'attributo [**member**](/windows/desktop/ADSchema/a-member) per il gruppo. Associare e ottenere l'interfaccia **IDirectoryObject** per l'oggetto gruppo. Usare quindi il metodo **IDirectoryObject:: SetObjectAttributes** per modificare l'attributo **member** .

> [!Note]  
> Poiché l'attributo [**member**](/windows/desktop/ADSchema/a-member) ha più valori, assicurarsi di usare il codice di controllo **\_ \_ Append attr Append** per aggiungere un nome distinto all'attributo **member** . Se si usa il codice di controllo degli **\_ \_ aggiornamenti attr ADS** , i valori dei **membri** esistenti verranno sovrascritti.

 

L'interfaccia [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) può essere usata anche per aggiungere membri a un gruppo quando il gruppo viene creato specificando i membri nel parametro *PAttributeEntries* del metodo [**IDirectoryObject:: CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) .

</dd> <dt>

<span id="Adding_Members_to_a_Group_by_Using_System.DirectoryServices"></span><span id="adding_members_to_a_group_by_using_system.directoryservices"></span><span id="ADDING_MEMBERS_TO_A_GROUP_BY_USING_SYSTEM.DIRECTORYSERVICES"></span>Aggiunta di membri a un gruppo tramite System. DirectoryServices
</dt> <dd>

È possibile utilizzare lo spazio dei nomi [System. DirectoryServices](/dotnet/api/system.directoryservices) per aggiungere membri a un gruppo utilizzando il metodo **PropertyValueCollection. Add** sulla proprietà **member** dell'oggetto Group. Per ulteriori informazioni, vedere [impostazione delle proprietà per gli oggetti directory](/previous-versions/ms180860(v=vs.90)).

</dd> <dt>

<span id="Adding_Members_to_a_Group_by_Using_the_LDAP_API"></span><span id="adding_members_to_a_group_by_using_the_ldap_api"></span><span id="ADDING_MEMBERS_TO_A_GROUP_BY_USING_THE_LDAP_API"></span>Aggiunta di membri a un gruppo tramite l'API LDAP
</dt> <dd>

È possibile utilizzare l'API [Lightweight Directory Access Protocol](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api) per aggiungere membri a un gruppo utilizzando una delle funzioni di [**\_ modifica \* LDAP**](/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_s) . Per ulteriori informazioni, vedere [modifica di una voce di directory](/previous-versions/windows/desktop/ldap/modifying-a-directory-entry).

</dd> </dl>

 

