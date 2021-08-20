---
description: Ogni effetto conforme a DXSAS deve definire, come minimo, un singolo parametro di effetto globale con la semantica globale.
ms.assetid: 2112db8d-6a11-451d-a9d2-ac1b3cb2da95
title: Parametro globale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4dc0a1337505cec30960ca12fa91ed692b9de9434e702c3fb03829e89ab46d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118094772"
---
# <a name="global-parameter"></a>Parametro globale

Ogni effetto conforme a DXSAS deve definire, come minimo, un singolo parametro di effetto globale con la semantica globale. Il parametro globale può anche usare una o più annotazioni facoltative. La sintassi è la seguente:


```
int VariableName : SasGlobal
<
    SasVersion 
    [OptionalAnnotations]
>;
```



dove:

-   VariableName è un nome di variabile di stringa di testo ASCII specificato dall'utente.
-   SasGlobal è la parola chiave semantica che identifica questo parametro come parametro DXSAS globale.
-   SasVersion è l'unica annotazione richiesta.
-   OptionalAnnotations può includere quanto segue:
    -   [SasEffectAuthor](#saseffectauthor)
    -   [SasEffectAuthoringSoftware](#saseffectauthoringsoftware)
    -   [SasEffectCategory](#saseffectcategory)
    -   [SasEffectCompany](#saseffectcompany)
    -   [SasEffectDescription](#saseffectdescription)
    -   [SasEffectHelp](#saseffecthelp)
    -   [SasEffectRevision](#saseffectrevision)

## <a name="sasversion"></a>SasVersion

L'unica annotazione richiesta è SasVersion. Viene dichiarato come il seguente:


```
int3 SasVersion = { major, minor, revision };
```



dove:

-   major indica la versione principale di DXSAS. Le versioni principali di DXSAS possono contenere modifiche al set di semantiche e annotazioni definite. La semantica e le annotazioni possono essere aggiunte e rimosse e, in generale, la compatibilità con le versioni precedenti non è garantita.
-   minor indica la versione secondaria della firma di accesso condiviso. Le versioni secondarie di DXSAS possono includere l'aggiunta di nuova semantica o annotazioni. Inoltre, la semantica e le annotazioni possono essere contrassegnate come deprecate nello standard DXSAS. Le annotazioni e la semantica deprecata devono essere ancora supportate dalle applicazioni host, ma possono generare un avviso diagnostico quando si usa tale semantica o annotazione. Le versioni secondarie sono compatibili con le versioni precedenti.
-   revision indica la revisione DXSAS. Le revisioni di DXSAS esistono solo per correggere bug, rimuovere ambiguità e perfezionare lo standard. Le revisioni dello standard sono compatibili con le versioni precedenti.

La versione corrente è 1.0.0. Non esiste alcun valore predefinito per questa annotazione.

## <a name="saseffectauthor"></a>SasEffectAuthor

In questo modo viene dichiarata la persona che ha creato l'effetto. Viene dichiarato come il seguente:


```
string SasEffectAuthor = "value";
```



dove value è una stringa che identifica l'autore dell'effetto. Il valore predefinito è una stringa vuota.

## <a name="saseffectauthoringsoftware"></a>SasEffectAuthoringSoftware

In questo modo viene dichiarato il software su cui è stato creato l'effetto. Viene dichiarato come il seguente:


```
string SasEffectAuthoringSoftware = "value";
```



dove value è una stringa che identifica il software di creazione dell'effetto. Il valore predefinito è una stringa vuota.

## <a name="saseffectcategory"></a>SasEffectCategory

In questo modo viene dichiarata la categoria dell'effetto. Viene dichiarato come il seguente:


```
string SasEffectCategory = "value";
```



dove value è una stringa che identifica la categoria dell'effetto. Il valore predefinito è una stringa vuota. La categoria viene espressa tramite un valore simile al percorso usando la barra come delimitatore. Gli effetti possono appartenere a una sola categoria perché non esiste alcuna sintassi per esprimere l'inclusione in più percorsi all'interno di un singolo valore SasEffectCategory. Il valore di questa annotazione non viene considerato come con distinzione tra maiuscole e minuscole dall'applicazione host.

## <a name="saseffectcompany"></a>SasEffectCompany

In questo modo viene dichiarata la società che ha creato l'effetto. Viene dichiarato come il seguente:


```
string SasEffectCompany = "value";
```



dove value è una stringa che identifica il nome della società proprietaria dell'effetto. Il valore predefinito è una stringa vuota.

## <a name="saseffectdescription"></a>SasEffectDescription

Descrive l'effetto. Viene dichiarato come il seguente:


```
string SasEffectDescription = "value";
```



dove value è una stringa che descrive l'effetto. Il valore predefinito è una stringa vuota.

## <a name="saseffecthelp"></a>SasEffectHelp

Si tratta di una stringa della Guida che può essere visualizzata all'utente ogni volta che viene richiesta la Guida sull'effetto associato. Viene dichiarato come il seguente:


```
string SasEffectHelp = "value";
```



dove value è una stringa che può essere visualizzata se l'utente richiede assistenza. Il valore predefinito è una stringa vuota.

## <a name="saseffectrevision"></a>SasEffectRevision

Questa annotazione consente agli strumenti e agli utenti di registrare il numero di revisione del file dell'effetto associato. Ad esempio, gli utenti possono inserire parole chiave appropriate nel valore di questa annotazione per richiamare la sostituzione delle parole chiave nel software di controllo delle revisioni preferito. Viene dichiarato come il seguente:


```
string SasEffectRevision = "value";
```



dove value è una stringa che identifica la revisione dell'effetto. Il valore predefinito è una stringa vuota.

## <a name="examples"></a>Esempio

Di seguito è riportato un esempio che usa solo l'annotazione singola richiesta:


```
int gp : SasGlobal
<
  int3 SasVersion = {1,0,0};
>;
```



Di seguito è riportato un esempio che usa l'annotazione obbligatoria e diverse annotazioni facoltative:


```
int gp : SasGlobal
<
  int3 SasVersion = {1,0,0};
  string SasEffectAuthor = "Mike's Shader";
  string SasEffectAuthoringSoftware = "fxe 2.5.4";
  string SasEffectCategory = "/surface/procedural/wood";
  string SasEffectCompany = "Microsoft Corporation";
  string SasEffectDescription = "Renders an irridescent surface.";
  string SasEffectHelp = "For more information, see https://somelocation/skin.htm";    
  string SasEffectRevision = "$Revision$";  
>;
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimenti semantici e annotazioni standard DirectX](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



