---
description: La clausola ORDER IN GROUP viene utilizzata insieme all'istruzione GROUP ON, che restituisce set di risultati in gruppi.
ms.assetid: edfa2037-3360-411d-8a12-cdb9680222f2
title: Clausola ORDER IN GROUP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b4a3a39ffeb2704a099389a6668a075fb4a24f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342951"
---
# <a name="order-in-group-clause"></a>Clausola ORDER IN GROUP

La clausola ORDER IN GROUP viene utilizzata insieme all'istruzione [Group on](-search-sql-group-on-over.md) , che restituisce set di risultati in gruppi. La clausola ORDER IN GROUP consente di ordinare ogni gruppo restituito in modo diverso. Se si esegue il raggruppamento in System. Kind, ad esempio, è possibile ordinare tutti i documenti in base System.Document. LastAuthor, tutti i file musicali per System. Music. AlbumArtist e tutti i messaggi di posta elettronica da System. Message. FromName.

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



L'identificatore del nome del gruppo è un intervallo o un valore noto della colonna di gruppo, come specificato nell'istruzione GROUP ON. Ad esempio, i valori noti per System. Photo. ISOSpeed includono ' ISO-100',' ISO-200' e così via. Un intervallo per System. Photo. DateTaken includerà' 2006-1-1' è 2007-1-1' per un'istruzione come GROUP in System. ItemDate \[ ' 2006-1-1',' 2007-1-1' \] .

L'identificatore di colonna deve essere una colonna valida specificata nell'istruzione GROUP ON o SELECT. È possibile includere più di una colonna, separate da virgole. Se, ad esempio, si esegue il raggruppamento in System. Photo. ISOSpeed, è possibile ordinare tutte le foto ISO-100, prima in base a System. Photo. ShutterSpeed e quindi a System. Photo. aperture.

L'identificatore di direzione facoltativo può essere ASC per l'ordine crescente (da basso a alto) o DESC per la decrescente (da alto a basso). Se non si specifica un identificatore di direzione, viene usato il valore predefinito Ascending. Se si specifica più di una colonna, ma non si specificano tutte le direzioni, la direzione specificata per ultima viene applicata a ogni colonna successiva fino a quando non si modifica in modo esplicito la direzione.

Gli intervalli o i valori non specificati in modo esplicito in una clausola ORDER GROUP IN sono ordinati in ordine crescente in base ai valori della colonna GROUP ON.

## <a name="examples"></a>Esempio

Nell'esempio seguente vengono raggruppati i risultati in base alla proprietà System. Kind. La query ordina il gruppo ' Program ' in base al nome dell'applicazione e al gruppo ' Music ' in base al titolo dell'album e al numero di traccia. Il gruppo **null** verrebbe ordinato in base al nome dell'elemento. Tutti gli altri gruppi verranno ordinati in base alla data dell'elemento.


```
GROUP ON System.Kind 
OVER (SELECT System.ItemUrl, System.Music.AlbumTitle, System.Music.TrackNumber, System.ItemName, System.ItemDate, System.Kind FROM SystemIndex
    ORDER 
        IN GROUP 'program' BY System.ApplicationName ASC
        IN GROUP 'music' BY System.Music.AlbumTitle ASC, System.Music.TrackNumber ASC
        IN GROUP NULL BY System.ItemName
        BY System.ItemDate DESC)
```



Nell'esempio seguente vengono raggruppati i risultati in base alla proprietà System. ItemDate, quindi viene ordinata l'URL, il tipo o il nome di ogni elemento Group by.


```
GROUP ON System.ItemDate ['2006-1-1', '2007-1-1', '2008-1-1'] 
OVER (SELECT System.ItemUrl, System.ItemName, System.ItemDate System.Kind FROM SystemIndex
    ORDER 
        IN GROUP MINVALUE BY System.ItemUrl ASC
        IN GROUP '2007-1-1' BY System.Kind
        IN GROUP NULL BY System.ItemName)
```



I risultati della query precedente verrebbero restituiti in cinque gruppi e ordinati come descritto nella tabella seguente.



| Gruppo    | Descrizione                                               | Ordinamento                                    |
|----------|-----------------------------------------------------------|----------------------------------------------|
| MINVALUE | Elementi con date precedenti alla 2006-1-1                          | Ordinato in base all'URL dell'elemento, in ordine crescente |
| 2006-1-1 | Elementi con date il o dopo il 2006-1-1 ma prima del 2007-1-1 | Ordinato per data dell'elemento, in ordine crescente      |
| 2007-1-1 | Elementi con date il o dopo il 2007-1-1 ma prima del 2008-1-1 | Ordinato per valore di tipo, in ordine crescente     |
| 2008-1-1 | Elementi con date il o dopo il 2008-1-1                     | Ordinato per data dell'elemento, in ordine crescente      |
| **NULL** | Elementi senza valore nella colonna System. ItemDate         | Ordinato in base al nome dell'elemento, in ordine crescente      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[RAGGRUPPA IN... SOPRA... Istruzione](-search-sql-group-on-over.md)
</dt> <dt>

[Clausola ORDER BY](-search-sql-orderby.md)
</dt> </dl>

 

 



