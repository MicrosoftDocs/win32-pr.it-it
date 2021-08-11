---
title: Creazione di nuovi utenti nell'unità organizzativa
description: Adam Adams è stato assunto nell'organizzazione Fabrikam Sales. Il suo report diretto è Patrick Hines.
ms.assetid: bc31ed04-e505-4d64-9fa3-d06af7351db0
ms.tgt_platform: multiple
keywords:
- Creazione di nuovi utenti nell'unità organizzativa ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b76d62c8d95e7d5e421fc562e38716477ff2dfb8f4097d4652710e2c50715487
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118180116"
---
# <a name="creating-new-users-in-the-organizational-unit"></a>Creazione di nuovi utenti nell'unità organizzativa

Adam Adams è stato assunto nell'organizzazione Fabrikam Sales. Il suo report diretto è Patrick Hines.

Come illustrato nell'esempio di codice seguente, Joe Andreshak, l'amministratore dell'organizzazione, creerà un nuovo account per lui.


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



Quando si crea un nuovo utente, è necessario specificare **sAMAccountName.** Si tratta di un attributo obbligatorio per la classe utente. Prima di poter creare un'istanza di un oggetto, è necessario impostare tutti gli attributi obbligatori. **SAMAccountName verrà** generato automaticamente se non ne viene specificato uno per un nuovo utente.

Quando si crea un nuovo utente, tutti gli attributi necessari devono essere impostati nella cache locale prima di chiamare il metodo [**IADs.SetInfo.**](/windows/desktop/api/Iads/nf-iads-iads-setinfo)

Joe, come amministratore, può assegnare la password di Luca usando il [**metodo IADsUser.SetPassword.**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) Il **metodo IADsUser.SetPassword** non funzionerà fino a quando non viene chiamato il metodo [**IADs.SetInfo.**](/windows/desktop/api/Iads/nf-iads-iads-setinfo)

Joe abilita quindi l'account utente impostando la [**proprietà IADsUser.AccountDisabled**](iadsuser-property-methods.md) su **FALSE.**

Nell'esempio di codice seguente viene illustrato come impostare Patrick come manager di Patrick.


```VB
Set usr = GetObject("LDAP://CN=patrickhines,OU=Sales,DC=Fabrikam,DC=COM")
usr.Put "manager", "CN=Terry Adams,OU=Sales,DC=Fabrikam,DC=COM"
usr.SetInfo
```



Ci si potrebbe chiedere cosa accade se Il cardinale cambia nome, si sposta in un'organizzazione diversa o lascia l'azienda. Who gestisce questo collegamento al report diretto dal responsabile? Per altre informazioni e la soluzione a questo problema, vedere [Riorganizzazione.](reorganization.md) Poiché lo schema di Active Directory è estendibile, è possibile modellare gli oggetti in modo da includere relazioni simili in stile di report con gestione diretta.

Prima di procedere con l'attività successiva, esaminare un esempio di codice che illustra come Joe visualizza i report diretti di Luca.


```VB
Set usr = GetObject("LDAP://CN=Terry Adams,OU=Sales,DC=Fabrikam,DC=COM")
reports = usr.GetEx ("directReports")

For each directReport in reports
    Debug.Print directReport
Next
```



In questo esempio di codice Patrick verrà visualizzato come report diretto di Patrick, anche se **l'attributo directReports** non è mai stato modificato. Active Directory esegue questa operazione automaticamente.

Nel mondo della directory, un attributo può avere uno o più valori. Poiché **directReports** ha più valori, è possibile ottenere queste informazioni esaminando lo schema, è più semplice usare il metodo [**IADs.GetEx,**](/windows/desktop/api/Iads/nf-iads-iads-getex) che restituisce una matrice di valori indipendentemente dal fatto che vengono restituiti valori singoli o multipli.

Lo Utenti e computer di Active Directory snap-in consente di visualizzare i report diretti e le relazioni di gestione nella pagina delle proprietà dell'utente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Aggiunta di utenti a un gruppo](adding-users-to-a-group.md)
</dt> </dl>

 

 




