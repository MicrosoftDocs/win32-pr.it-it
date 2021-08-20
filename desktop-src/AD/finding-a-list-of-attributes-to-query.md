---
title: Ricerca di un elenco di attributi su cui eseguire una query
description: Quando si cercano oggetti di una determinata classe, i confronti nel filtro di ricerca devono specificare gli attributi effettivamente esistenti negli oggetti di tale classe.
ms.assetid: 19d52933-e4b0-414f-9785-871e624da07b
ms.tgt_platform: multiple
keywords:
- Ricerca di un elenco di attributi per eseguire query su AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e0edfee59c42a8cf07be05ab31e58c0298f7285c8a02de659257e3b3cd14bfc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118189191"
---
# <a name="finding-a-list-of-attributes-to-query"></a>Ricerca di un elenco di attributi su cui eseguire una query

Quando si cercano oggetti di una determinata classe, i confronti nel filtro di ricerca devono specificare gli attributi effettivamente esistenti negli oggetti di tale classe. Per ottenere gli attributi dell'elenco in un oggetto di una determinata classe, eseguire l'associazione a tale classe nello schema astratto e recuperare le proprietà [**IADsClass.MandatoryProperties**](/windows/desktop/ADSI/iadsclass-property-methods) e **IADsClass.OptionalProperties.** Per altre informazioni, vedere [Lettura dello schema astratto](reading-the-abstract-schema.md).

Inoltre, tutti gli oggetti ereditano dalla classe astratta superiore. Pertanto, qualsiasi attributo nella **parte superiore** può esistere, anche se non può essere impostato, in qualsiasi oggetto.

Se si esegue una ricerca nel catalogo globale, assicurarsi di specificare gli attributi nel catalogo globale. Gli attributi inclusi nel catalogo globale hanno **isMemberOfPartialAttributeSet** impostato su **TRUE** nei **relativi oggetti attributeSchema.** Tenere presente che questi dati non sono disponibili nello schema astratto. leggerlo **dall'oggetto attributeSchema** nel contenitore dello schema.

Nel catalogo globale è possibile eseguire query su un attributo di collegamento indietro solo se vengono soddisfatte entrambe le condizioni seguenti: in primo luogo, l'attributo è contrassegnato per l'inclusione nel catalogo globale. In secondo piano, anche il collegamento di inoltro corrispondente è contrassegnato per l'inclusione nel catalogo globale. Ciò si applica ai filtri di query e ai risultati della query. Per altre informazioni, vedere [Attributi collegati](linked-attributes.md).

Vengono inoltre costruiti alcuni attributi, principalmente nell'oggetto utente. I filtri di query non possono contenere attributi costruiti. Gli attributi costruiti non possono essere valutati nei filtri di query. tuttavia, possono essere restituiti nei risultati della query. Ciò si applica a tutti i contesti di denominazione e al catalogo globale. Gli attributi costruiti hanno **ADS \_ SYSTEMFLAG \_ ATTR \_ IS \_ CONSTRUCTED** (0x00000004) nella **proprietà systemFlags** nei **relativi oggetti attributeSchema.**

> [!Note]  
> Per altre informazioni sulle classi e sugli attributi predefiniti inclusi nel sistema, vedere Active Directory Domain Services [Reference](active-directory-domain-services-reference.md). Queste pagine elencano gli attributi obbligatori e facoltativi di ogni classe di oggetto. Per gli attributi, la pagina di riferimento indica se l'attributo è indicizzato, costruito, collegato o nel catalogo globale.

 

 

 