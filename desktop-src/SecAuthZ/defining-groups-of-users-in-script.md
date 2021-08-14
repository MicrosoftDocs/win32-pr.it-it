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
ms.openlocfilehash: 6198d31a53dbd7d30100a8df56536cf0336c9c1e7ca5b78ad4e9e73e40da13cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118913987"
---
# <a name="defining-groups-of-users-in-script"></a>Definizione di gruppi di utenti nello script

In Gestione autorizzazioni un [**oggetto IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) rappresenta un gruppo di utenti. I ruoli possono quindi essere assegnati a questo gruppo di utenti collettivamente. Un **oggetto IAzApplicationGroup** può includere anche altri **oggetti IAzApplicationGroup** come membri. Per altre informazioni sui gruppi di applicazioni, vedere [Utenti e gruppi](users-and-groups.md).

Un gruppo può essere definito da elenchi espliciti di membri e non membri o da una query [*Lightweight Directory Access Protocol*](/windows/desktop/SecGloss/l-gly) (LDAP). Gli esempi seguenti illustrano come creare ogni tipo di gruppo di applicazioni:

-   [Creazione di un gruppo di base](#creating-a-basic-group)
-   [Creazione di un gruppo di query LDAP](#creating-an-ldap-query-group)

## <a name="creating-a-basic-group"></a>Creazione di un gruppo di base

Un gruppo di applicazioni di base viene definito dai membri inclusi nelle proprietà [**Members**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_members) e [**NonMembers**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_nonmembers) dell'oggetto [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) che rappresenta il gruppo. Gli utenti e i gruppi elencati nella proprietà **Members** sono inclusi nel gruppo di applicazioni e gli utenti e i gruppi elencati nella proprietà **NonMembers** vengono esclusi dal gruppo di applicazioni. L'elenco **nella proprietà NonMembers** sostituisce l'elenco nella **proprietà** Members.

L'esempio seguente illustra come creare un gruppo di applicazioni di base e aggiungere tutti gli utenti locali come membri di tale gruppo. L'esempio presuppone che sia presente un archivio criteri XML esistente denominato MyStore.xml nella directory radice dell'unità C.


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

Un gruppo di query LDAP ha un'appartenenza definita dalla query contenuta nel valore della relativa [**proprietà LdapQuery.**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_ldapquery)

L'esempio seguente illustra come creare un gruppo di applicazioni di query LDAP e aggiungere tutti gli utenti come membri di tale gruppo. L'esempio presuppone che sia presente un archivio criteri XML esistente denominato MyStore.xml nella directory radice dell'unità C.


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



 

 
