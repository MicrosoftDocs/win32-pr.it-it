---
title: Elemento fragment
description: L'elemento fragment specifica una condizione della query che seleziona gli elementi dalla libreria. Le condizioni vengono specificate dalle stringhe di condizione. Una stringa di condizione include in genere una parte del nome, una parte della condizione e una parte di valore.
ms.assetid: 1575318f-8527-42ba-9c2f-9993a60987d7
keywords:
- Elemento fragment Windows Media Player
topic_type:
- apiref
api_name:
- fragment Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1010b269302f88f163232bcaf3e37111e5fc219944ff1d141c1189e119bba05a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003701"
---
# <a name="fragment-element"></a>Elemento fragment

**L'elemento** fragment specifica una condizione della query che seleziona gli elementi dalla libreria. Le condizioni vengono specificate dalle stringhe di condizione. Una stringa di condizione include in genere una parte del nome, una parte della condizione e una parte di valore.

``` syntax
<fragment
    name = "string"
>
</fragment>
```

## <a name="attributes"></a>Attributi

<dl> <dt>

<span id="name__required______________"></span><span id="NAME__REQUIRED______________"></span>**name** (obbligatorio) 
</dt> <dd>

Parte di una stringa di condizione. Vedere la sezione Osservazioni.

</dd> </dl>

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia | Elementi                                                               |
|-----------|------------------------------------------------------------------------|
| Padre    | [filter](filter-element.md), [sourceFilter](sourcefilter-element.md) |
| Figlio     | [argument](argument-element.md)                                       |



 

## <a name="remarks"></a>Commenti

Alcune stringhe di condizione hanno una parte dell'attributo dei metadati, una parte della condizione e una parte di valore. Ad esempio, nella stringa di condizione "Album Artist Is Joe", la parte dell'attributo dei metadati è "Album Artist", la parte della condizione è "Is" e la parte del valore è "Joe".

Esempio:


```XML
<fragment name = "Album Artist">
    <argument name = "condition">Is</argument>
    <argument name = "value">Joe</argument>
</fragment>
```



Per le stringhe di condizione di questo tipo, la tabella seguente illustra i possibili attributi dei metadati, le possibili condizioni e i valori possibili:



| Attributo dei metadati                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | Possibili condizioni                                                                                             | Valori possibili                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ActorAlbum Artist<br/> Titolo album<br/> Autore<br/> Didascalia<br/> Canale<br/> Composer<br/> Conduttore<br/> Provider di contenuti<br/> Genere del provider di contenuti<br/> Contributi dell'artista<br/> Testo sul copyright<br/> Responsabile<br/> Episodio<br/> Tipo di file<br/> Genre<br/> Chiave<br/> Parole chiave<br/> Linguaggio<br/> Umore<br/> Classificazione dei genitori<br/> Periodo<br/> Producer<br/> Provider<br/> Publisher<br/> Serie<br/> Nome stazione<br/> Sottogenere<br/> Sottotitolo<br/> Titolo<br/> Writer<br/> | Uguale a Non è uguale a<br/> È<br/> Non è<br/> Contiene<br/> Non contiene<br/> | Qualsiasi valore di stringa                                                                                                                                                                                                                                                                                                  |
| Velocità in bit (in kilobyte al secondo).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | Uguale a Non è uguale a<br/> È<br/> Non è<br/> Contiene<br/> Non contiene<br/> | 4864<br/> 96<br/> 128<br/> 160<br/> 192<br/> 256<br/> 300<br/> 500<br/> 750<br/> 1000<br/> 1500<br/> 3000<br/> 4500<br/> 6000<br/> 7500<br/>                                                                            |
| Tipo di supporto secondario                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | Uguale a Non è uguale a<br/> È<br/> Non è<br/> Contiene<br/> Non contiene<br/> | Audio: NewsAudio: Talk Show<br/> Audio: audiolili<br/> Audio: Audio Spoken Word<br/> Video: Notizie<br/> Video: Talk Show<br/> Video: Home Video<br/> Video: Film/Film<br/> Video: Serie TV<br/> Video: Video aziendale<br/> Video: Musica Video<br/> |
| Dimensioni file (in KB)Altezza immagine<br/> Larghezza immagine<br/> Play Count : Totals totals (Conteggio play: totali totali totali)<br/> Play Count : Evening Totals<br/> Play Count : Morning Totals<br/> Play Count : Night Totals<br/> Play Count (Conteggio play): totale complessivo<br/> Play Count :Total Weekday<br/> Play Count (Conteggio play): Total Weekend (Fine settimana totale)<br/>                                                                                                                                                                                                                                                                                                                  | è minore diIs maggiore di<br/> È<br/> Non è<br/>                                          | Qualsiasi numero                                                                                                                                                                                                                                                                                                        |
| Broadcast timeDate Encoded<br/> Data registrazione<br/> Data di inizio<br/> Anno di rilascio<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | è beforeIs after<br/> È<br/> Non è<br/>                                                    | YesterdayLast week<br/> Ultimo mese<br/> 6 mesi<br/> 1 anno<br/> 2 anni<br/> 5 anni<br/> Anni 2000<br/> Anni '90<br/> Anni '80<br/> Anni '70<br/> Anni '60<br/> Anni '50<br/> Anni '40<br/>                                                            |
| Date Added                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | è beforeIs after<br/> È<br/> Non è<br/>                                                    | YesterdayLast week<br/> Ultimo mese<br/> 6 mesi<br/> 1 anno<br/> 2 anni<br/> 5 anni<br/>                                                                                                                                                                                   |
| Data ultima riproduzione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               | Più recente di<br/> È<br/> Non è<br/>                                           | YesterdayLast week<br/> Ultimo mese<br/> 6 mesi<br/> 1 anno<br/> 2 anni<br/> 5 anni<br/>                                                                                                                                                                                   |
| Mese di inizio                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | È precedente A È più recente di<br/> È<br/> Non è<br/>                                         | 12<br/> 3<br/> 4<br/> 5<br/> 6<br/> 7<br/> 8<br/> 9<br/> 10<br/> 11<br/> 12<br/> 13<br/>                                                                                                                                                  |
| Anno impiegato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | È precedente A È più recente di<br/> È<br/> Non è<br/>                                         | Qualsiasi anno                                                                                                                                                                                                                                                                                                          |
| Classificazione automatica RatingMy Rating<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                | Is At LeastIs No More Than<br/> È<br/> Non è<br/>                                           | Stella non riclassata1<br/> 2 stelle<br/> 3 stelle<br/> 4 stelle<br/> 5 stelle<br/>                                                                                                                                                                                                              |
| Campo personalizzato \# 1Campo personalizzato \# 2<br/> File Name<br/> Campi chiave<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         | ContainsDoes Not Contain<br/>                                                                             | Qualsiasi stringa                                                                                                                                                                                                                                                                                                        |



 

Alcune stringhe di condizione hanno una parte del limitatore, una parte numerica e una parte di formato. Ad esempio, nella stringa di condizione "Limit Total Size To 3 Megabytes", la parte del limitatore è "Limit Total Size To", la parte numerica è "3" e la parte del formato è "Megabyte".

Esempio:


```XML
<fragment name = "Limit Total Size To">
  <argument name = "number">3</argument>
  <argument name = "format">Megabytes</argument>
</fragment>
```



Per le stringhe di condizione di questo tipo, la tabella seguente mostra i possibili limitatori e formati.



| Limitatore                 | Numeri possibili | Formati possibili                |
|-------------------------|------------------|---------------------------------|
| Limita dimensioni totali a     | Qualsiasi numero       | Kilobyte, Megabyte, Gigabyte |
| Limita durata totale a | Qualsiasi numero       | Secondi, minuti, ore, giorni   |



 

Alcune stringhe di condizione hanno una parte del limitatore e una parte numerica. Ad esempio, nella stringa di condizione "Limita il numero di elementi a 25", la parte del limitatore è "Numero limite di elementi" e la parte relativa al numero è "25".

Esempio:


```XML
<fragment name = "Limit Number of Items">
    <argument name = "number">25</argument>
</fragment>
```



Per le stringhe di condizione di questo tipo, la tabella seguente mostra l'unico limitatore possibile.



| Limitatore               | Numeri possibili |
|-----------------------|------------------|
| Limita numero di elementi | Qualsiasi numero       |



 

Alcune stringhe di condizione hanno una parte di protezione e una parte di condizione. Ad esempio, nella stringa della condizione "Protezione è presente", la parte relativa alla protezione è "Protezione" e la parte relativa alla condizione è "Is".

Esempio:


```XML
<fragment name = "Protection">
    <argument name = "condition">Is</argument>
</fragment>
```



Per le stringhe di condizione di questo tipo, la tabella seguente illustra le possibili condizioni.



| Parte relativa alla protezione | Condizioni possibili             |
|--------------------|---------------------------------|
| Protezione         | È<br/> Non è<br/> |



 

Esiste un tipo di elemento **frammento** che non contiene una stringa di condizione. Se l'attributo name di un **elemento di** frammento è "Randomize Playback Order" l'elemento **fragment** non contiene **elementi argomento.** Questo **elemento frammento** indica al giocatore di riprodurre l'elenco in ordine casuale.

Esempio:


```XML
<fragment name = "Randomize Playback Order">
</fragment>
```



Alcune stringhe di condizione hanno una parte di ordinamento, una parte di valore e una parte di condizione. Ad esempio, nella stringa di condizione "Sort By Title Ascending order", la parte di ordinamento è "Sort By", la parte del valore è "Title" e la parte della condizione è "Ascending". Si noti che in questo caso la parte del valore è un attributo di metadati.

Esempio:


```XML
<fragment name = "Sort By">
    <argument name = "value">Title</argument>
    <argument name = "condition">Ascending</argument>
</fragment>
```



Per le stringhe di condizione di questo tipo, la tabella seguente mostra i valori e le condizioni possibili.



| Parte dell'ordinamento | Valori possibili                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              | Condizioni possibili                              |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| Sort By (Ordina per)      | GenreTitle<br/> Date Added<br/> Classificazione automatica<br/> Valutazione personale<br/> Conteggio di riproduzione: totale complessivo<br/> Conteggio di riproduzione: totali del mattino<br/> Conteggio di riproduzione: totali pomeridiano<br/> Conteggio di riproduzione: totali serali<br/> Conteggio di riproduzione: totali notturni<br/> Conteggio di riproduzione: totale giorno della settimana<br/> Conteggio di riproduzione: fine settimana totale<br/> Attore<br/> Sottotitolo<br/> Nome stazione<br/> Canale<br/> Ora di trasmissione<br/> Responsabile<br/> Anno di rilascio<br/> Writer<br/> Producer<br/> Data registrata<br/> Data codificata<br/> Velocità in bit<br/> Protezione<br/> | Crescente Decrescente<br/> Casuale<br/> |



 

Quando si usa un elemento frammento per ordinare una playlist, è necessario ordinare in base a un attributo di metadati applicabile al tipo di elementi multimediali da ordinare. Ad esempio, se si ordinano elementi musicali, non è possibile ordinare in base a Actor. La tabella seguente illustra gli attributi dei metadati che è possibile usare per ordinare i tipi di supporti.



| Tipo di supporto  | Attributi di metadati possibili                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Musica       | GenreTitle<br/> Date Added<br/> Classificazione automatica<br/> Valutazione personale<br/> Conteggio di riproduzione: totale complessivo<br/> Conteggio di riproduzione: totali del mattino<br/> Conteggio di riproduzione :Totali pomeridiano<br/> Conteggio di riproduzione :Totali serali<br/> Conteggio di riproduzione : Totali notturni<br/> Numero di riproduzione :Total Weekday<br/> Conteggio di riproduzione: fine settimana totale<br/>                                                                                                                                                                                                                                                                                            |
| Video o TV | GenreActor<br/> Sottotitolo<br/> Titolo<br/> Date Added<br/> Classificazione automatica<br/> Nome stazione<br/> Canale<br/> Ora di trasmissione<br/> Responsabile<br/> Anno di rilascio<br/> Writer<br/> Producer<br/> Data registrata<br/> Data codificata<br/> Velocità in bit<br/> Valutazione personale<br/> Protezione<br/> Conteggio di riproduzione: totale complessivo<br/> Conteggio di riproduzione: totali del mattino<br/> Conteggio di riproduzione: totali pomeridiano<br/> Conteggio di riproduzione: totali serali<br/> Conteggio di riproduzione: totali notturni<br/> Conteggio di riproduzione: totale giorno della settimana<br/> Conteggio di riproduzione: fine settimana totale<br/> |
| Pulsante di opzione       | TitleDate Added<br/> Velocità in bit<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Foto       | Titolo                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Altro       | GenreTitle<br/> Date Added<br/> Classificazione automatica<br/> Valutazione personale<br/> Velocità in bit<br/> Play Count (Conteggio play): totale complessivo<br/> Play Count : Morning Totals<br/> Play Count : Afternoon Totals<br/> Play Count : Evening Totals<br/> Play Count : Night Totals<br/> Play Count :Total Weekday<br/> Play Count (Conteggio play): Total Weekend (Fine settimana totale)<br/>                                                                                                                                                                                                                                                                    |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successive<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento argument**](argument-element.md)
</dt> <dt>

[**Elemento filter**](filter-element.md)
</dt> <dt>

[**Elemento sourceFilter**](sourcefilter-element.md)
</dt> <dt>

[**Windows Informazioni di riferimento per gli elementi della playlist multimediale**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





