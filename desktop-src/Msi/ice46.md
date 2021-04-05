---
description: ICE46 verifica la presenza di proprietà personalizzate in condizioni, testo formattato e altri percorsi diversi da una proprietà definita dal sistema solo in caso di uno o più caratteri.
ms.assetid: 892d7462-0222-4fa0-b14c-17742a266c0a
title: ICE46
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e24a76560b02a3a0ce3afa681c7ba74fcc7a2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756224"
---
# <a name="ice46"></a>ICE46

ICE46 verifica la presenza di proprietà personalizzate in condizioni, testo formattato e altri percorsi diversi da una proprietà definita dal sistema solo in caso di uno o più caratteri.

## <a name="result"></a>Risultato

ICE46 Invia un messaggio informativo se è presente una proprietà personalizzata in una condizione, in un testo formattato e in un'altra posizione diversa da una proprietà definita dal sistema solo nel caso di uno o più caratteri.

## <a name="example"></a>Esempio

ICE46 segnala gli errori seguenti per l'esempio illustrato.



| Errore ICE46                                                                                                                                            | Descrizione                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| La proprietà ReinstallMode definita nella tabella delle proprietà differisce da un'altra proprietà definita solo per caso.                                                   | Il nome di proprietà definito dal sistema **REINSTALLMODE** differisce dalla proprietà personalizzata solo per caso. Le proprietà fanno distinzione tra maiuscole e minuscole, pertanto la proprietà personalizzata non corrisponde alla proprietà di sistema. Si tratta di una delle cause comuni degli errori. |
| Proprietà' setProperty ' a cui viene fatto riferimento nella colonna ' InstallExecuteSequence '. La condizione ' della riga ' InstallFinalize ' differisce da una proprietà definita solo per caso. | La tabella delle proprietà definisce la proprietà della tabella, ma la proprietà a cui si fa riferimento è SetProperty. Le proprietà fanno distinzione tra maiuscole e minuscole, pertanto le due proprietà non sono uguali. Si tratta di una delle cause comuni degli errori.                          |



 

[Tabella delle proprietà](property-table.md)



| Proprietà      | Valore   |
|---------------|---------|
| ReinstallMode | omus    |
| MyProperty    | valore |



 

[Tabella InstallExecuteSequence](installexecutesequence-table.md) (parziale)



| Azione          | Condizione  |
|-----------------|------------|
| InstallFinalize | MyProperty |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



