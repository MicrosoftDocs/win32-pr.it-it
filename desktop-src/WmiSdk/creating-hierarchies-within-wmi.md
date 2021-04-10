---
description: Lo spazio dei nomi WMI è un oggetto di programmazione che definisce l'ambito per un set di classi e istanze. Le classi del provider WMI devono essere definite all'interno di uno spazio dei nomi.
ms.assetid: a00f26e6-bb81-45bc-a530-9346a074bb3c
ms.tgt_platform: multiple
title: Creazione di gerarchie all'interno di WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5743c8da8c40fc0419a96a8ec9c65e7e112573a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226954"
---
# <a name="creating-hierarchies-within-wmi"></a>Creazione di gerarchie all'interno di WMI

[*Lo spazio dei nomi WMI*](gloss-n.md) è un oggetto di programmazione che definisce l'ambito per un set di classi e istanze. Le classi del provider WMI devono essere definite all'interno di uno spazio dei nomi.

Gli spazi dei nomi descrivono diversi ambienti gestiti, ad esempio l'ambiente SMS. Poiché le classi e le istanze di uno schema definiscono i componenti di un ambiente gestito, per ogni nuovo schema è necessario un nuovo spazio dei nomi. Lo spazio dei nomi radice cimv2, ad esempio, \\ contiene le classi e le istanze definite nello schema Win32, nonché le classi del Common Information Model padre (CIM) da cui lo schema Win32 eredita. Le classi CIM sono definite da Distributed Management Task Force ([DMTF](https://www.dmtf.org/home)).

> [!Note]  
> Per assicurarsi che tutte le definizioni delle classi WMI per gli oggetti gestiti vengano ripristinate nel [*repository WMI*](gloss-w.md) se WMI presenta un errore e viene riavviato, usare l'istruzione del preprocessore [**\# pragma autocover**](pragma-autorecover.md) nel file [*Managed Object Format (MOF)*](gloss-m.md) .

 

WMI definisce uno spazio dei nomi come istanza della classe di sistema [**\_ \_ dello spazio dei nomi**](--namespace.md) o qualsiasi classe che deriva dallo **\_ \_ spazio dei nomi**. La classe di sistema **\_ \_ dello spazio dei nomi** ha una singola proprietà denominata **Name**, che deve essere univoca all'interno dell'ambito dello spazio dei nomi padre. La proprietà **Name** deve contenere anche una stringa che inizia con una lettera. Tutti gli altri caratteri nella stringa possono essere lettere, cifre o caratteri di sottolineatura. Tutti i caratteri non fanno distinzione tra maiuscole e minuscole.

Oltre a determinare il nome univoco per uno spazio dei nomi figlio, lo spazio dei nomi WMI padre può proteggere le istanze statiche delle classi da modifiche accidentali da parte di altri provider. Ad esempio, potrebbe risultare utile annidare un nuovo spazio dei nomi in uno spazio dei nomi esistente per un altro provider. Tuttavia, il provider originale può tentare di aggiornare tutte le istanze della classe in modo che corrispondano a un nuovo schema. In questo modo, il provider originale può eliminare tutti i sottoelementi figlio in uno spazio dei nomi. Sebbene sia un'azione appropriata per lo spazio dei nomi di destinazione, può influire sulle istanze di classe non correlate in uno spazio dei nomi figlio (ovvero, le classi del provider personalizzate).

Pertanto, in genere è consigliabile creare e registrare lo spazio dei nomi come separato dagli spazi dei nomi che non si controllano direttamente. Ciò è particolarmente vero se le classi derivano solo da classi CIM generali o da altre classi della società. Lo spazio dei nomi può trovarsi nello spazio dei nomi **radice** , ad esempio quanto segue:

**Radice/MyCompany/prodotto**

Se invece la nuova classe deriva dalla classe di un altro provider, potrebbe essere necessario archiviare la classe in uno spazio dei nomi secondario del provider. Si noti che questo espone la nuova classe all'eliminazione accidentale da parte del provider originale.

In WMI sono disponibili diversi modi per creare uno spazio dei nomi:

-   [Creazione di uno spazio dei nomi figlio con codice MOF](creating-a-child-namespace-with-mof-code.md)
-   [Creazione di uno spazio dei nomi di pari livello con codice MOF](creating-a-sibling-namespace-with-mof-code.md)
-   [Creazione di uno spazio dei nomi con l'API WMI](creating-a-namespace-with-the-wmi-api.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Progettazione di classi Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



