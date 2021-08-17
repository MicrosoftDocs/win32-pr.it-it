---
title: Associazione a oggetti Active Directory
description: Prima di continuare con questo scenario, è necessario comprendere come vengono denominati gli oggetti ADSI in Active Directory e come associarli. L'associazione di un oggetto ADSI connette l'oggetto al servizio directory e consente di accedere ai metodi dell'oggetto.
ms.assetid: 0d8d8f1c-786f-4d87-977c-91a167bcf118
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0b473c9e3370c3d1739fc904b8c6409d756f62b5c358db200c3de821f55349f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962260"
---
# <a name="binding-to-active-directory-objects"></a>Associazione a oggetti Active Directory

Prima di continuare con questo scenario, è necessario comprendere come vengono denominati gli oggetti ADSI in Active Directory e come associarli. L'associazione di un oggetto ADSI connette l'oggetto al servizio directory e consente di accedere ai metodi dell'oggetto.

## <a name="adspath"></a>ADsPath

Un oggetto ADSI viene identificato in modo univoco dalla relativa stringa di associazione, detta anche ADsPath. ADsPath è una combinazione di un identificatore programmatico (progID) del provider ADSI e del nome distinto (DN) dell'oggetto.

Ecco il formato di ADsPath:

"progID://DN"

-   pogID: identificatore a livello di codice del provider ADSI, ad esempio LDAP o WinNT.

-   :// : separa il progID dal DN.

-   DN: nome distinto dell'oggetto ADSI, ovvero il percorso completo dell'oggetto, in cui il percorso è costituito da nomi distinti relativi (RDN).

Un RDN è il nome dell'oggetto senza il percorso ed è univoco dai relativi oggetti di pari livello. Un RDN è costituito da un ID attributo e un valore, ad esempio "DC=Fabrikam", dove DC è l'attributo e Fabrikam è il valore. DC è un ID attributo RDN che sta per componente di dominio.

Ecco un esempio di ADsPath:

"LDAP://DC=Fabrikam,DC=Com"

## <a name="binding-the-object"></a>Associazione dell'oggetto

Ecco come associare l'oggetto dominio in questo scenario:


```VB
Set dom = GetObject("LDAP://DC=Fabrikam,DC=Com")
```



Quando si esegue questo esempio di codice, ADSI usa il DN per determinare gli oggetti ADSI da associare. Dopo che ADSI ha associato questi oggetti, è possibile accedere ai relativi metodi. L'esempio di codice precedente associa un oggetto dominio a [**IAD**](/windows/desktop/api/Iads/nn-iads-iads) [**e IADsContainer.**](/windows/desktop/api/Iads/nn-iads-iadscontainer) È ora possibile usare metodi su tali interfacce, ad esempio [**Get,**](/windows/desktop/api/Iads/nf-iads-iads-get) [**Put,**](/windows/desktop/api/Iads/nf-iads-iads-put) [**Create,**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) [**Delete**](/windows/desktop/api/Iads/nf-iads-iadscontainer-delete)e [**MoveHere.**](/windows/desktop/api/Iads/nf-iads-iadscontainer-movehere)

Dopo aver associato un oggetto di dominio, è possibile stamparne alcuni attributi:


```VB
Debug.Print dom.Get("Name")
Debug.Print dom.Get("whenCreated")
```



Per altre informazioni su ADsPath, vedere [Stringa di associazione.](binding-string.md) Per altre informazioni sull'associazione, vedere [Associazione a un oggetto ADSI.](binding-to-an-adsi-object.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di un'unità organizzativa](creating-an-organizational-unit.md)
</dt> </dl>

 

 




