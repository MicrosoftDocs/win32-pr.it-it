---
title: Ricerca di un elenco di attributi su cui eseguire una query
description: Durante la ricerca di oggetti di una classe specifica, i confronti nel filtro di ricerca devono specificare gli attributi che esistono effettivamente negli oggetti di tale classe.
ms.assetid: 19d52933-e4b0-414f-9785-871e624da07b
ms.tgt_platform: multiple
keywords:
- Ricerca di un elenco di attributi per la query AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4b6fb6b4d948a7cbc4d76caba9b78e189324eaa
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724514"
---
# <a name="finding-a-list-of-attributes-to-query"></a>Ricerca di un elenco di attributi su cui eseguire una query

Durante la ricerca di oggetti di una classe specifica, i confronti nel filtro di ricerca devono specificare gli attributi che esistono effettivamente negli oggetti di tale classe. Per ottenere gli attributi dell'elenco in un oggetto di una determinata classe, eseguire l'associazione a tale classe nello schema astratto e recuperare le proprietà [**IADsClass. MandatoryProperties**](/windows/desktop/ADSI/iadsclass-property-methods) e **IADsClass. OptionalProperties** . Per altre informazioni, vedere [Reading the abstract schema](reading-the-abstract-schema.md).

Inoltre, tutti gli oggetti ereditano dalla classe astratta top. Pertanto, qualsiasi attributo in **Top** può esistere, anche se non può essere impostato, su qualsiasi oggetto.

Se si esegue una ricerca nel catalogo globale, assicurarsi di specificare gli attributi nel catalogo globale. Per gli attributi inclusi nel catalogo globale l' **isMemberOfPartialAttributeSet** è impostato su **true** nei rispettivi oggetti **attributeSchema** . Tenere presente che questi dati non sono disponibili nello schema astratto; leggerlo dall'oggetto **attributeSchema** nel contenitore dello schema.

Nel catalogo globale è possibile eseguire una query su un attributo di collegamento indietro solo se vengono soddisfatte entrambe le condizioni seguenti: prima, l'attributo viene contrassegnato per l'inclusione nel catalogo globale. In secondo luogo, il collegamento in diretta corrispondente viene anche contrassegnato per l'inclusione nel catalogo globale. Questo vale per i filtri di query e i risultati della query. Per ulteriori informazioni, vedere [attributi collegati](linked-attributes.md).

Inoltre, vengono costruiti alcuni attributi, soprattutto sull'oggetto utente. I filtri query non possono contenere attributi costruiti. Non è possibile valutare gli attributi costruiti nei filtri di query. Tuttavia, possono essere restituiti nei risultati della query. Questo vale per tutti i contesti di denominazione e il catalogo globale. Gli attributi costruiti hanno **Ads \_ SYSTEMFLAG \_ attr \_ \_** (0x00000004) nella proprietà **systemFlags** sui rispettivi oggetti **attributeSchema** .

> [!Note]  
> Per ulteriori informazioni sulle classi e sugli attributi predefiniti inclusi nel sistema, vedere [Active Directory Domain Services Reference](active-directory-domain-services-reference.md). Queste pagine elencano gli attributi obbligatori e facoltativi di ogni classe di oggetti. Per gli attributi, la pagina di riferimento indica se l'attributo è indicizzato, costruito, collegato o nel catalogo globale.

 

 

 