---
description: Questo argomento descrive una nuova visualizzazione in Windows, denominata visualizzazione Contenuto, che visualizza il contenuto più pertinente per ogni elemento.
title: Visualizzazione contenuto per tipo o tipo di file
ms.topic: article
ms.date: 05/31/2018
ms.assetid: E01A6726-14C4-4c00-81D4-AE1008088678
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 83f70649bd0eb022bde9cc4a8c69e0df162fe2551268f611390bae835409e939
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858713"
---
# <a name="content-view-by-file-type-or-kind"></a>Visualizzazione contenuto per tipo o tipo di file

Questo argomento descrive una nuova visualizzazione in Windows, denominata visualizzazione Contenuto, che visualizza il contenuto più pertinente per ogni elemento. Usando un set di chiavi del Registro di sistema, gli elementi possono definire un elenco di proprietà e un layout che la shell usa per la visualizzazione contenuto. La shell recupera le chiavi del Registro di sistema usando la matrice di associazioni [dell'elemento](fa-perceivedtypes.md).

## <a name="how-does-the-content-view-work"></a>Funzionamento della visualizzazione contenuto

In Windows 7 e versioni successive, la visualizzazione Contenuto usa una logica di ridimensionamento che elimina le proprietà quando le dimensioni della finestra diminuiscono, per garantire che le proprietà più critiche hanno ancora spazio per essere chiaramente leggibili. Lo screenshot seguente illustra la visualizzazione Contenuto dei risultati della ricerca contenenti musica, immagini e documenti.

![visualizzazione contenuto dei risultati della ricerca contenenti musica, immagini e documenti](images/content-view/contentviewsearchresults.png)

Alcune origini dati della shell usano la visualizzazione contenuto per impostazione predefinita, ma gli utenti possono selezionare la visualizzazione Contenuto facendo clic **sul** pulsante Visualizza controllo in Windows Explorer. Un'origine dati Shell estende lo spazio dei nomi Shell ed espone gli elementi in un archivio dati. Gli elementi in un archivio dati possono essere indicizzati dal Windows di ricerca usando un gestore di protocollo.

## <a name="how-to-implement-the-content-view"></a>Come implementare la visualizzazione contenuto

Quando si registra un [](../search/-search-3x-wds-extidx-prot-implementing.md)nuovo gestore di protocollo o tipo di [file,](fa-file-types.md) è possibile sfruttare la visualizzazione Contenuto usando uno dei due approcci diversi. È possibile usare un set esistente di proprietà e un modello di layout oppure è possibile creare una propria combinazione.

È possibile usare una voce del Registro di sistema per associare il tipo di file o l'elemento a un tipo [predefinito,](../properties/building-property-handlers-user-friendly-kind-names.md)ovvero una proprietà che può essere definita una categoria di contenuto. Associando il tipo di file o l'elemento a determinati di questi tipi, si ereditano automaticamente gli elenchi di proprietà e i modelli di layout della visualizzazione Contenuto di Kind. Windows definisce modelli di layout di visualizzazione contenuto ed elenchi di proprietà per i tipi seguenti: documenti, posta elettronica, cartella, musica, immagine e generica. Questo tipo di associazione è consigliato. Consente di offrire un'esperienza coerente che un utente si aspetta per elementi simili.

Per altre informazioni, vedere [](../properties/building-property-handlers-user-friendly-kind-names.md) [Tipi di file](fa-file-types.md) e nomi di tipi e Come registrare un set univoco di proprietà e modello di layout per il tipo di file [o l'elemento](register-a-unique-content-view-set-of-properties-and-layout-pattern-for-the-file-type-or-item.md).

## <a name="additional-resources"></a>Risorse aggiuntive

-   Per la documentazione di riferimento delle proprietà, vedere [System.Kind](../properties/props-system-kind.md)e [System.KindText.](../properties/props-system-kindtext.md)
-   Per la documentazione di riferimento di [PropList, vedere System.PropList.ContentViewModeForBrowse](../properties/props-system-proplist-contentviewmodeforbrowse.md)e [System.PropList.ContentViewModeForSearch.](../properties/props-system-proplist-contentviewmodeforsearch.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione dell'applicazione](app-registration.md)
</dt> <dt>

[Tipi di file](fa-file-types.md)
</dt> <dt>

[Funzionamento delle associazioni di file](fa-how-work.md)
</dt> <dt>

[Verifica del tipo di file](file-type-verifier.md)
</dt> <dt>

[Gestori di tipi di file](fa-file-extensions.md)
</dt> <dt>

[Identificatori a livello di codice](fa-progids.md)
</dt> <dt>

[Tipi percepiti](fa-perceivedtypes.md)
</dt> <dt>

[Matrici di associazioni](fa-associationarray.md)
</dt> </dl>

 

 
