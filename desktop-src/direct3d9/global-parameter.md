---
description: Ogni effetto conforme a DXSAS deve definire come minimo un singolo parametro di effetto globale con la semantica globale.
ms.assetid: 2112db8d-6a11-451d-a9d2-ac1b3cb2da95
title: Parametro globale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 647ef789e37cd7c8d6cd2fe554f1f8becbfd5e92
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304098"
---
# <a name="global-parameter"></a>Parametro globale

Ogni effetto conforme a DXSAS deve definire come minimo un singolo parametro di effetto globale con la semantica globale. Il parametro Global può inoltre utilizzare una o più annotazioni facoltative. La sintassi è la seguente:


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
-   OptionalAnnotations può includere gli elementi seguenti:
    -   [SasEffectAuthor](#saseffectauthor)
    -   [SasEffectAuthoringSoftware](#saseffectauthoringsoftware)
    -   [SasEffectCategory](#saseffectcategory)
    -   [SasEffectCompany](#saseffectcompany)
    -   [SasEffectDescription](#saseffectdescription)
    -   [SasEffectHelp](#saseffecthelp)
    -   [SasEffectRevision](#saseffectrevision)

## <a name="sasversion"></a>SasVersion

L'unica annotazione richiesta è SasVersion. Viene dichiarata come segue:


```
int3 SasVersion = { major, minor, revision };
```



dove:

-   Major indica la versione principale di DXSAS. Le versioni principali di DXSAS possono contenere modifiche di sweep al set di semantiche e annotazioni definite. La semantica e le annotazioni possono essere aggiunte e rimosse e, in generale, la compatibilità con le versioni precedenti non è garantita.
-   minor indica la versione secondaria di SAS. Le versioni secondarie di DXSAS possono includere l'aggiunta di nuove semantiche o annotazioni. Inoltre, la semantica e le annotazioni possono essere contrassegnate come deprecate nello standard DXSAS. La semantica deprecata e le annotazioni devono essere comunque supportate dalle applicazioni host, ma possono generare un avviso di diagnostica quando viene utilizzata una semantica o un'annotazione. Le versioni secondarie sono compatibili con le versioni precedenti.
-   Revisione indica la revisione DXSAS. Le revisioni di DXSAS esistono solo come mezzo per correggere i bug, rimuovere l'ambiguità e perfezionare lo standard. Le revisioni dello standard sono compatibili con le versioni precedenti.

La versione corrente è 1.0.0. Non esiste alcun valore predefinito per questa annotazione.

## <a name="saseffectauthor"></a>SasEffectAuthor

Viene dichiarata la persona che ha creato l'effetto. Viene dichiarata come segue:


```
string SasEffectAuthor = "value";
```



dove value è una stringa che identifica l'autore dell'effetto. Il valore predefinito è una stringa vuota.

## <a name="saseffectauthoringsoftware"></a>SasEffectAuthoringSoftware

Questo dichiara il software su cui è stato creato l'effetto. Viene dichiarata come segue:


```
string SasEffectAuthoringSoftware = "value";
```



dove value è una stringa che identifica il software di creazione dell'effetto. Il valore predefinito è una stringa vuota.

## <a name="saseffectcategory"></a>SasEffectCategory

Viene dichiarata la categoria Effect. Viene dichiarata come segue:


```
string SasEffectCategory = "value";
```



dove value è una stringa che identifica la categoria dell'effetto. Il valore predefinito è una stringa vuota. La categoria viene espressa tramite un valore simile al percorso usando la barra come delimitatore. Gli effetti possono appartenere solo a una categoria poiché non esiste alcuna sintassi per esprimere l'inclusione in più percorsi all'interno di un singolo valore SasEffectCategory. Il valore di questa annotazione non viene considerato come distinzione tra maiuscole e minuscole dall'applicazione host.

## <a name="saseffectcompany"></a>SasEffectCompany

Viene dichiarata la società che ha creato l'effetto. Viene dichiarata come segue:


```
string SasEffectCompany = "value";
```



dove value è una stringa che identifica il nome della società che possiede l'effetto. Il valore predefinito è una stringa vuota.

## <a name="saseffectdescription"></a>SasEffectDescription

In questo articolo viene descritto l'effetto. Viene dichiarata come segue:


```
string SasEffectDescription = "value";
```



dove value è una stringa che descrive l'effetto. Il valore predefinito è una stringa vuota.

## <a name="saseffecthelp"></a>SasEffectHelp

Si tratta di una stringa della guida che può essere visualizzata all'utente ogni volta che è richiesta la guida sull'effetto associato. Viene dichiarata come segue:


```
string SasEffectHelp = "value";
```



dove value è una stringa che può essere visualizzata se l'utente richiede la guida. Il valore predefinito è una stringa vuota.

## <a name="saseffectrevision"></a>SasEffectRevision

Questa annotazione consente agli strumenti e agli utenti di registrare il numero di revisione del file degli effetti associati. Ad esempio, gli utenti possono inserire parole chiave appropriate nel valore di questa annotazione per richiamare la sostituzione delle parole chiave nel software di controllo delle revisioni preferito. Viene dichiarata come segue:


```
string SasEffectRevision = "value";
```



dove value è una stringa che identifica la revisione dell'effetto. Il valore predefinito è una stringa vuota.

## <a name="examples"></a>Esempio

Di seguito è riportato un esempio che usa solo la singola annotazione obbligatoria:


```
int gp : SasGlobal
<
  int3 SasVersion = {1,0,0};
>;
```



Di seguito è riportato un esempio che usa l'annotazione richiesta e diverse Annotazioni facoltative:


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

[Informazioni di riferimento sulla semantica e le annotazioni standard DirectX](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



