---
title: Contenitori e lascia
description: Active Directory Domain Services una gerarchia di oggetti in cui ogni istanza di oggetto, ad eccezione della radice della gerarchia di directory, è contenuta da un altro oggetto.
ms.assetid: ef17e84c-6c7f-4ebe-a904-fead6c27518d
ms.tgt_platform: multiple
keywords:
- contenitori e lascia Active Directory
- Active Directory foglia
- contenitore Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be794e806a15bd7d220d5bcda0b517216d4dd75d93ed235e33ffc862eb7c18e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118021799"
---
# <a name="containers-and-leaves"></a>Contenitori e lascia

Active Directory Domain Services una gerarchia di oggetti in cui ogni istanza di oggetto, ad eccezione della radice della gerarchia di directory, è contenuta da un altro oggetto. La struttura di questa gerarchia è più flessibile rispetto a file system di directory e file. Le regole, nello schema [di Active Directory,](active-directory-schema.md)determinano invece quali classi di oggetti possono contenere istanze di altre classi di oggetti. Ad esempio, la definizione dello schema predefinita della [**classe di**](/windows/desktop/ADSchema/c-user) oggetti User include le classi di oggetti [**Organizational-Unit**](/windows/desktop/ADSchema/c-organizationalunit) e [**Container**](/windows/desktop/ADSchema/c-container) come possibili superiori. cio, possibili oggetti padre o contenitori di **un'istanza dell'oggetto** User. Ciò significa che un **oggetto Organizational-Unit** può contenere un oggetto **User,** ma un **oggetto User** non può contenere un altro oggetto **User,** a meno che non venga modificata la definizione dello schema **della classe User.**

Fatta eccezione per gli oggetti schema, ad esempio gli oggetti [**classSchema**](/windows/desktop/ADSchema/c-classschema) o [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) che definiscono le classi e gli attributi che possono esistere in una foresta server, qualsiasi oggetto in Active Directory Domain Services può essere un contenitore. In particolare, qualsiasi classe di oggetto visualizzata nell'attributo [**possSuperiors**](/windows/desktop/ADSchema/a-posssuperiors) o [**systemPossSuperiors**](/windows/desktop/ADSchema/a-systemposssuperiors) di una definizione di classe di oggetti è potenzialmente un contenitore. Per altre informazioni sui contenitori di una classe di oggetti predefinita, vedere Active Directory Domain Services [Reference](active-directory-domain-services-reference.md). È possibile eseguire l'associazione a livello di codice allo schema astratto e usare i metodi [**IADsClass::get \_ Containment**](/windows/desktop/api/iads/nn-iads-iadsclass) o [**IADsClass::get \_ PossibleSuperiors**](/windows/desktop/api/iads/nn-iads-iadsclass) per ottenere le classi che una determinata classe può contenere o contenere. Per altre informazioni, vedere [Lettura dello schema astratto](reading-the-abstract-schema.md). È anche possibile leggere [**l'attributo possibleInferiors**](/windows/desktop/ADSchema/a-possibleinferiors) di qualsiasi istanza di oggetto per determinare le classi di oggetti che l'oggetto può contenere. Tenere presente che **possibleInferiors** è un attributo costruito, ovvero viene calcolato dai valori **possSuperiors** / **systemPossSuperiors** delle altre definizioni di classe e non viene effettivamente archiviato nella directory.

Tenere presente che lo schema di Active Directory definisce una [**classe Container.**](/windows/desktop/ADSchema/c-container) Come illustrato in precedenza, non è necessario che un oggetto sia un'istanza della classe **Container** come contenitore. Esiste anche una [**classe Leaf**](/windows/desktop/ADSchema/c-leaf) e anche se le sottoclassi di questa classe non sono in genere contenitori, non esiste alcun motivo per cui non sia possibile.

Infine, è possibile impostare un flag sull'identificatore di visualizzazione associato a una classe di oggetti per indicare che le interfacce utente devono sempre visualizzare le istanze della classe come elementi foglia anziché come contenitori. Ciò consente di evitare che l'interfaccia utente sia ingombrata da troppi contenitori. Per altre informazioni, vedere [Visualizzazione di contenitori come nodi foglia.](viewing-containers-as-leaf-nodes.md)

 

 