---
title: Trasferimento di utenti esistenti all'unità organizzativa
description: Quando l'amministratore dell'organizzazione, Joe worden, aggiorna il dominio di Windows NT 4,0 per Active Directory, viene eseguita la migrazione di tutti gli utenti e gruppi ai contenitori di utenti nel dominio fabrikam.
ms.assetid: 230a594f-70c2-4ab6-a7e8-d5a77f2d6dd1
ms.tgt_platform: multiple
keywords:
- Trasferimento di utenti esistenti all'unità organizzativa AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 535ff7110eaf956f108854e8442faa7386667346
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104220911"
---
# <a name="moving-existing-users-to-the-organizational-unit"></a>Trasferimento di utenti esistenti all'unità organizzativa

Quando l'amministratore dell'organizzazione, Joe worden, aggiorna il dominio di Windows NT 4,0 per Active Directory, viene eseguita la migrazione di tutti gli utenti e gruppi ai contenitori di utenti nel dominio fabrikam. Joe può ora spostare tali utenti e gruppi nelle unità organizzative appropriate. Un oggetto può anche essere spostato tra domini Windows 2000 correlati tramite ADSI.

Nell'esempio di codice seguente Joe sposta "SergioMelchiori" nell'organizzazione delle vendite.


```VB
Set usr = salesOU.MoveHere("LDAP://CN=jeffsmith,CN=Users,DC=fabrikam,DC=com", vbNullString)
```



Il metodo [**IADsContainer. MoveHere**](/windows/desktop/api/Iads/nf-iads-iadscontainer-movehere) accetta il ADsPath dell'oggetto da spostare e il nuovo nome di oggetto (RDN). Per avere lo stesso nome, è possibile specificare **null** (**vbNullString**) per il parametro *bstrNewName* . Per rinominare l'oggetto quando viene spostato, specificare il nuovo nome distinto relativo per il parametro *bstrNewName* . Ad esempio, per spostare SergioMelchiori nell'organizzazione vendite e rinominare l'oggetto "SergioMelchiori" in "Jeff \_ Smith" nella stessa operazione, Joe eseguirà il codice seguente:


```VB
Set usr = salesOU.MoveHere("LDAP://CN=jeffsmith,CN=Users,DC=Fabrikam,DC=com", "CN=jeff_smith")
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di nuovi utenti nell'unità organizzativa](creating-new-users-in-the-organizational-unit.md)
</dt> </dl>

 

 




