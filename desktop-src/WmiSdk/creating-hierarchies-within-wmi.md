---
description: Lo spazio dei nomi WMI è un oggetto di programmazione che definisce l'ambito per un set di classi e istanze. Le classi del provider WMI devono essere definite all'interno di uno spazio dei nomi.
ms.assetid: a00f26e6-bb81-45bc-a530-9346a074bb3c
ms.tgt_platform: multiple
title: Creazione di gerarchie all'interno di WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a2649fb764c1710613b27e1c9bbe518dd4cb8d02215df935ddccb59c9d7e922
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119568781"
---
# <a name="creating-hierarchies-within-wmi"></a>Creazione di gerarchie all'interno di WMI

[*Lo spazio dei*](gloss-n.md) nomi WMI è un oggetto di programmazione che definisce l'ambito per un set di classi e istanze. Le classi del provider WMI devono essere definite all'interno di uno spazio dei nomi.

Gli spazi dei nomi descrivono ambienti gestiti diversi, ad esempio l'ambiente SMS. Poiché le classi e le istanze di uno schema definiscono i componenti di un ambiente gestito, ogni nuovo schema richiede un nuovo spazio dei nomi. Ad esempio, lo spazio dei nomi cimv2 radice contiene le classi e le istanze definite nello schema Win32, nonché le classi Common Information Model cimv2 padre da cui eredita lo \\ schema Win32. Le classi CIM sono definite dalla Distributed Management Task Force ([DMTF](https://www.dmtf.org/home)).

> [!Note]  
> Per assicurarsi che tutte le definizioni di classe WMI per gli oggetti gestiti siano ripristinate nel [*repository WMI*](gloss-w.md) se WMI ha un errore e si riavvia, usare l'istruzione del preprocessore [**\# pragma autorecover**](pragma-autorecover.md) nel file di Managed Object Format [*(MOF).*](gloss-m.md)

 

WMI definisce uno spazio dei nomi come istanza della classe di sistema [**\_ \_ Namespace**](--namespace.md) o qualsiasi classe che deriva da **\_ \_ Namespace**. La **\_ \_ classe di** sistema Namespace ha una singola proprietà denominata **Name**, che deve essere univoca nell'ambito dello spazio dei nomi padre. La **proprietà Name** deve contenere anche una stringa che inizia con una lettera. Tutti gli altri caratteri nella stringa possono essere lettere, cifre o caratteri di sottolineatura. Per tutti i caratteri non viene distinzione tra maiuscole e minuscole.

Oltre a determinare il nome univoco per uno spazio dei nomi figlio, lo spazio dei nomi WMI padre può proteggere le istanze statiche delle classi da modifiche accidentali da parte di altri provider. Ad esempio, può risultare utile annidare un nuovo spazio dei nomi in uno spazio dei nomi esistente per un altro provider. Tuttavia, il provider originale può tentare di aggiornare tutte le istanze della classe in modo che corrispondano a un nuovo schema. In questo modo, il provider originale può eliminare tutti i sotto-elementi figlio in uno spazio dei nomi. Sebbene possa trattarsi di un'azione appropriata per lo spazio dei nomi di destinazione, può influire sulle istanze di classe non correlate in uno spazio dei nomi figlio, ad esempio le classi del provider.

Pertanto, è in genere consigliabile creare e registrare lo spazio dei nomi come separato dagli spazi dei nomi che non si controllano direttamente. Ciò vale soprattutto se le classi derivano solo da classi CIM generali o da altre classi dell'azienda. Lo spazio dei nomi può essere nello spazio dei nomi **Radice,** ad esempio:

**Root/myCompany/myProduct**

Al contrario, se la nuova classe deriva dalla classe di un altro provider, potrebbe essere necessario archiviare la classe in uno spazio dei nomi secondario di tale provider. Si noti che questa operazione espone la nuova classe all'eliminazione accidentale da parte del provider originale.

WMI offre diversi modi per creare uno spazio dei nomi:

-   [Creazione di uno spazio dei nomi figlio con codice MOF](creating-a-child-namespace-with-mof-code.md)
-   [Creazione di uno spazio dei nomi di pari livello con codice MOF](creating-a-sibling-namespace-with-mof-code.md)
-   [Creazione di uno spazio dei nomi con l'API WMI](creating-a-namespace-with-the-wmi-api.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Progettazione di Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



