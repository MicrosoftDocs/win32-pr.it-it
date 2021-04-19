---
title: Elemento Fragment
description: L'elemento Fragment specifica una condizione della query che seleziona gli elementi dalla libreria. Le condizioni sono specificate dalle stringhe di condizione. Una stringa di condizione ha in genere una parte del nome, una parte di condizione e una parte del valore.
ms.assetid: 1575318f-8527-42ba-9c2f-9993a60987d7
keywords:
- Elemento Fragment Media Player Windows
topic_type:
- apiref
api_name:
- fragment Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: da4cd18c6286cf2439e310b4e797f6978f3b2395
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330109"
---
# <a name="fragment-element"></a>Elemento Fragment

L'elemento **Fragment** specifica una condizione della query che seleziona gli elementi dalla libreria. Le condizioni sono specificate dalle stringhe di condizione. Una stringa di condizione ha in genere una parte del nome, una parte di condizione e una parte del valore.

``` syntax
<fragment
    name = "string"
>
</fragment>
```

## <a name="attributes"></a>Attributi

<dl> <dt>

<span id="name__required______________"></span><span id="NAME__REQUIRED______________"></span>**nome** (obbligatorio) 
</dt> <dd>

Parte di una stringa di condizione. Vedere la sezione Osservazioni.

</dd> </dl>

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia | Elementi                                                               |
|-----------|------------------------------------------------------------------------|
| Padre    | [Filter](filter-element.md), [sourceFilter](sourcefilter-element.md) |
| Figlio     | [argument](argument-element.md)                                       |



 

## <a name="remarks"></a>Commenti

Determinate stringhe di condizione hanno una parte dell'attributo dei metadati, una parte della condizione e una parte del valore. Nella stringa di condizione "Album Artist is Joe", ad esempio, la parte relativa all'attributo dei metadati è "Album Artist", la parte della condizione è "is" e la parte value è "Joe".

Esempio:


```XML
<fragment name = "Album Artist">
    <argument name = "condition">Is</argument>
    <argument name = "value">Joe</argument>
</fragment>
```



Per le stringhe di condizione di questo tipo, nella tabella seguente vengono illustrati i possibili attributi di metadati, le possibili condizioni e i possibili valori:



| Attributo Metadata                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | Condizioni possibili                                                                                             | Valori possibili                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Artista ActorAlbum<br/> Titolo album<br/> Autore<br/> Didascalia<br/> Channel<br/> Composer<br/> Conduttore<br/> Provider di contenuti<br/> Genere del provider di contenuti<br/> Autore di contributi<br/> Testo copyright<br/> Responsabile<br/> Episodio<br/> Tipo di file<br/> Genre<br/> Chiave<br/> Parole chiave<br/> Linguaggio<br/> Umore<br/> Classificazione parentale<br/> Periodo<br/> Producer<br/> Provider<br/> Publisher<br/> Serie<br/> Nome stazione<br/> Sottogenere<br/> Sottotitolo<br/> Titolo<br/> Writer<br/> | EqualsDoes non uguale<br/> È<br/> Non è<br/> Contiene<br/> Non contiene<br/> | Qualsiasi valore di stringa                                                                                                                                                                                                                                                                                                  |
| Velocità in bit (espressa in kilobyte al secondo).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | EqualsDoes non uguale<br/> È<br/> Non è<br/> Contiene<br/> Non contiene<br/> | 4864<br/> 96<br/> 128<br/> 160<br/> 192<br/> 256<br/> 300<br/> 500<br/> 750<br/> 1000<br/> 1500<br/> 3000<br/> 4500<br/> 6000<br/> 7500<br/>                                                                            |
| Tipo di supporto secondario                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | EqualsDoes non uguale<br/> È<br/> Non è<br/> Contiene<br/> Non contiene<br/> | Audio: NewsAudio: talk show<br/> Audio: libri audio<br/> Audio: Word vocale<br/> Video: novità<br/> Video: presentazione<br/> Video: Home page<br/> Video: film/film<br/> Video: Show TV<br/> Video: video aziendale<br/> Video: video di musica<br/> |
| Dimensioni file (in KB) altezza immagine<br/> Larghezza immagine<br/> Conteggio riproduzione: totali pomeridiani<br/> Conteggio riproduzione: totali serali<br/> Conteggio riproduzione: totali mattina<br/> Conteggio riproduzione: totali notturni<br/> Conteggio riproduzione: totale complessivo<br/> Conteggio riproduzione: totale giorni feriali<br/> Numero di riscontri: weekend totale<br/>                                                                                                                                                                                                                                                                                                                  | È minore di è maggiore di<br/> È<br/> Non è<br/>                                          | Qualsiasi numero                                                                                                                                                                                                                                                                                                        |
| Trasmissione temporizzata codificata<br/> Data di registrazione<br/> Data di inizio<br/> Anno versione<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | Precede dopo<br/> È<br/> Non è<br/>                                                    | Settimana YesterdayLast<br/> Ultimo mese<br/> 6 mesi<br/> 1 anno<br/> 2 anni<br/> 5 anni<br/> 2000<br/> anni '90<br/> anni '80<br/> anni '70<br/> 1960<br/> 1950<br/> 1940<br/>                                                            |
| Date Added                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | Precede dopo<br/> È<br/> Non è<br/>                                                    | Settimana YesterdayLast<br/> Ultimo mese<br/> 6 mesi<br/> 1 anno<br/> 2 anni<br/> 5 anni<br/>                                                                                                                                                                                   |
| Data ultima riproduzione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               | ThanMore meno recenti di<br/> È<br/> Non è<br/>                                           | Settimana YesterdayLast<br/> Ultimo mese<br/> 6 mesi<br/> 1 anno<br/> 2 anni<br/> 5 anni<br/>                                                                                                                                                                                   |
| Mese impiegato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | Precede è più recente di<br/> È<br/> Non è<br/>                                         | 12<br/> 3<br/> 4<br/> 5<br/> 6<br/> 7<br/> 8<br/> 9<br/> 10<br/> 11<br/> 12<br/> 13<br/>                                                                                                                                                  |
| Anno impiegato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | Precede è più recente di<br/> È<br/> Non è<br/>                                         | Qualsiasi anno                                                                                                                                                                                                                                                                                                          |
| Classificazione RatingMy automatica<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                | È almeno non più di<br/> È<br/> Non è<br/>                                           | Stella Unrated1<br/> 2 stelle<br/> 3 stelle<br/> 4 stelle<br/> 5 stelle<br/>                                                                                                                                                                                                              |
| Campo personalizzato \# 1Custom campo \# 2<br/> File Name<br/> Campi chiave<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         | ContainsDoes non contiene<br/>                                                                             | Qualsiasi stringa                                                                                                                                                                                                                                                                                                        |



 

Alcune stringhe di condizione hanno una parte limitere, una parte di numero e una parte di formato. Ad esempio, nella stringa di condizione "Limita dimensioni totali a 3 megabyte", la parte limitere è "Limita dimensioni totali a", la parte numero è "3" e la parte del formato è "megabyte".

Esempio:


```XML
<fragment name = "Limit Total Size To">
  <argument name = "number">3</argument>
  <argument name = "format">Megabytes</argument>
</fragment>
```



Per le stringhe di condizione di questo tipo nella tabella seguente sono indicati i limiti e i formati possibili.



| Limitatore                 | Numeri possibili | Formati possibili                |
|-------------------------|------------------|---------------------------------|
| Limita dimensioni totali a     | Qualsiasi numero       | Kilobyte, megabyte, Gigabyte |
| Limita durata totale a | Qualsiasi numero       | Secondi, minuti, ore, giorni   |



 

Alcune stringhe di condizione hanno una parte del limitere e una parte di numeri. Ad esempio, nella stringa di condizione "limita numero di elementi a 25", la parte limitere è "limite numero di elementi" e la parte numero è "25".

Esempio:


```XML
<fragment name = "Limit Number of Items">
    <argument name = "number">25</argument>
</fragment>
```



Per le stringhe di condizione di questo tipo la tabella seguente mostra l'unico limite possibile.



| Limitatore               | Numeri possibili |
|-----------------------|------------------|
| Limita numero di elementi | Qualsiasi numero       |



 

Alcune stringhe di condizione hanno una parte di protezione e una parte della condizione. Nella stringa di condizione "Protection is present", ad esempio, la parte Protection è "Protection" e la parte della condizione è "is".

Esempio:


```XML
<fragment name = "Protection">
    <argument name = "condition">Is</argument>
</fragment>
```



Per le stringhe di condizione di questo tipo, nella tabella seguente vengono illustrate le condizioni possibili.



| Parte della protezione | Condizioni possibili             |
|--------------------|---------------------------------|
| Protezione         | È<br/> Non è<br/> |



 

È presente un tipo di elemento **Fragment** che non contiene una stringa di condizione. Se l'attributo Name di un elemento **Fragment** è "ordine di riproduzione casuale", l'elemento **Fragment** non contiene elementi **argument** . Questo elemento **Fragment** indica al lettore di riprodurre l'elenco in ordine casuale.

Esempio:


```XML
<fragment name = "Randomize Playback Order">
</fragment>
```



Alcune stringhe di condizione hanno una parte di ordinamento, una parte del valore e una parte della condizione. Ad esempio, nella stringa di condizione "Ordina per titolo ascendente", la parte di ordinamento è "Ordina per", la parte del valore è "title" e la parte della condizione è "Ascending". Si noti che in questo caso la parte del valore è un attributo di metadati.

Esempio:


```XML
<fragment name = "Sort By">
    <argument name = "value">Title</argument>
    <argument name = "condition">Ascending</argument>
</fragment>
```



Per le stringhe di condizione di questo tipo, nella tabella seguente vengono illustrati i valori e le condizioni possibili.



| Porzione di ordinamento | Valori possibili                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              | Condizioni possibili                              |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| Sort By (Ordina per)      | GenreTitle<br/> Date Added<br/> Classificazione automatica<br/> Classificazione personale<br/> Conteggio riproduzione: totale complessivo<br/> Conteggio riproduzione: totali mattina<br/> Conteggio riproduzione: totali pomeridiani<br/> Conteggio riproduzione: totali serali<br/> Conteggio riproduzione: totali notturni<br/> Conteggio riproduzione: totale giorni feriali<br/> Numero di riscontri: weekend totale<br/> Attore<br/> Sottotitolo<br/> Nome stazione<br/> Channel<br/> Ora broadcast<br/> Responsabile<br/> Anno versione<br/> Writer<br/> Producer<br/> Data di registrazione<br/> Data codificata<br/> Velocità in bit<br/> Protezione<br/> | AscendingDescending<br/> Random (Casuale)<br/> |



 

Quando si usa un elemento Fragment per ordinare una playlist, è necessario ordinare in un attributo di metadati che si applica al tipo di elementi multimediali da ordinare. Se, ad esempio, si ordinano elementi di musica non è possibile ordinare l'attore. La tabella seguente illustra gli attributi di metadati che è possibile usare per ordinare i tipi di supporto.



| Tipo di supporto  | Attributi di metadati possibili                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Musica       | GenreTitle<br/> Date Added<br/> Classificazione automatica<br/> Classificazione personale<br/> Conteggio riproduzione: totale complessivo<br/> Conteggio riproduzione: totali mattina<br/> Conteggio riproduzione: totali pomeridiani<br/> Conteggio riproduzione: totali serali<br/> Conteggio riproduzione: totali notturni<br/> Conteggio riproduzione: totale giorni feriali<br/> Numero di riscontri: weekend totale<br/>                                                                                                                                                                                                                                                                                            |
| Video o TV | GenreActor<br/> Sottotitolo<br/> Titolo<br/> Date Added<br/> Classificazione automatica<br/> Nome stazione<br/> Channel<br/> Ora broadcast<br/> Responsabile<br/> Anno versione<br/> Writer<br/> Producer<br/> Data di registrazione<br/> Data codificata<br/> Velocità in bit<br/> Classificazione personale<br/> Protezione<br/> Conteggio riproduzione: totale complessivo<br/> Conteggio riproduzione: totali mattina<br/> Conteggio riproduzione: totali pomeridiani<br/> Conteggio riproduzione: totali serali<br/> Conteggio riproduzione: totali notturni<br/> Conteggio riproduzione: totale giorni feriali<br/> Numero di riscontri: weekend totale<br/> |
| Pulsante di opzione       | TitleDate aggiunto<br/> Velocità in bit<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Foto       | Titolo                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Altro       | GenreTitle<br/> Date Added<br/> Classificazione automatica<br/> Classificazione personale<br/> Velocità in bit<br/> Conteggio riproduzione: totale complessivo<br/> Conteggio riproduzione: totali mattina<br/> Conteggio riproduzione: totali pomeridiani<br/> Conteggio riproduzione: totali serali<br/> Conteggio riproduzione: totali notturni<br/> Conteggio riproduzione: totale giorni feriali<br/> Numero di riscontri: weekend totale<br/>                                                                                                                                                                                                                                                                    |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento argument**](argument-element.md)
</dt> <dt>

[**Filter-elemento**](filter-element.md)
</dt> <dt>

[**Elemento sourceFilter**](sourcefilter-element.md)
</dt> <dt>

[**Riferimento agli elementi della playlist Windows Media**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





