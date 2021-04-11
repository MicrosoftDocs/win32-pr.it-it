---
title: Visualizzazione di contenitori come nodi foglia
description: Qualsiasi oggetto in Active Directory Domain Services può essere un contenitore di altri oggetti.
ms.assetid: 38300ca5-745a-4640-9723-6052a9843f45
ms.tgt_platform: multiple
keywords:
- Visualizzazione di contenitori come nodi foglia
- contenitori AD, visualizzazione come nodi foglia
- AD foglia, visualizzazione di contenitori come nodi foglia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1631526ed78132829a7576960a997b13cc232b5f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104336759"
---
# <a name="viewing-containers-as-leaf-nodes"></a>Visualizzazione di contenitori come nodi foglia

Qualsiasi oggetto in Active Directory Domain Services può essere un contenitore di altri oggetti. Questo può ingombrare l'interfaccia utente, pertanto è possibile dichiarare che un oggetto di una classe specifica deve essere visualizzato solo come foglia nell'interfaccia utente. L'attributo **treatAsLeaf** è un attributo di identificatore di visualizzazione a valore singolo che determina se gli oggetti di tale classe devono essere visualizzati solo come oggetti foglia. Questo attributo è un valore booleano che, se **true**, indica che gli oggetti della classe devono essere visualizzati solo come elementi foglia. Se **false**, indica che gli oggetti della classe possono essere visualizzati come contenitore o foglia. Come tutti gli attributi dell'identificatore di visualizzazione, l'attributo **treatAsLeaf** viene impostato in base alle singole impostazioni locali, pertanto questo attributo può essere localizzato in base alle esigenze. Ad esempio, la **visualizzazione dell'utente** per l'identificatore di visualizzazione delle impostazioni locali inglesi (0409) ha l'attributo **TreatAsLeaf** impostato su **true** per impostazione predefinita. In questo modo, l'interfaccia utente visualizzerà tutti gli oggetti **utente** come oggetti foglia.

**Per impostare il valore dell'attributo **treatAsLeaf****

1.  Eseguire l'associazione all'attributo di visualizzazione desiderato nelle impostazioni locali desiderate. Per ulteriori informazioni e un esempio di codice, vedere [contenitore DisplaySpecifiers](displayspecifiers-container.md).
2.  Usare il metodo [**IADs::P UT**](/windows/desktop/api/iads/nf-iads-iads-put) per impostare l'attributo **treatAsLeaf** su **true** o **false**.
3.  Per eseguire il commit delle modifiche nella directory, chiamare il metodo [**IADs:: seinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) .

 

 