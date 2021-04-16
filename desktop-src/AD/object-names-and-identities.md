---
title: Nomi e identità degli oggetti
description: Un oggetto in Active Directory Domain Services dispone di diverse identità, incluse le seguenti.
ms.assetid: ad8bc74d-45a8-4df3-bfb8-35dd376b9c0b
ms.tgt_platform: multiple
keywords:
- nomi di oggetti e identità Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a803b4cc068a3ee0f9e2a75f61ff239c1d971bf3
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472515"
---
# <a name="object-names-and-identities"></a>Nomi e identità degli oggetti

Un oggetto in Active Directory Domain Services dispone di diverse identità, incluse le seguenti.

## <a name="relative-distinguished-name"></a>Nome distinto relativo

Il nome distinto relativo è il nome definito dall'attributo di denominazione di un oggetto. L'attributo **rDnAttID** di un oggetto **classSchema** identifica l'attributo Naming per le istanze della classe. La maggior parte delle classi di oggetti usa l'attributo **CN** (nome comune) come attributo di denominazione. Il nome distinto relativo di un oggetto deve essere univoco nel contenitore in cui si trova l'oggetto. Possono essere presenti molte istanze di oggetti con lo stesso nome distinto relativo, ma due non possono trovarsi nello stesso contenitore. Per ulteriori informazioni sull'attributo **rDnAttID** e sugli oggetti **classSchema** , vedere [caratteristiche delle classi di oggetti](characteristics-of-object-classes.md).

## <a name="distinguished-name"></a>Nome distinto

Il [*nome distinto*](/previous-versions/windows/desktop/legacy/ms681901(v=vs.85)) è il nome corrente dell'oggetto ed è contenuto nell'attributo **Distinguishname** dell'oggetto. Il nome distinto è una stringa che include la posizione dell'oggetto e viene formata concatenando il nome distinto relativo dell'oggetto e ognuno dei relativi predecessori fino alla radice. Il nome distinto del contenitore Users nel dominio Fabrikam.com, ad esempio, sarà "CN = Users, DC = Fabrikam, DC = com". I nomi distinti sono univoci all'interno di una foresta. Il nome distinto di un oggetto viene modificato quando l'oggetto viene spostato o rinominato.

## <a name="object-guid"></a>GUID oggetto

Il GUID dell'oggetto è un identificatore univoco globale assegnato da Active Directory Domain Services quando viene creata l'istanza dell'oggetto. Il GUID dell'oggetto è contenuto nell'attributo **objectGUID** dell'oggetto. Un GUID è un numero a 128 bit che garantisce l'univocità nello spazio e nel tempo. I GUID oggetto non cambiano mai. Pertanto, se un oggetto viene rinominato o spostato in un punto qualsiasi della foresta aziendale, il GUID dell'oggetto rimane invariato. Le applicazioni che salvano i riferimenti agli oggetti in Active Directory Domain Services devono utilizzare il GUID dell'oggetto per garantire che il riferimento all'oggetto sopravviva a una ridenominazione dell'oggetto. Il nome distinto di un oggetto potrebbe cambiare, ma il GUID dell'oggetto non lo sarà.

## <a name="other-identities"></a>Altre identità

Le istanze degli oggetti possono avere molti altri attributi e gli attributi possono essere usati per l'identificazione dalle applicazioni. Ad esempio, gli oggetti entità di sicurezza (istanze delle classi di oggetti **User**, **computer** e **Group** ) presentano gli attributi **userPrincipalName**, **sAMAccountName** e **objectSID** . Questi attributi sono "nomi" molto importanti per Windows 2000, ma non fanno parte dell'identità dell'oggetto dal punto di vista della directory.

 

 