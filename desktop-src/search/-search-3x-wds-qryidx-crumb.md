---
description: L'argomento briciolo supporta le istruzioni complete AQS (Advanced Query Syntax) ed è particolarmente utile come mezzo per controllare l'ambito di una ricerca.
ms.assetid: b0b974ae-0573-45e4-888e-07138604b62e
title: Argomento BRICIOLo (ricerca di Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51f36764174e0eecaedee4a9c360bb9d7dabca3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128595"
---
# <a name="crumb-argument-windows-search"></a>Argomento BRICIOLo (ricerca di Windows)

L' `crumb` argomento supporta le istruzioni complete AQS (Advanced Query Syntax) ed è particolarmente utile come mezzo per controllare l'ambito di una ricerca. Oltre a AQS ements, l' `crumb` argomento può assumere un parametro speciale `location` in Windows Vista e i `kind` `store` parametri e in XP, come descritto più avanti in questo argomento.

Questo argomento è organizzato nel modo seguente:

-   [Sintassi briciola](#crumb-syntax)
    -   [Esempi generali](#general-examples)
-   [Uso di briciole con vista (percorso)](#using-crumb-with-vista-location)
    -   [Esempi di vista](#vista-examples)
    -   [Costanti per le cartelle comuni](#constants-for-common-folders)
-   [Uso di briciole con Windows XP (Kind e Store)](#using-crumb-with-windows-xp-kind-and-store)
    -   [Esempi di XP](#xp-examples)
-   [Argomenti correlati](#related-topics)

 

## <a name="crumb-syntax"></a>Sintassi briciola

La sintassi della briciola è la seguente:


```
crumb=<column>:<value>[,<label>][,<column>:<value>[,<label>]]& 
```



La <column> parte è qualsiasi proprietà nel sistema di proprietà e il <value> parte è un valore valido per la proprietà. La <label> parte è un alias facoltativo per la proprietà visualizzata come hint dell'interfaccia utente.

### <a name="general-examples"></a>Esempi generali


```
crumb=System.Author:paolo&
crumb=store:mapi&
crumb=location:c%3a%5cMyVacationPix,Vacation&
```



 

## <a name="using-crumb-with-vista-location"></a>Uso di briciole con vista (percorso)

Nel parametro briciola, Windows Vista supporta AQS completi e anche la `location` proprietà, che dispone di un'implementazione speciale disponibile solo in Windows Vista. È possibile usare una stringa AQS o la `location` proprietà all'interno di un singolo parametro briciolo, ma non entrambi. Se il parametro briciolo include AQS, tutto il resto del parametro briciolo viene ignorato.

La `location` proprietà consente di specificare un percorso per la ricerca. Windows Vista può ignorare l'indicizzatore e attraversare la directory direttamente se il percorso è esterno all'ambito di ricerca per indicizzazione dell'indicizzatore. Di conseguenza, queste ricerche possono risultare più lente delle ricerche che usano l'indicizzatore.

Quando si specifica una `location` proprietà, sono supportati due parametri aggiuntivi e facoltativi:



| Parametro | Valori                  | Descrizione                                                                                                                                                                       |
|-----------|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| inclusione | Includi, Escludi        | Specifica se la query deve includere o escludere elementi da tale percorso. Il valore predefinito è "include". Windows Vista non supporta le esclusioni senza inclusioni. (Vedere l'esempio) |
| ricorsione | ricorsivo, non ricorsivo | Specifica se la ricerca deve rimaledire tutte le sottocartelle a partire dal valore definito nel percorso:<value>. Il valore predefinito è "ricorsivo".                             |



 

Per definire l'ambito di una ricerca usando il protocollo search-ms:, sono disponibili opzioni diverse a seconda della destinazione dell'ambito.

Cartella in un computer locale:

-   Usare AQS (briciole = Folder: <percorso con codifica URL>)
-   Usare l'argomento location (briciole = location: <percorso con codifica URL>)

Cartella in un computer remoto/rete:

-   Usare l'argomento location (briciole = location: <percorso con codifica URL>)

Cartella a cui si accede tramite un gestore di protocollo UNC noto:

-   Usare AQS (briciole = Store: <UNC protocol handler name> )
-   Usare l'argomento location (briciole = location: <percorso con codifica URL>)

### <a name="vista-examples"></a>Esempi di vista


```
search-ms:query=vacation&crumb=location:shell%3aPersonal,include,recursive&

search-ms:crumb=location:c%3a%5cPictures&crumb=location:c%3a%5cPictures%5cDuplicates,,exclude& 

search-ms:crumb=location:c%3a%5cDocuments&crumb=kind:pics&
```



Nel primo esempio viene eseguita una ricerca di "Vacation" a partire dalla posizione shell://Personal (un collegamento speciale alla cartella documenti dell'utente), inclusa la cartella e tutte le sottocartelle. Vedere la tabella seguente.

Nel secondo esempio viene eseguita una ricerca all'interno di C: \\ Immagini, ma non in c: \\ Immagini \\ duplicati.

Il terzo esempio esegue una ricerca all'interno di C: \\ Documents, limitato a file con la proprietà Kind impostata su pics.

### <a name="constants-for-common-folders"></a>Costanti per le cartelle comuni

Windows Vista consente l'utilizzo di valori [KNOWNFOLDERID](/previous-versions//bb762584(v=vs.85)) che forniscono un metodo univoco indipendente dal sistema per identificare le cartelle speciali utilizzate spesso dalle applicazioni, ma che potrebbero non avere lo stesso nome o percorso in un determinato sistema. Ad esempio, la cartella di sistema può essere "C: \\ Windows" in un sistema e "c: \\ WinNT" in un altro. Prima di Windows Vista, venivano usati [CSIDL](/windows/desktop/shell/csidl) .

Usare questi percorsi con questa sintassi:


```
crumb=location:shell%3a<LocationName>&
```



 

## <a name="using-crumb-with-windows-xp-kind-and-store"></a>Uso di briciole con Windows XP (Kind e Store)

Per la ricerca di Windows in Windows XP (WDS 3. x), i termini "Kind" e "Store" di AQS hanno un'implementazione speciale. I valori "Kind" sono gli stessi [valori usati in WDS 2. x](../lwef/-search-2x-wds-perceivedtype.md). I valori "Store" includono quanto segue:

-   MAPI
-   file
-   outlookexpress
-   any

### <a name="xp-examples"></a>Esempi di XP


```
search-ms:query=from:john&crumb=store:outlookexpress,OE%20Mail&
search-ms:query=from:john&crumb=kind:communications&
```



Nel primo esempio vengono restituiti i messaggi di posta elettronica di Microsoft Outlook Express da John con l'etichetta personalizzata "OE Mail". Nel secondo esempio viene eseguita una ricerca di qualsiasi comunicazione da John.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Introduzione con argomenti di Parameter-Value](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[Argomenti dell'identificatore delle impostazioni locali](-search-3x-wds-qryidx-localeidentifiers.md)
</dt> <dt>

[Argomento della sintassi](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[Argomento STACKEDBY](-search-3x-wds-qryidx-stackedby.md)
</dt> <dt>

[Argomento SOTTOQUERY](-search-3x-wds-qryidx-subquery.md)
</dt> </dl>

 

 
