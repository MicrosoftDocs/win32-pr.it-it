---
description: ICE79 convalida i riferimenti ai componenti e alle funzionalità immessi nei campi del database usando il tipo di dati Condizione.
ms.assetid: f0a8ceac-084a-4693-b27d-f610eec4702a
title: ICE79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f11ab5bcf0cd538005a5188559b0426e27004cb5a6d043852be3e361d10e509
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119821571"
---
# <a name="ice79"></a>ICE79

ICE79 convalida i riferimenti ai componenti e alle funzionalità immessi nei campi del database usando il [tipo di dati](condition.md) Condizione.

## <a name="result"></a>Risultato

ICE79 invia due avvisi.



| Avviso ICE79                                                                      | Descrizione                                                      |
|------------------------------------------------------------------------------------|------------------------------------------------------------------|
| Tabella di convalida \_ mancante nel database. Impossibile controllare completamente i nomi delle proprietà. | Nel database manca la [ \_ tabella di convalida](-validation-table.md). |
| Errore durante il recupero dei valori dalla \[ colonna 2 \] nella tabella \[ \] 1. Colonna ignorata.         | Errore durante il recupero del valore.                                          |



 

ICE79 invia due errori.



| Errore ICE79                                                          | Descrizione                               |
|----------------------------------------------------------------------|-------------------------------------------|
| Riferimento al componente '%ls' nella colonna '%s'. %s' della riga %s non è valido. | È stato trovato un riferimento al componente non valido. |
| Alla funzionalità '%ls' viene fatto riferimento nella colonna '%s'. %s' della riga %s non è valido.   | È stato trovato un riferimento alla funzionalità non valido    |



 

## <a name="example"></a>Esempio

Ice79 segnala gli errori seguenti per l'esempio:

``` syntax
Component 'NoSuchComponent' referenced in column 
'InstallExecuteSequence'.'Condition' of row Custom2 is invalid.
Feature 'NoSuchFeature' referenced in column 
'InstallExecuteSequence'.'Condition' of row Custom1 is invalid.
```

In questo esempio NoSuchComponent è assente dalla tabella [Component](component-table.md) e NoSuchFeature è assente dalla [tabella Feature](feature-table.md).

[Tabella InstallExecuteSequence](installexecutesequence-table.md) (parziale)



| Azione  | Condition                                |
|---------|------------------------------------------|
| Personalizzato1 | TESTACTION=1046 AND &NoSuchFeature>2  |
| Personalizzato2 | TESTACTION=146 AND $NoSuchComponent>2 |



 

Per correggere questi errori, immettere i record validi per NoSuchFeature e NoSuchComponent nelle tabelle Funzionalità e Componente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 



