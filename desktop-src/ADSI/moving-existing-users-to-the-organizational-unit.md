---
title: Spostamento di utenti esistenti nell'unità organizzativa
description: Quando l'amministratore dell'organizzazione, Joe Worden, aggiorna il dominio Windows NT 4.0 ad Active Directory, viene eseguita la migrazione di tutti gli utenti e i gruppi ai contenitori Users nel dominio Fabrikam.
ms.assetid: 230a594f-70c2-4ab6-a7e8-d5a77f2d6dd1
ms.tgt_platform: multiple
keywords:
- Spostamento di utenti esistenti nell'unità organizzativa AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d26104feb5d4c8b6a1f24176ce23fcbb6ef6a965ca29c58887f02724b3ccba8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118178955"
---
# <a name="moving-existing-users-to-the-organizational-unit"></a>Spostamento di utenti esistenti nell'unità organizzativa

Quando l'amministratore dell'organizzazione, Joe Worden, aggiorna il dominio Windows NT 4.0 ad Active Directory, viene eseguita la migrazione di tutti gli utenti e i gruppi ai contenitori Users nel dominio Fabrikam. Joe può ora spostare gli utenti e i gruppi nelle unità organizzative appropriate. Un oggetto può anche essere spostato tra domini Windows 2000 usando ADSI.

Nell'esempio di codice seguente Joe sposta "jeffsmith" nell'organizzazione Sales.


```VB
Set usr = salesOU.MoveHere("LDAP://CN=jeffsmith,CN=Users,DC=fabrikam,DC=com", vbNullString)
```



Il [**metodo IADsContainer.MoveHere**](/windows/desktop/api/Iads/nf-iads-iadscontainer-movehere) accetta il valore ADsPath dell'oggetto da spostare e il nuovo nome dell'oggetto (RDN). Per mantenere lo stesso nome, è possibile specificare **NULL** (**vbNullString**) per il *parametro bstrNewName.* Per rinominare l'oggetto quando viene spostato, specificare il nuovo nome distinto relativo per il *parametro bstrNewName.* Ad esempio, per spostare jeffsmith nell'organizzazione di vendita e rinominare l'oggetto "jeffsmith" in "jeff smith" nella stessa operazione, Joe eseguirà \_ il codice seguente:


```VB
Set usr = salesOU.MoveHere("LDAP://CN=jeffsmith,CN=Users,DC=Fabrikam,DC=com", "CN=jeff_smith")
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di nuovi utenti nell'unità organizzativa](creating-new-users-in-the-organizational-unit.md)
</dt> </dl>

 

 




