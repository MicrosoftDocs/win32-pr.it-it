---
title: Creazione di un'unità organizzativa
description: Ora che si dispone dell'oggetto dominio, è possibile iniziare a creare unità organizzative.
ms.assetid: c9955b44-5ca1-4b4b-85c8-e0d55a4304ca
ms.tgt_platform: multiple
keywords:
- Creazione di un'unità organizzativa ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78ec0da1efe78d54eba8bc0dc05a998717aaf91f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955105"
---
# <a name="creating-an-organizational-unit"></a>Creazione di un'unità organizzativa

Ora che si dispone dell'oggetto dominio, è possibile iniziare a creare unità organizzative. Fabrikam è costituito da due divisioni: vendite e produzione. La società sta pianificando di assumere due amministratori di Windows 2000 per gestire ogni divisione. Joe worden, come amministratore dell'organizzazione, creerà due nuove unità organizzative nel dominio fabrikam. Grazie alla creazione di un'unità organizzativa, Joe può raggruppare più oggetti e consentire a un altro utente di gestire questi oggetti. Nell'esempio di codice seguente viene creata l'unità organizzativa Sales (OU).


```VB
Dim dom as IADsContainer
Set dom = GetObject("LDAP://DC=Fabrikam,DC=Com")
Set salesOrg = dom.Create("organizationalUnit", "OU=Sales")
salesOrg.Put "description", "Sales Headquarter,SF"
salesOrg.Put "wwwHomePage", "https://fabrikam.com/sales"
salesOrg.SetInfo
```



Il metodo [**IADsContainer. Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) accetta il nome della classe e il nome del nuovo oggetto. A questo punto non viene eseguito il commit dell'oggetto per Active Directory. Tuttavia, nel client sarà presente un riferimento a un oggetto ADSI/COM. Con questo oggetto ADSI è possibile impostare o modificare gli attributi usando il metodo [**IADs. Put**](/windows/desktop/api/Iads/nf-iads-iads-put) . Il metodo **IADs. Put** accetta il nome dell'attributo e il valore dell'attributo. Tuttavia, non viene eseguito il commit di alcun elemento nella directory; tutto viene memorizzato nella cache del client. Quando si chiama il metodo [**IADs. SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) , viene eseguito il commit delle modifiche, in questo caso la creazione di oggetti e la modifica degli attributi, nella directory. Queste modifiche sono transazionali, pertanto verrà visualizzato il nuovo oggetto con tutti gli attributi impostati o nessun oggetto.

È anche possibile annidare unità organizzative. Nell'esempio di codice seguente si presuppone che la divisione Sales venga divisa ulteriormente nelle aree East e West.


```VB
Set east = salesOrg.Create("organizationalUnit", "OU=East")
east.SetInfo
```



Questo vale anche per l'area ovest.

Per eseguire il binding direttamente all'area est nell'organizzazione vendite, specificare il nome distinto.


```VB
Set east = GetObject("LDAP://OU=East,OU=Sales,DC=Fabrikam,DC=COM")
Debug.Print east.Get "description"
east.Put "wwwHomePage", "https://fabrikam.com/sales/east"
```



Se è già stato associato all'oggetto padre (Sales), è possibile eseguire l'associazione all'oggetto figlio (East) dall'oggetto padre utilizzando il nome relativo dell'oggetto figlio.


```VB
Set east = salesOU.GetObject("organizationalUnit", "OU=East")
```



Per assicurarsi che gli oggetti siano stati creati, utilizzare lo snap-in MMC utenti e computer Active Directory per visualizzare le nuove unità organizzative.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Trasferimento di utenti esistenti all'unità organizzativa](moving-existing-users-to-the-organizational-unit.md)
</dt> </dl>

 

 




