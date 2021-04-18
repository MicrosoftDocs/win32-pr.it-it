---
title: Delega di unità organizzative
description: La società Fabrikam ingaggia due amministratori, Mike e Paul, per gestire rispettivamente le unità organizzative East e West.
ms.assetid: ecf71ae6-9b6f-4e3c-878a-2c6fd193da33
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9928884c8be19f9668d6f81ed9462f6fb757286f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297689"
---
# <a name="delegating-organizational-units"></a>Delega di unità organizzative

La società Fabrikam ingaggia due amministratori, Mike e Paul, per gestire rispettivamente le unità organizzative East e West. Davide delega le sue responsabilità amministrative in modo che possano creare ed eliminare gli utenti nelle rispettive unità organizzative.

Prima di vedere come configurare queste unità organizzative in Mike e Paul, è necessario comprendere come configurare l'accesso agli oggetti in Active Directory. Ogni oggetto in Active Directory dispone di un descrittore di sicurezza. Con il descrittore di sicurezza è possibile modificare le autorizzazioni per l'oggetto, propagare le autorizzazioni, abilitare il controllo e così via. Il descrittore di sicurezza dispone di due elenchi di controllo di accesso (ACL): un ACL discrezionale (DACL) e un ACL di sistema (SACL). Ogni ACL può contenere voci di controllo di accesso (ACE). Con una voce ACE è possibile impostare l'accesso consentito o negato per un oggetto. Inoltre, è possibile specificare azioni specifiche da concedere o negare. Esempi di azioni includono Create Child, Delete Child, Read Property e Write Property. Questi diritti vengono specificati con [**accessMask**](iadsaccesscontrolentry-property-methods.md).

Successivamente, è possibile specificare le classi o gli attributi a cui è associata questa voce ACE. Nell'esempio di Fabrikam che segue, Davide sceglie la classe utente in modo che ogni amministratore possa aggiungere utenti al sistema. Successivamente, è necessario rispondere alla domanda: "chi sarà il beneficiario di questo ACE?" Joe specificherà Mike.

Infine, è possibile impostare il comportamento di ereditarietà ACE, ad esempio è possibile specificare ACE per propagare la gerarchia. In breve, l'esempio precedente comporterà la creazione ed eliminazione di oggetti utente nell'unità organizzativa Sales East.

Joe usa l'esempio di codice seguente per configurare le voci ACE e ACL nell'unità organizzativa East.


```VB
Set ou = GetObject("LDAP://OU=East, OU=Sales, DC=Fabrikam,DC=COM")
Set sec = ou.Get("ntSecurityDescriptor")
Set acl = sec.DiscretionaryAcl

Set ace = CreateObject("AccessControlEntry") 
' You can also use Set ace = new ADsAccessControlEntry.

' Grant access to the object.
ace.AceType = ADS_ACETYPE_ACCESS_ALLOWED_OBJECT 

' Create and delete child objects.
ace.AccessMask = ADS_RIGHT_DS_CREATE_CHILD Or ADS_RIGHT_DS_DELETE_CHILD 
' Create the user object with the user schema IDGUID.
ace.ObjectType = "{BF967ABA-0DE6-11D0-A285-00AA003049E2}" 
' Propagate the ACE down.  
ace.AceFlags = ADS_ACEFLAG_INHERIT_ACE
' Provide an option that notifies that the objectType is filled.
ace.Flags = ADS_FLAG_OBJECT_TYPE_PRESENT 
' Show the beneficiary of this ACE.
ace.Trustee = "FABRIKAM\Mike" 
acl.AddAce ace

sec.DiscretionaryAcl = acl
ou.Put "ntSecurityDescriptor", Array(sec)
' Use SetInfo to commit the data to Active Directory.
ou.SetInfo 

' Release the objects.
Set ace = Nothing
Set acl  = Nothing
Set sec = Nothing
```



Nella figura seguente viene illustrato il menu Active Directory **Crea nuovo visualizzazione** dopo l'esecuzione del codice. Quando Joe, l'amministratore, accede, vede diverse classi che è possibile creare. Tuttavia, quando Mike si connette, può solo creare oggetti utente.

![menu di opzione Crea nuova vista](images/adadsi5.png)

Per altre informazioni, vedere [modello di sicurezza ADSI](adsi-security-model.md).

 

 




