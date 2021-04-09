---
description: ICE79 convalida i riferimenti ai componenti e alle funzionalità immessi nei campi del database usando il tipo di dati Condition.
ms.assetid: f0a8ceac-084a-4693-b27d-f610eec4702a
title: ICE79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9081297f2bf2f11283380c0f057bd0fbec417975
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129966"
---
# <a name="ice79"></a>ICE79

ICE79 convalida i riferimenti ai componenti e alle funzionalità immessi nei campi del database usando il tipo di dati [Condition](condition.md) .

## <a name="result"></a>Risultato

ICE79 invia due avvisi.



| Avviso di ICE79                                                                      | Descrizione                                                      |
|------------------------------------------------------------------------------------|------------------------------------------------------------------|
| Nel database manca la \_ tabella di convalida. Non è stato possibile controllare completamente i nomi di proprietà. | Nel database manca la [ \_ tabella di convalida](-validation-table.md). |
| Errore durante il recupero dei valori dalla colonna \[ 2 \] nella tabella \[ 1 \] . Colonna ignorata.         | Errore durante il recupero del valore.                                          |



 

ICE79 invia due errori.



| Errore ICE79                                                          | Descrizione                               |
|----------------------------------------------------------------------|-------------------------------------------|
| Si fa riferimento al componente '% ls ' nella colonna '% s'. % s'della riga% s non è valido. | È stato trovato un riferimento a un componente non valido. |
| Funzione '% ls ' a cui viene fatto riferimento nella colonna '% s'.' % s'della riga% s non è valido.   | È stato trovato un riferimento alla funzionalità non valido    |



 

## <a name="example"></a>Esempio

ICE79 segnala gli errori seguenti per l'esempio:

``` syntax
Component 'NoSuchComponent' referenced in column 
'InstallExecuteSequence'.'Condition' of row Custom2 is invalid.
Feature 'NoSuchFeature' referenced in column 
'InstallExecuteSequence'.'Condition' of row Custom1 is invalid.
```

In questo esempio, NoSuchComponent è assente dalla [tabella Component](component-table.md) e NoSuchFeature è assente dalla [tabella Feature](feature-table.md).

[Tabella InstallExecuteSequence](installexecutesequence-table.md) (parziale)



| Azione  | Condizione                                |
|---------|------------------------------------------|
| Personalizzata1 | TESTACTION = 1046 e &NoSuchFeature>2  |
| Custom2 | TESTACTION = 146 e $NoSuchComponent>2 |



 

Per correggere questi errori, immettere record validi per NoSuchFeature e NoSuchComponent nelle tabelle feature e Component.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



