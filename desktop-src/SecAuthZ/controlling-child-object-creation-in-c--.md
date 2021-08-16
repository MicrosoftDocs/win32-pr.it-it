---
description: È possibile usare l'elenco DACL di un oggetto contenitore per controllare chi può creare oggetti figlio all'interno del contenitore.
ms.assetid: 95f2f058-f847-4f58-b469-090bf599ae98
title: Controllo della creazione di oggetti figlio in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2820f6d1bd9aae335e018e15b3b298b5b907f51a47d78e517b8ad798d0aba442
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117782716"
---
# <a name="controlling-child-object-creation-in-c"></a>Controllo della creazione di oggetti figlio in C++

È possibile usare l'elenco DACL di un oggetto contenitore per controllare chi può creare oggetti figlio all'interno del contenitore. Questo può essere importante perché l'autore di un oggetto viene in genere assegnato come proprietario dell'oggetto e il proprietario di un oggetto può controllare l'accesso all'oggetto.

I vari tipi di oggetti contenitore hanno diritti di accesso specifici che controllano la possibilità di creare oggetti figlio. Ad esempio, un thread deve disporre dell'accesso KEY CREATE SUB KEY a una chiave del Registro di sistema \_ \_ per creare una \_ sottochiave nella chiave . L'elenco DACL di una chiave del Registro di sistema può contenere voci ACE che consentono o negano questo diritto di accesso. Analogamente, NTFS supporta i diritti di accesso FILE ADD FILE e FILE ADD SUBDIRECTORY per controllare la possibilità di creare \_ file o directory in una \_ \_ \_ directory.

Il diritto di accesso ADS RIGHT DS CREATE CHILD controlla la creazione di oggetti figlio in un oggetto del \_ \_ servizio \_ \_ directory. Tuttavia, gli oggetti DS possono contenere tipi diversi di oggetti, quindi il sistema supporta una granularità di controllo più fine. È possibile usare [ACE specifiche dell'oggetto](object-specific-aces.md) per consentire o negare il diritto di creare un tipo specificato di oggetto figlio. È possibile consentire a un utente di creare un tipo di oggetto figlio impedendo all'utente di creare altri tipi di oggetti figlio.

Nell'esempio seguente viene utilizzata [**la funzione SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) per aggiungere una voce ACE specifica dell'oggetto a un elenco di controllo di accesso. La ACE concede l'autorizzazione per creare un tipo specificato di oggetto figlio. Il **membro grfAccessPermissions** della struttura [**EXPLICIT \_ ACCESS**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) è impostato su ADS RIGHT DS CREATE CHILD per indicare che la ACE controlla la \_ creazione \_ \_ \_ dell'oggetto figlio. Il **membro ObjectsPresent** della struttura [**OBJECTS AND \_ \_ SID**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_sid) è impostato su ACE OBJECT TYPE PRESENT per indicare che il membro \_ \_ \_ **ObjectTypeGuid** contiene un GUID valido. Il GUID identifica un tipo di oggetto figlio di cui viene controllata la creazione.

Nell'esempio seguente pOldDACL deve essere un puntatore valido a una struttura [**ACL**](/windows/desktop/api/Winnt/ns-winnt-acl) esistente. Per informazioni su come creare una struttura **ACL** per un oggetto, vedere Creazione di un descrittore di sicurezza per [un nuovo oggetto in C++.](creating-a-security-descriptor-for-a-new-object-in-c--.md)


```C++
DWORD dwRes;
PACL pOldDACL = NULL;
PACL pNewDACL = NULL;
GUID guidChildObjectType = GUID_NULL;   // GUID of object to control creation of
PSID pTrusteeSID = NULL;           // trustee for new ACE
EXPLICIT_ACCESS ea;
OBJECTS_AND_SID ObjectsAndSID;

// pOldDACL must be a valid pointer to an existing ACL structure.

// guidChildObjectType must be the GUID of an object type 
// that is a possible child of the object associated with pOldDACL.
 
// Initialize an OBJECTS_AND_SID structure with object type GUIDs and 
// the SID of the trustee for the new ACE. 

ZeroMemory(&ObjectsAndSID, sizeof(OBJECTS_AND_SID));
ObjectsAndSID.ObjectsPresent = ACE_OBJECT_TYPE_PRESENT;
ObjectsAndSID.ObjectTypeGuid = guidChildObjectType;
ObjectsAndSID.InheritedObjectTypeGuid  = GUID_NULL;
ObjectsAndSID.pSid = (SID *)pTrusteeSID;

// Initialize an EXPLICIT_ACCESS structure for the new ACE. 

ZeroMemory(&ea, sizeof(EXPLICIT_ACCESS));
ea.grfAccessPermissions = ADS_RIGHT_DS_CREATE_CHILD;
ea.grfAccessMode = GRANT_ACCESS;
ea.grfInheritance= NO_INHERITANCE;
ea.Trustee.TrusteeForm = TRUSTEE_IS_OBJECTS_AND_SID;
ea.Trustee.ptstrName = (LPTSTR) &ObjectsAndSID;

// Create a new ACL that merges the new ACE
// into the existing DACL.

dwRes = SetEntriesInAcl(1, &ea, pOldDACL, &pNewDACL);
```



 

 



