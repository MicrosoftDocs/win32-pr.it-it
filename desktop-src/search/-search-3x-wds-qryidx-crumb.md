---
description: Informazioni su come usare l'argomento CRUMB Windows Search come mezzo per controllare l'ambito di una ricerca.
ms.assetid: b0b974ae-0573-45e4-888e-07138604b62e
title: Argomento CRUMB (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f56287c7182c0cf370250d53075a1c951ddf28b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403734"
---
# <a name="crumb-argument-windows-search"></a>Argomento CRUMB (Windows Search)

L'argomento supporta istruzioni AQS (Advanced Query Syntax) complete ed è particolarmente utile per controllare `crumb` l'ambito di una ricerca. Oltre agli argomenti AQS, l'argomento può assumere un parametro speciale in Windows Vista e i parametri e in XP, come descritto `crumb` più avanti in questo `location` `kind` `store` argomento.

Questo argomento è organizzato come segue:

-   [Sintassi crumb](#crumb-syntax)
    -   [Esempi generali](#general-examples)
-   [Uso di crumb con Vista (posizione)](#using-crumb-with-vista-location)
    -   [Esempi di Vista](#vista-examples)
    -   [Costanti per cartelle comuni](#constants-for-common-folders)
-   [Uso di crumb con Windows XP (tipo e archivio)](#using-crumb-with-windows-xp-kind-and-store)
    -   [Esempi di XP](#xp-examples)
-   [Argomenti correlati](#related-topics)

 

## <a name="crumb-syntax"></a>Sintassi crumb

La sintassi di base è la seguente:


```
crumb=<column>:<value>[,<label>][,<column>:<value>[,<label>]]& 
```



La <column> parte è qualsiasi proprietà nel sistema di proprietà e <value> portion è un valore valido per tale proprietà. La <label> parte è un alias facoltativo per la proprietà visualizzata come suggerimento dell'interfaccia utente.

### <a name="general-examples"></a>Esempi generali


```
crumb=System.Author:paolo&
crumb=store:mapi&
crumb=location:c%3a%5cMyVacationPix,Vacation&
```



 

## <a name="using-crumb-with-vista-location"></a>Uso di crumb con Vista (posizione)

Nel parametro crumb Windows Vista supporta AQS completo e anche la proprietà , che ha un'implementazione speciale `location` disponibile solo in Windows Vista. È possibile usare una stringa AQS o la proprietà `location` all'interno di un singolo parametro crumb, ma non entrambi. Se il parametro crumb include AQS, tutti gli altri elementi nel parametro crumb vengono ignorati.

La `location` proprietà consente di specificare un percorso in cui eseguire la ricerca. Windows Vista può ignorare l'indicizzatore e attraversare direttamente la directory se il percorso non rientra nell'ambito della ricerca per indicizzazione dell'indicizzatore. Di conseguenza, queste ricerche possono essere più lente delle ricerche che usano l'indicizzatore.

Quando si specifica una `location` proprietà, sono supportati due parametri aggiuntivi e facoltativi:



| Parametro | Valori                  | Descrizione                                                                                                                                                                       |
|-----------|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Inclusione | include, exclude        | Specifica se la query deve includere o escludere elementi da tale percorso. L'impostazione predefinita è "Include". Windows Vista non supporta le esclusioni senza inclusioni. (Vedere l'esempio) |
| ricorsione | ricorsivo, non ricorsivo | Specifica se la ricerca deve essere ricorsiva di tutte le sottocartelle a partire dal valore definito nel percorso:<value>. L'impostazione predefinita è "Recursive".                             |



 

Per impostare l'ambito di una ricerca usando il protocollo search-ms:, sono disponibili opzioni diverse a seconda della destinazione dell'ambito.

Cartella in un computer locale:

-   Usare AQS (crumb=folder:<percorso con codifica URL>)
-   Usare l'argomento location (crumb=location:<percorso con codifica URL>)

Cartella in un computer/rete remoto:

-   Usare l'argomento location (crumb=location:<percorso con codifica URL>)

Cartella a cui si accede tramite un gestore di protocollo UNC noto:

-   Usare AQS (crumb=store: <UNC protocol handler name> )
-   Usare l'argomento location (crumb=location:<percorso con codifica URL>)

### <a name="vista-examples"></a>Esempi di Vista


```
search-ms:query=vacation&crumb=location:shell%3aPersonal,include,recursive&

search-ms:crumb=location:c%3a%5cPictures&crumb=location:c%3a%5cPictures%5cDuplicates,,exclude& 

search-ms:crumb=location:c%3a%5cDocuments&crumb=kind:pics&
```



Nel primo esempio viene eseguita una ricerca di "vacation" a partire dal percorso shell://Personal (un collegamento speciale alla cartella Documenti dell'utente), incluse tale cartella e tutte le sottocartelle. Vedere la tabella seguente.

Nel secondo esempio viene eseguita una ricerca all'interno di C: \\ Immagini, ma non in C: \\ Immagini \\ duplicate.

Il terzo esempio esegue una ricerca all'interno di C: Documenti, limitata ai file con la proprietà \\ kind impostata su pics.

### <a name="constants-for-common-folders"></a>Costanti per cartelle comuni

Windows Vista consente l'uso di valori [KNOWNFOLDERID](/previous-versions//bb762584(v=vs.85)) che forniscono un modo univoco indipendente dal sistema per identificare le cartelle speciali usate di frequente dalle applicazioni, ma che potrebbero non avere lo stesso nome o percorso in un sistema specificato. Ad esempio, la cartella di sistema può essere "C: Windows" in un \\ sistema e "C: \\ Winnt" in un altro sistema. Nelle versioni precedenti a Windows Vista [venivano usati i CSID.](/windows/desktop/shell/csidl)

Usare queste posizioni con la sintassi seguente:


```
crumb=location:shell%3a<LocationName>&
```



 

## <a name="using-crumb-with-windows-xp-kind-and-store"></a>Uso di crumb con Windows XP (tipo e archivio)

Per Windows Search in Windows XP (WDS 3.x), i termini "kind" e "store" di AQS hanno un'implementazione speciale. I valori "kind" sono gli stessi [usati in WDS 2.x.](../lwef/-search-2x-wds-perceivedtype.md) I valori "store" includono quanto segue:

-   Mapi
-   file
-   outlookexpress
-   any

### <a name="xp-examples"></a>Esempi di XP


```
search-ms:query=from:john&crumb=store:outlookexpress,OE%20Mail&
search-ms:query=from:john&crumb=kind:communications&
```



Nel primo esempio vengono restituiti messaggi di posta elettronica di Microsoft Outlook Express da John con l'etichetta personalizzata "OE Mail". Nel secondo esempio viene eseguita una ricerca di qualsiasi comunicazione da John.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attività iniziali con Parameter-Value argomenti](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[Argomenti dell'identificatore delle impostazioni locali](-search-3x-wds-qryidx-localeidentifiers.md)
</dt> <dt>

[Argomento SYNTAX](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[Argomento STACKEDBY](-search-3x-wds-qryidx-stackedby.md)
</dt> <dt>

[Argomento SUBQUERY](-search-3x-wds-qryidx-subquery.md)
</dt> </dl>

 

 
