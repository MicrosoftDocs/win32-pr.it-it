---
title: Associazione a oggetti Active Directory
description: Prima di continuare con questo scenario, è necessario comprendere in che modo gli oggetti ADSI vengono denominati in Active Directory e come associarli. Il binding di un oggetto ADSI connette l'oggetto al servizio directory e consente di accedere ai metodi dell'oggetto.
ms.assetid: 0d8d8f1c-786f-4d87-977c-91a167bcf118
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fa54f2015e0d5663db2917eb27b250f39eb4c0c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044073"
---
# <a name="binding-to-active-directory-objects"></a>Associazione a oggetti Active Directory

Prima di continuare con questo scenario, è necessario comprendere in che modo gli oggetti ADSI vengono denominati in Active Directory e come associarli. Il binding di un oggetto ADSI connette l'oggetto al servizio directory e consente di accedere ai metodi dell'oggetto.

## <a name="adspath"></a>ADsPath

Un oggetto ADSI viene identificato in modo univoco dalla relativa stringa di associazione, definita anche ADsPath. Un ADsPath è una combinazione di un identificatore a livello di codice (progID) del provider ADSI e del nome distinto (DN) dell'oggetto.

Ecco il formato di un ADsPath:

"progID://DN"

-   pogID: identificatore a livello di codice del provider ADSI, ad esempio LDAP o WinNT.

-   ://-separa il progID dal DN.

-   DN: nome distinto dell'oggetto ADSI, ovvero il percorso completo dell'oggetto, in cui il percorso è costituito da nomi distinti relativi (RDNs).

Un RDN è il nome dell'oggetto senza il percorso ed è univoco dagli oggetti di pari livello. Un RDN è costituito da un ID e un valore di attributo, ad esempio "DC = Fabrikam", dove DC è l'attributo e Fabrikam è il valore. Il controller di dominio è un ID di attributo RDN che corrisponde al componente di dominio.

Di seguito è riportato un esempio di ADsPath:

"LDAP://DC = Fabrikam, DC = com"

## <a name="binding-the-object"></a>Associazione dell'oggetto

Ecco come è possibile associare l'oggetto dominio in questo scenario:


```VB
Set dom = GetObject("LDAP://DC=Fabrikam,DC=Com")
```



Quando si esegue questo esempio di codice, ADSI usa il DN per determinare gli oggetti ADSI da associare. Dopo aver associato tali oggetti, è possibile accedere ai relativi metodi. Nell'esempio di codice precedente viene associato un oggetto di dominio a [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) e [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer). È ora possibile usare metodi su tali interfacce, ad esempio [**Get**](/windows/desktop/api/Iads/nf-iads-iads-get), [**put**](/windows/desktop/api/Iads/nf-iads-iads-put), [**create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create), [**Delete**](/windows/desktop/api/Iads/nf-iads-iadscontainer-delete)e [**MoveHere**](/windows/desktop/api/Iads/nf-iads-iadscontainer-movehere).

Dopo aver associato un oggetto di dominio, è possibile stampare alcuni degli attributi:


```VB
Debug.Print dom.Get("Name")
Debug.Print dom.Get("whenCreated")
```



Per ulteriori informazioni su ADsPath, vedere [Binding String](binding-string.md). Per ulteriori informazioni sull'associazione, vedere [associazione a un oggetto ADSI](binding-to-an-adsi-object.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di un'unità organizzativa](creating-an-organizational-unit.md)
</dt> </dl>

 

 




