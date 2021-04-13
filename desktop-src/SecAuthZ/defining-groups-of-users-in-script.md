---
description: Un oggetto IAzApplicationGroup rappresenta un gruppo di utenti. I ruoli possono quindi essere assegnati a questo gruppo di utenti collettivamente. Un oggetto IAzApplicationGroup può includere anche altri oggetti IAzApplicationGroup come membri.
ms.assetid: 8b445419-7316-4034-b742-a05845af1862
title: Definizione di gruppi di utenti nello script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4f0b652530167c71fbea7bc23d27434ae458f9b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348936"
---
# <a name="defining-groups-of-users-in-script"></a>Definizione di gruppi di utenti nello script

In Gestione autorizzazioni, un oggetto [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) rappresenta un gruppo di utenti. I ruoli possono quindi essere assegnati a questo gruppo di utenti collettivamente. Un oggetto **IAzApplicationGroup** può includere anche altri oggetti **IAzApplicationGroup** come membri. Per ulteriori informazioni sui gruppi di applicazioni, vedere [utenti e gruppi](users-and-groups.md).

Un gruppo può essere definito da elenchi espliciti di membri e non membri o da una query LDAP ( [*Lightweight Directory Access Protocol*](/windows/desktop/SecGloss/l-gly) ). Negli esempi seguenti viene illustrato come creare ogni tipo di gruppo di applicazioni:

-   [Creazione di un gruppo di base](#creating-a-basic-group)
-   [Creazione di un gruppo di query LDAP](#creating-an-ldap-query-group)

## <a name="creating-a-basic-group"></a>Creazione di un gruppo di base

Un gruppo di applicazioni di base viene definito dai membri inclusi nelle proprietà [**membri**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_members) e non [**membri**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_nonmembers) dell'oggetto [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) che rappresenta il gruppo. Gli utenti e i gruppi elencati nella proprietà **membri** sono inclusi nel gruppo di applicazioni e gli utenti e i gruppi elencati nella proprietà non **membri** vengono esclusi dal gruppo di applicazioni. L'elenco nella proprietà non **Members** sostituisce l'elenco nella proprietà **Members** .

Nell'esempio seguente viene illustrato come creare un gruppo di applicazioni di base e come aggiungere tutti gli utenti locali come membri del gruppo. Nell'esempio si presuppone l'esistenza di un archivio criteri XML denominato MyStore.xml nella directory radice dell'unità C.


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, "msxml://C:\MyStore.xml"

'  Create an application object in the store.
Dim expenseApp
Set expenseApp= AzManStore.OpenApplication("Expense")

'  Create an application group object.
Dim appGroup
Set appGroup = expenseApp.CreateApplicationGroup("Trusted Users")

'  Add a well-known SID for all local users to the group.
appGroup.AddMember("S-1-1-0")

'  Save the application group to the store.
appGroup.Submit
```



## <a name="creating-an-ldap-query-group"></a>Creazione di un gruppo di query LDAP

Un gruppo di query LDAP ha un'appartenenza definita dalla query contenuta nel valore della relativa proprietà [**LdapQuery**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_ldapquery) .

Nell'esempio seguente viene illustrato come creare un gruppo di applicazioni di query LDAP e come aggiungere tutti gli utenti come membri di tale gruppo. Nell'esempio si presuppone l'esistenza di un archivio criteri XML denominato MyStore.xml nella directory radice dell'unità C.


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, "msxml://C:\MyStore.xml"

'  Create an application object in the store.
Dim expenseApp
Set expenseApp= AzManStore.OpenApplication("Expense")

'  Create an application group object.
Dim appGroup
Set appGroup = expenseApp.CreateApplicationGroup("LDAP Trusted Users")

'  Set the Type property of the group to two
'  (AZ_GROUPTYPE_LDAP_QUERY).
appGroup.Type = 2

'  Add LDAP query for all users.
appGroup.LdapQuery = ("&(objectCategory=person)(objectClass=user)")

'  Save the application group to the store.
appGroup.Submit

```



 

 
