---
description: È possibile utilizzare l'elenco DACL di un oggetto contenitore per controllare gli utenti autorizzati a creare oggetti figlio all'interno del contenitore.
ms.assetid: 95f2f058-f847-4f58-b469-090bf599ae98
title: Controllo della creazione di oggetti figlio in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 598b2fd9a9889fbb77d2b3a4ecd004efcd823b8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527637"
---
# <a name="controlling-child-object-creation-in-c"></a>Controllo della creazione di oggetti figlio in C++

È possibile utilizzare l'elenco DACL di un oggetto contenitore per controllare gli utenti autorizzati a creare oggetti figlio all'interno del contenitore. Questo può essere importante perché il creatore di un oggetto viene in genere assegnato come proprietario dell'oggetto e il proprietario di un oggetto può controllare l'accesso all'oggetto.

I vari tipi di oggetti contenitore hanno diritti di accesso specifici che controllano la possibilità di creare oggetti figlio. Un thread, ad esempio, deve avere \_ \_ l'accesso key create Sub \_ Key a una chiave del registro di sistema per creare una sottochiave sotto la chiave. L'elenco DACL di una chiave del registro di sistema può contenere voci ACE che consentono o negano il diritto di accesso. Analogamente, NTFS supporta il file \_ Add \_ FILE e file \_ Add \_ sottodirectory diritti di accesso per controllare la possibilità di creare file o directory in una directory.

La \_ \_ \_ \_ creazione di un diritto di accesso figlio per gli annunci di dominio destro consente di controllare la creazione di oggetti figlio in un oggetto servizio directory (DS). Tuttavia, gli oggetti DS possono contenere tipi diversi di oggetti, in modo che il sistema supporti una maggiore granularità del controllo. È possibile utilizzare le [voci ACE specifiche dell'oggetto](object-specific-aces.md) per consentire o negare il diritto di creare un tipo specificato di oggetto figlio. È possibile consentire a un utente di creare un tipo di oggetto figlio evitando all'utente di creare altri tipi di oggetti figlio.

Nell'esempio seguente viene usata la funzione [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) per aggiungere una voce ACE specifica dell'oggetto a un ACL. La voce ACE concede l'autorizzazione per creare un tipo specificato di oggetto figlio. Il membro **grfAccessPermissions** della struttura [**di \_ accesso esplicita**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) è impostato su Ads \_ Rights \_ DS \_ Create \_ child per indicare che la voce ACE controlla la creazione dell'oggetto figlio. Il membro **ObjectsPresent** della struttura [**Objects \_ e \_ SID**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_sid) è impostato sul \_ tipo di oggetto ACE \_ \_ presente per indicare che il membro **ObjectTypeGuid** contiene un GUID valido. Il GUID identifica un tipo di oggetto figlio la cui creazione viene controllata.

Nell'esempio seguente, pOldDACL deve essere un puntatore valido a una struttura [**ACL**](/windows/desktop/api/Winnt/ns-winnt-acl) esistente. Per informazioni su come creare una struttura **ACL** per un oggetto, vedere [creazione di un descrittore di sicurezza per un nuovo oggetto in C++](creating-a-security-descriptor-for-a-new-object-in-c--.md).


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



 

 



