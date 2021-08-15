---
title: Creazione di un'unità organizzativa
description: Dopo aver creato l'oggetto dominio, è possibile iniziare a creare unità organizzative.
ms.assetid: c9955b44-5ca1-4b4b-85c8-e0d55a4304ca
ms.tgt_platform: multiple
keywords:
- Creazione di un'unità organizzativa ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf2db91c02836e2425cd25e72afe6e57ff6619948372a20d03079d65eee5c882
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118961990"
---
# <a name="creating-an-organizational-unit"></a>Creazione di un'unità organizzativa

Dopo aver creato l'oggetto dominio, è possibile iniziare a creare unità organizzative. Fabrikam ha due divisioni: Vendite e Produzione. L'azienda prevede di assumere due Windows 2000 amministratori per gestire ogni divisione. Joe Worden, come amministratore dell'organizzazione, creerà due nuove unità organizzative nel dominio Fabrikam. Creando un'unità organizzativa, Joe può raggruppare più oggetti e consentire a un altro utente di gestire questi oggetti. L'esempio di codice seguente crea l'unità organizzativa Sales (OU).


```VB
Dim dom as IADsContainer
Set dom = GetObject("LDAP://DC=Fabrikam,DC=Com")
Set salesOrg = dom.Create("organizationalUnit", "OU=Sales")
salesOrg.Put "description", "Sales Headquarter,SF"
salesOrg.Put "wwwHomePage", "https://fabrikam.com/sales"
salesOrg.SetInfo
```



Il [**metodo IADsContainer.Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) accetta il nome della classe e il nome del nuovo oggetto. A questo punto non viene eseguito il commit dell'oggetto in Active Directory. Tuttavia, si avrà un riferimento a un oggetto ADSI/COM nel client. Con questo oggetto ADSI è possibile impostare o modificare gli attributi usando il [**metodo IADs.Put.**](/windows/desktop/api/Iads/nf-iads-iads-put) Il **metodo IADs.Put** accetta il nome dell'attributo e il valore dell'attributo. Tuttavia, non viene eseguito il commit di alcun oggetto nella directory. tutti gli elementi vengono memorizzati nella cache del client. Quando si chiama il [**metodo IADs.SetInfo,**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) viene eseguito il commit delle modifiche, in questo caso la creazione di oggetti e la modifica degli attributi, nella directory. Queste modifiche vengono transazionate, ovvero verrà visualizzato il nuovo oggetto con tutti gli attributi impostati o nessun oggetto.

È anche possibile annidare le unità organizzative. Nell'esempio di codice seguente si presuppone che la divisione Sales sia suddivisa ulteriormente nelle aree East e West.


```VB
Set east = salesOrg.Create("organizationalUnit", "OU=East")
east.SetInfo
```



Questo vale anche per l'area Occidentale.

Per eseguire l'associazione direttamente all'area Orientale nell'organizzazione Sales, specificare il nome distinto.


```VB
Set east = GetObject("LDAP://OU=East,OU=Sales,DC=Fabrikam,DC=COM")
Debug.Print east.Get "description"
east.Put "wwwHomePage", "https://fabrikam.com/sales/east"
```



Se è già stato associato all'oggetto padre (Sales), è possibile eseguire l'associazione all'oggetto figlio (East) dall'oggetto padre usando il nome relativo dell'oggetto figlio.


```VB
Set east = salesOU.GetObject("organizationalUnit", "OU=East")
```



Per assicurarsi che gli oggetti siano stati creati, utilizzare lo snap-in MMC Utenti e computer di Active Directory per visualizzare le nuove unità organizzative.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Spostamento di utenti esistenti nell'unità organizzativa](moving-existing-users-to-the-organizational-unit.md)
</dt> </dl>

 

 




