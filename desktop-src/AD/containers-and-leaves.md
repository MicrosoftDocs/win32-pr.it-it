---
title: Contenitori e foglie
description: Active Directory Domain Services contenere una gerarchia di oggetti in cui ogni istanza dell'oggetto, ad eccezione della radice della gerarchia di directory, è contenuta in un altro oggetto.
ms.assetid: ef17e84c-6c7f-4ebe-a904-fead6c27518d
ms.tgt_platform: multiple
keywords:
- contenitori e foglie Active Directory
- Active Directory foglia
- Active Directory contenitore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f9039e4619ea0bd50d20c3bd425b6a8536a1034
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472646"
---
# <a name="containers-and-leaves"></a>Contenitori e foglie

Active Directory Domain Services contenere una gerarchia di oggetti in cui ogni istanza dell'oggetto, ad eccezione della radice della gerarchia di directory, è contenuta in un altro oggetto. La struttura di questa gerarchia è più flessibile rispetto a una file system di directory e file. Al contrario, le regole, nello [schema di Active Directory](active-directory-schema.md), determinano quali classi di oggetti possono contenere istanze di altre classi di oggetti. La definizione dello schema predefinito della classe di oggetti [**User**](/windows/desktop/ADSchema/c-user) , ad esempio, include le classi di oggetti dell' [**unità organizzativa**](/windows/desktop/ADSchema/c-organizationalunit) e del [**contenitore**](/windows/desktop/ADSchema/c-container) come possibili valori migliori. ovvero i contenitori o gli oggetti padre possibili di un'istanza dell'oggetto **utente** . Ciò significa che un oggetto **unità organizzativa** può contenere un oggetto **utente** , ma un oggetto **utente** non può contenere un altro oggetto **utente** , a meno che non venga modificata la definizione dello schema della classe **utente** .

Ad eccezione degli oggetti dello schema, ovvero degli oggetti [**classSchema**](/windows/desktop/ADSchema/c-classschema) o [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) che definiscono le classi e gli attributi che possono esistere in una foresta di server, qualsiasi oggetto in Active Directory Domain Services può essere un contenitore. In particolare, qualsiasi classe di oggetti visualizzata nell'attributo [**possSuperiors**](/windows/desktop/ADSchema/a-posssuperiors) o [**systemPossSuperiors**](/windows/desktop/ADSchema/a-systemposssuperiors) di una definizione di classe di oggetti è potenzialmente un contenitore. Per ulteriori informazioni sui contenitori di una classe di oggetti predefinita, vedere [Active Directory Domain Services Reference](active-directory-domain-services-reference.md). È possibile associare a livello di codice allo schema astratto e usare i metodi [**IADsClass:: Get \_ containment**](/windows/desktop/api/iads/nn-iads-iadsclass) o [**IADsClass:: Get \_ PossibleSuperiors**](/windows/desktop/api/iads/nn-iads-iadsclass) per ottenere le classi che una determinata classe può contenere o essere contenuta in. Per altre informazioni, vedere [Reading the abstract schema](reading-the-abstract-schema.md). È anche possibile leggere l'attributo [**PossibleInferiors**](/windows/desktop/ADSchema/a-possibleinferiors) di qualsiasi istanza dell'oggetto per determinare le classi di oggetti che l'oggetto può contenere. Tenere presente che **PossibleInferiors** è un attributo costruito, il che significa che viene calcolato dai  / valori **systemPossSuperiors** di possSuperiors delle altre definizioni della classe e che non viene effettivamente archiviato nella directory.

Tenere presente che lo schema Active Directory definisce una classe [**contenitore**](/windows/desktop/ADSchema/c-container) . Come illustrato in precedenza, un oggetto non deve essere un'istanza della classe **contenitore** come contenitore. Esiste anche una classe [**foglia**](/windows/desktop/ADSchema/c-leaf) e anche se le sottoclassi di questa classe non sono in genere contenitori, non esiste alcun motivo per cui non possono esserlo.

Infine, è possibile impostare un flag nell'identificatore di visualizzazione associato a una classe di oggetti per indicare che le interfacce utente devono sempre visualizzare le istanze della classe come foglie anziché contenitori. Questo consente di evitare che l'interfaccia utente venga ingombrata da un numero eccessivo di contenitori. Per altre informazioni, vedere [visualizzazione di contenitori come nodi foglia](viewing-containers-as-leaf-nodes.md).

 

 