---
description: Il sistema di proprietà contiene una proprietà denominata System.Kind, che divide gli elementi in tipi in base all'estensione di file e con cui gli utenti finali possono identificarsi facilmente.
ms.assetid: 1466b4c7-49ea-417a-ac94-7b45515ccb96
title: Uso dei nomi dei tipi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dca36d7c1de587efd8d96f0c18aaca9457721714
ms.sourcegitcommit: ecd0ba4732f5264aab9baa2839c11f7fea36318f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/07/2021
ms.locfileid: "113481876"
---
# <a name="using-kind-names"></a>Uso dei nomi dei tipi

Il sistema di proprietà contiene una proprietà denominata , che divide gli elementi in tipi in base all'estensione di file e con cui gli utenti finali `System.Kind` possono identificarsi facilmente.

Questo argomento è organizzato come segue:

-   [Informazioni sulla proprietà System.Kind](#about-the-systemkind-property)
-   [Gerarchia dei valori di tipo e registrazione](#kind-value-hierarchy-and-registration)
-   [Risorse aggiuntive](#additional-resources)
-   [Argomenti correlati](#related-topics)

## <a name="about-the-systemkind-property"></a>Informazioni sulla proprietà System.Kind

Kind è stato introdotto in Windows Vista per esprimere una nozione più semplice del tipo di file. La proprietà divide gli elementi in tipi e fornisce un nome tipo che gli utenti finali possono identificare, ad esempio `System.Kind` Documenti, Musica, Immagini e così via. Di conseguenza, i nomi dei tipi sono noti come descrittivi. Poiché la proprietà è impostata sullo stesso valore per gli elementi dello stesso tipo di file e associa elementi con caratteristiche simili a una proprietà comune, il sistema e l'utente possono agire sull'intero `System.Kind` gruppo. Ad esempio, la proprietà può essere usata per limitare una ricerca agli elementi di un tipo specifico, visualizzare le proprietà più rilevanti per un elemento nella visualizzazione Contenuto o raggruppare `System.Kind` elementi simili.

Poiché Kind è una proprietà stringa multivalore, è possibile avere un `audio;video` valore o `link;document` Kind. Un `System.Kind` valore è un elenco ordinato di valori stringa. In alcuni casi, potrebbe essere presente un solo elemento nell'elenco. In altri casi, un elemento può appartenere a più di un tipo. Per un esempio di un elemento appartenente a più di un tipo, vedere l'esempio di chiave del Registro di sistema in questo argomento. I valori stringa derivano da un set predefinito di valori noti. I valori vengono confrontati usando funzioni di confronto tra stringhe senza distinzione tra maiuscole e minuscole e senza distinzione tra maiuscole e minuscole. Queste stringhe non sono localizzate.

Alcuni nomi di tipo sono già associati a proprietà e modelli di layout. Ad esempio, gli elementi associati a e gli elementi associati a visualizzano proprietà diverse anche quando sono nella stessa visualizzazione, a causa delle proprietà e dei modelli di layout già associati a questi due `Kind.Picture` `Kind.Document` nomi Kind. Ogni tipo di elemento può essere associato a uno dei quattro modelli di layout univoci che definiscono il numero di proprietà visualizzate per ogni elemento e il relativo layout. Per altre informazioni, vedere [Visualizzazione contenuto basata sull'associazione tipo di file o tipo](/previous-versions/windows/desktop/legacy/ee330739(v=vs.85)).

## <a name="kind-value-hierarchy-and-registration"></a>Gerarchia dei valori di tipo e registrazione

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

I gestori delle proprietà possono dichiarare la proprietà in modo statico tramite il Registro di sistema oppure possono fornire il valore in modo dinamico tramite il codice come con `System.Kind` una proprietà standard.

Per definire in modo statico la proprietà, viene aggiunta una voce di valore `Kind` **REG \_ SZ** nella chiave del Registro di sistema **KindMap,** come illustrato nell'esempio seguente.

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

Si noti che `Kind` può essere un singolo valore o più valori in una stringa delimitata da punti e virgola. Quando si specificano più valori, il valore `Kind` più specifico viene elencato per primo con il valore meno specifico seguente. Nell'esempio il nome Contact viene assegnato per primo perché è gerarchicamente più specifico di Communications. Il valore **Item** viene assunto e non deve essere specificato in modo esplicito.

## <a name="additional-resources"></a>Risorse aggiuntive

-   Per la documentazione di riferimento sulle proprietà, [vedere System.Kind](./props-system-kind.md) e [System.KindText](./props-system-kindtext.md).
-   Per altre informazioni sulla creazione di nuovi o sull'uso di tipi di file esistenti, vedere [Tipi di file](../shell/fa-file-types.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sui gestori delle proprietà](./building-property-handlers-properties.md)
</dt> <dt>

[Uso degli elenchi di proprietà](./building-property-handlers-property-lists.md)
</dt> <dt>

[Inizializzazione dei gestori di proprietà](./building-property-handlers-property-handlers.md)
</dt> <dt>

[Registrazione e distribuzione di gestori di proprietà](./prophand-reg-dist.md)
</dt> <dt>

[Procedure consigliate e domande frequenti sul gestore delle proprietà](./prophand-bestprac-faq.yml)
</dt> </dl>

 

 
