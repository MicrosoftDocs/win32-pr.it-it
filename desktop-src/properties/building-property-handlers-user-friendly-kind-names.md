---
description: Il sistema di proprietà contiene una proprietà denominata System. Kind, che divide gli elementi in tipi in base all'estensione del nome di file e che gli utenti finali possono identificare facilmente con.
ms.assetid: 1466b4c7-49ea-417a-ac94-7b45515ccb96
title: Uso dei nomi dei tipi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f358306deaeb04d4ea30b10b0665cdc8323b4d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344816"
---
# <a name="using-kind-names"></a>Uso dei nomi dei tipi

Il sistema di proprietà contiene una proprietà denominata `System.Kind` , che divide gli elementi in tipi in base all'estensione del nome file e con cui gli utenti finali possono identificare facilmente.

Questo argomento è organizzato nel modo seguente:

-   [Informazioni sulla proprietà System. Kind](#about-the-systemkind-property)
-   [Gerarchia e registrazione del valore Kind](#kind-value-hierarchy-and-registration)
-   [Risorse aggiuntive](#additional-resources)
-   [Argomenti correlati](#related-topics)

## <a name="about-the-systemkind-property"></a>Informazioni sulla proprietà System. Kind

La tipologia è stata introdotta in Windows Vista per esprimere una nozione di tipo file più intuitiva. La `System.Kind` Proprietà divide gli elementi in tipi e fornisce un nome di tipo che gli utenti finali possono identificare, ad esempio documenti, musica, immagini e così via. Di conseguenza, i nomi dei tipi sono noti come intuitivi. Poiché la `System.Kind` proprietà è impostata sullo stesso valore per gli elementi dello stesso tipo di file e associa elementi con caratteristiche simili a una proprietà comune, il sistema e l'utente possono agire sul gruppo nel suo complesso. La proprietà, ad esempio, `System.Kind` può essere utilizzata per limitare la ricerca agli elementi di un tipo specifico, visualizzare le proprietà più rilevanti per un elemento nella visualizzazione contenuto oppure raggruppare elementi simili.

Poiché Kind è una proprietà di stringa multivalore, è possibile avere un `audio;video` `link;document` valore di tipo o. Un `System.Kind` valore è un elenco ordinato di valori stringa. In alcuni casi, potrebbe essere presente un solo elemento nell'elenco. In altri casi, un elemento può appartenere a più di un tipo. Per un esempio di elemento che appartiene a più di un tipo, vedere l'esempio di chiave del registro di sistema in questo argomento. I valori di stringa sono da un set predefinito di valori noti. I valori vengono confrontati utilizzando le funzioni di confronto tra stringhe senza distinzione tra maiuscole e minuscole e indipendenti dalle impostazioni locali. Queste stringhe non sono localizzate.

Alcuni nomi di tipi sono già associati a proprietà e modelli di layout. Ad esempio, gli elementi associati agli `Kind.Picture` elementi e associati a `Kind.Document` visualizzano proprietà diverse anche quando si trovano nella stessa vista, a causa delle proprietà e dei modelli di layout già associati a questi due nomi di tipo. Ogni tipo di elemento può essere associato a uno dei quattro modelli di layout univoci che definiscono il numero di proprietà visualizzate per ogni elemento e il relativo layout. Per altre informazioni, vedere [visualizzazione contenuto in base al tipo di file o all'associazione di tipo](/previous-versions/windows/desktop/legacy/ee330739(v=vs.85)).

## <a name="kind-value-hierarchy-and-registration"></a>Gerarchia e registrazione del valore Kind

Un `Kind` valore deve rappresentare uno dei valori nell'elenco seguente.

```
Item
   Folder
   Program
   Game
   WebHistory
   Feed
   Document
   Link
   Movie
   Music
   RecordedTV
   Video
   Picture
   Communications
      Calendar
      Contact
      E-Mail
      Task
      Journal
      Note
      InstantMessage
```

I gestori di proprietà possono dichiarare la `System.Kind` Proprietà in modo statico tramite il registro di sistema oppure possono fornire il valore in modo dinamico tramite il codice come se si trattasse di una proprietà standard.

Per definire in modo statico la `Kind` proprietà, viene aggiunta una voce di valore **reg \_ SZ** sotto la chiave del registro di sistema **KindMap** , come illustrato nell'esempio seguente.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  KindMap
                     .recipe = Document
                     .ccc = Contact; Communications
```

Si noti che `Kind` può essere un singolo valore o più valori in una stringa delimitata da punto e virgola. Quando si specificano più valori, il `Kind` valore più specifico viene elencato per primo con quanto segue il meno specifico. Nell'esempio, Contact viene denominato First perché è gerarchicamente più specifico delle comunicazioni. L' **elemento** value viene utilizzato e non deve essere specificato in modo esplicito.

## <a name="additional-resources"></a>Risorse aggiuntive

-   Per la documentazione di riferimento sulle proprietà, vedere [System. Kind](./props-system-kind.md) e [System. KindText](./props-system-kindtext.md).
-   Per ulteriori informazioni sulla creazione di nuovi tipi di file o sull'utilizzo di tipi di file esistenti, vedere [tipi di file](../shell/fa-file-types.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sui gestori delle proprietà](./building-property-handlers-properties.md)
</dt> <dt>

[Uso degli elenchi di proprietà](./building-property-handlers-property-lists.md)
</dt> <dt>

[Inizializzazione di gestori di proprietà](./building-property-handlers-property-handlers.md)
</dt> <dt>

[Registrazione e distribuzione di gestori di proprietà](./prophand-reg-dist.md)
</dt> <dt>

[Procedure consigliate e domande frequenti sul gestore delle proprietà](./prophand-bestprac-faq.md)
</dt> </dl>

 

 
