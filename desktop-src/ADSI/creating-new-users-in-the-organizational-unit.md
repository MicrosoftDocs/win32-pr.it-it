---
title: Creazione di nuovi utenti nell'unità organizzativa
description: Terry Adams è stato assunto nell'organizzazione vendite di Fabrikam. Il suo report diretto è Patrick Hines.
ms.assetid: bc31ed04-e505-4d64-9fa3-d06af7351db0
ms.tgt_platform: multiple
keywords:
- Creazione di nuovi utenti nell'unità organizzativa ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c45f9dc91f1c36493a4ae8e1c9bb1a69268c9987
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104470806"
---
# <a name="creating-new-users-in-the-organizational-unit"></a>Creazione di nuovi utenti nell'unità organizzativa

Terry Adams è stato assunto nell'organizzazione vendite di Fabrikam. Il suo report diretto è Patrick Hines.

Come illustrato nell'esempio di codice seguente, Joe Andreani, l'amministratore dell'organizzazione, creerà un nuovo account per l'utente.


```VB
Dim salesOU as IADsContainer
Set salesOU = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=COM")
Set usr = salesOU.Create("user", "CN=Terry Adams")
usr.Put "sAMAccountName", "terryadams"
usr.Put "userPrincipalName", "terryadams@fabrikam.com" 
usr.Put "title" "Marketing Manager"
usr.SetInfo

usr.SetPassword "seahorse"
usr.AccountDisabled = False
usr.SetInfo
```



Quando si crea un nuovo utente, è necessario specificare un **sAMAccountName**. Si tratta di un attributo obbligatorio per la classe utente. Prima di poter creare un'istanza di un oggetto, è necessario impostare tutti gli attributi obbligatori. Il **sAMAccountName** verrà generato automaticamente se non ne viene specificato uno per un nuovo utente.

Quando si crea un nuovo utente, è necessario impostare tutti gli attributi necessari nella cache locale prima di chiamare il metodo [**IADs. seinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) .

Joe, in qualità di amministratore, può assegnare la password di Terry usando il metodo [**IADsUser. sepassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) . Il metodo **IADsUser. sepassword** non funzionerà fino a quando non viene chiamato il metodo [**IADs. seinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) .

Joe Abilita quindi l'account utente impostando la proprietà [**IADsUser. accountdisabled**](iadsuser-property-methods.md) su **false**.

Nell'esempio di codice seguente viene illustrato come impostare Terry come responsabile di Patrick.


```VB
Set usr = GetObject("LDAP://CN=patrickhines,OU=Sales,DC=Fabrikam,DC=COM")
usr.Put "manager", "CN=Terry Adams,OU=Sales,DC=Fabrikam,DC=COM"
usr.SetInfo
```



Ci si potrebbe chiedere cosa accade se Terry cambia il proprio nome, si sposta in un'altra organizzazione o lascia l'azienda. Chi gestisce il collegamento diretto al report? Per ulteriori informazioni e per risolvere il problema, vedere [riorganizzazione](reorganization.md). Poiché lo schema di Active Directory è estendibile, è possibile modellare gli oggetti in modo da includere relazioni di stile del rapporto dirette da gestione analoghe.

Prima di passare all'attività successiva, esaminare un esempio di codice che Mostra come Joe visualizzerà i dipendenti diretti di Terry.


```VB
Set usr = GetObject("LDAP://CN=Terry Adams,OU=Sales,DC=Fabrikam,DC=COM")
reports = usr.GetEx ("directReports")

For each directReport in reports
    Debug.Print directReport
Next
```



In questo esempio di codice Patrick verrà visualizzato come report diretto di Terry, anche se l'attributo **DirectReports** non è mai stato modificato. Questa operazione viene eseguita automaticamente Active Directory.

Nel mondo della directory, un attributo può avere uno o più valori. Poiché **DirectReports** ha più valori, è possibile ottenere queste informazioni esaminando lo schema, è più semplice usare il metodo [**IADs. GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) , che restituisce una matrice di valori, indipendentemente dal fatto che vengano restituiti valori singoli o multipli.

Lo snap-in Active Directory utenti e computer consente di visualizzare i report diretti e le relazioni di gestione nella pagina delle proprietà dell'utente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Aggiunta di utenti a un gruppo](adding-users-to-a-group.md)
</dt> </dl>

 

 




