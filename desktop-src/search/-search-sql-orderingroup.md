---
description: La clausola ORDER IN GROUP viene usata insieme all'istruzione GROUP ON, che restituisce set di risultati in gruppi.
ms.assetid: edfa2037-3360-411d-8a12-cdb9680222f2
title: Clausola ORDER IN GROUP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83b17981f6368b67852e393d38ef8c4b856601d73014d9bdce40292e7e4a499d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944651"
---
# <a name="order-in-group-clause"></a>Clausola ORDER IN GROUP

La clausola ORDER IN GROUP viene usata insieme [all'istruzione GROUP ON,](-search-sql-group-on-over.md) che restituisce set di risultati in gruppi. La clausola ORDER IN GROUP consente di ordinare ogni gruppo restituito in modo diverso. Se ad esempio si raggruppa in base a System.Kind, è possibile ordinare tutti i documenti System.Docordinamento. LastAuthor, tutti i file musicali di System. Musica. AlbumArtist e tutti i messaggi di posta elettronica di System.Message.FromName.

## <a name="syntax"></a>Sintassi

Di seguito è riportata la sintassi della clausola ORDER IN GROUP:


```
GROUP ON <group column and optional ranges>
OVER (SELECT ... FROM SystemIndex
    ORDER 
        IN GROUP '<group name>' BY <column> [<direction>] [,<column> [<direction>]]
        [IN GROUP '<group name>' BY <column> [<direction>] [,<column> [<direction>]] ]
        [BY <column> [<direction>] [,<column> [<direction>]] ])
```



L'identificatore del nome di gruppo è un intervallo o un valore noto della colonna del gruppo, come specificato nell'istruzione GROUP ON. Ad esempio, i valori noti per System.Photo.ISOSpeed includono "ISO-100", "ISO-200" e così via. Un intervallo per System.Photo.DateTaken include '2006-1-1' e '2007-1-1' per un'istruzione come GROUP ON System.ItemDate \[ '2006-1-1', '2007-1-1'. \]

L'identificatore di colonna deve essere una colonna valida specificata nell'istruzione GROUP ON o SELECT. È possibile includere più di una colonna, separate da virgole. Ad esempio, se si raggruppa in base a System.Photo.ISOSpeed, è possibile ordinare tutte le foto ISO-100, prima in base a System.Photo.PhotosSpeed e quindi in base a System.Photo.Aperture.

L'identificatore di direzione facoltativo può essere ASC per l'ordine crescente (da basso a alto) o DESC per decrescente (dall'alto al basso). Se non si specifica un identificatore di direzione, viene usato il valore predefinito crescente. Se si specifica più di una colonna, ma non si specificano tutte le direzioni, la direzione specificata per ultima viene applicata a ogni colonna successiva fino a quando non si modifica in modo esplicito la direzione.

Gli intervalli o i valori non specificati in modo esplicito in una clausola ORDER GROUP IN vengono ordinati in ordine crescente in base ai valori nella colonna GROUP ON.

## <a name="examples"></a>Esempio

L'esempio seguente raggruppa i risultati in base alla proprietà System.Kind. La query ordinerebbe il gruppo "program" in base al nome dell'applicazione e il gruppo "music" in base al titolo dell'album e al numero di traccia. Il **gruppo NULL** verrà ordinato in base al nome dell'elemento. Tutti gli altri gruppi verrebbero ordinati in base alla data dell'elemento.


```
GROUP ON System.Kind 
OVER (SELECT System.ItemUrl, System.Music.AlbumTitle, System.Music.TrackNumber, System.ItemName, System.ItemDate, System.Kind FROM SystemIndex
    ORDER 
        IN GROUP 'program' BY System.ApplicationName ASC
        IN GROUP 'music' BY System.Music.AlbumTitle ASC, System.Music.TrackNumber ASC
        IN GROUP NULL BY System.ItemName
        BY System.ItemDate DESC)
```



L'esempio seguente raggruppa i risultati in base alla proprietà System.ItemDate e quindi ordina ogni gruppo in base all'URL, al tipo o al nome dell'elemento.


```
GROUP ON System.ItemDate ['2006-1-1', '2007-1-1', '2008-1-1'] 
OVER (SELECT System.ItemUrl, System.ItemName, System.ItemDate System.Kind FROM SystemIndex
    ORDER 
        IN GROUP MINVALUE BY System.ItemUrl ASC
        IN GROUP '2007-1-1' BY System.Kind
        IN GROUP NULL BY System.ItemName)
```



I risultati della query precedente verranno restituiti in cinque gruppi e ordinati come descritto nella tabella seguente.



| Gruppo    | Descrizione                                               | Ordinamento                                    |
|----------|-----------------------------------------------------------|----------------------------------------------|
| Minvalue | Elementi con date precedenti al 1-1-2006                          | Ordinato in base all'URL dell'elemento, in ordine crescente |
| 2006-1-1 | Elementi con date in data 1-1-2006 o precedenti al 1-1-2007 | Ordinato in base alla data dell'elemento, in ordine crescente      |
| 2007-1-1 | Elementi con date in data 1-1-2007 o precedenti al 1-1-2008 | Ordinato in base al valore del tipo, in ordine crescente     |
| 2008-1-1 | Elementi con date il giorno o dopo il 1-1-2008                     | Ordinato in base alla data dell'elemento, in ordine crescente      |
| **NULL** | Elementi senza valore nella colonna System.ItemDate         | Ordinato in base al nome dell'elemento, in ordine crescente      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[GROUP ON ... Oltre... affermazione](-search-sql-group-on-over.md)
</dt> <dt>

[Clausola ORDER BY](-search-sql-orderby.md)
</dt> </dl>

 

 



