---
description: In questo argomento viene descritta una nuova visualizzazione in Esplora risorse, denominata visualizzazione contenuto, che Visualizza il contenuto più rilevante per ogni elemento.
title: Visualizzazione contenuto per tipo di file o tipo
ms.topic: article
ms.date: 05/31/2018
ms.assetid: E01A6726-14C4-4c00-81D4-AE1008088678
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 81982d2242a7ea466c10e7d0ee37d899eea3e687
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757361"
---
# <a name="content-view-by-file-type-or-kind"></a>Visualizzazione contenuto per tipo di file o tipo

In questo argomento viene descritta una nuova visualizzazione in Esplora risorse, denominata visualizzazione contenuto, che Visualizza il contenuto più rilevante per ogni elemento. Utilizzando un set di chiavi del registro di sistema, gli elementi possono definire un elenco di proprietà e un layout utilizzati dalla Shell per la visualizzazione del contenuto. La shell recupera le chiavi del registro di sistema usando la [matrice di associazioni](fa-perceivedtypes.md)dell'elemento.

## <a name="how-does-the-content-view-work"></a>Come funziona la visualizzazione del contenuto?

In Windows 7 e versioni successive, la visualizzazione contenuto usa una logica di ridimensionamento che rilascia le proprietà quando la dimensione della finestra diminuisce, per garantire che le proprietà più importanti abbiano ancora spazio per essere leggibili in modo chiaro. Lo screenshot seguente illustra la visualizzazione contenuto dei risultati della ricerca che contengono musica, immagini e documenti.

![Visualizzazione contenuto dei risultati della ricerca che contengono musica, immagini e documenti](images/content-view/contentviewsearchresults.png)

Alcune origini dati della Shell utilizzano la visualizzazione contenuto per impostazione predefinita, ma gli utenti possono selezionare la visualizzazione contenuto facendo clic sul pulsante **Visualizza controllo** in Esplora risorse. Un'origine dati della shell estende lo spazio dei nomi della shell ed espone gli elementi in un archivio dati. Gli elementi in un archivio dati possono essere indicizzati dal sistema di ricerca Windows utilizzando un gestore di protocollo.

## <a name="how-to-implement-the-content-view"></a>Come implementare la visualizzazione contenuto

Quando si registra un nuovo [tipo di file](fa-file-types.md) o [gestore di protocollo](../search/-search-3x-wds-extidx-prot-implementing.md), è possibile sfruttare la visualizzazione contenuto utilizzando uno di due approcci diversi. È possibile usare un set di proprietà e un modello di layout esistente oppure è possibile creare una combinazione personalizzata.

È possibile utilizzare una voce del registro di sistema per associare il tipo di file o l'elemento a un [tipo](../properties/building-property-handlers-user-friendly-kind-names.md)predefinito, ovvero una proprietà che è possibile considerare come una categoria di contenuto. Associando il tipo di file o l'elemento con determinati tipi, si ereditano automaticamente i modelli di layout di visualizzazione del contenuto e gli elenchi di proprietà di tale tipo. Windows definisce i modelli di layout di visualizzazione del contenuto e gli elenchi di proprietà per i tipi seguenti: Documents, email, Folder, Music, Picture e Generic. Questo tipo di associazione è consigliato. Consente di fornire l'esperienza coerente che un utente aspetta per gli elementi simili.

Per altre informazioni, vedere [tipi di file](fa-file-types.md) e [nomi](../properties/building-property-handlers-user-friendly-kind-names.md) di tipi e [come registrare un set di visualizzazioni di contenuto univoco di proprietà e pattern di layout per il tipo di file o l'elemento](register-a-unique-content-view-set-of-properties-and-layout-pattern-for-the-file-type-or-item.md).

## <a name="additional-resources"></a>Risorse aggiuntive

-   Per la documentazione di riferimento della proprietà, vedere [System. Kind](../properties/props-system-kind.md)e [System. KindText](../properties/props-system-kindtext.md).
-   Per la documentazione di riferimento di proprietà, vedere [System. propt. ContentViewModeForBrowse](../properties/props-system-proplist-contentviewmodeforbrowse.md)e [System. propt. ContentViewModeForSearch](../properties/props-system-proplist-contentviewmodeforsearch.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione dell'applicazione](app-registration.md)
</dt> <dt>

[Tipi di file](fa-file-types.md)
</dt> <dt>

[Funzionamento delle associazioni di file](fa-how-work.md)
</dt> <dt>

[Tipo di file Verifier](file-type-verifier.md)
</dt> <dt>

[Gestori di tipi di file](fa-file-extensions.md)
</dt> <dt>

[Identificatori a livello di codice](fa-progids.md)
</dt> <dt>

[Tipi percepiti](fa-perceivedtypes.md)
</dt> <dt>

[Matrici di associazione](fa-associationarray.md)
</dt> </dl>

 

 
