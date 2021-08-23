---
description: ICE46 verifica la presenza di proprietà personalizzate in condizioni, testo formattato e altre posizioni che differiscono da una proprietà definita dal sistema solo in base alla distinzione tra maiuscole e minuscole di uno o più caratteri.
ms.assetid: 892d7462-0222-4fa0-b14c-17742a266c0a
title: ICE46
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbe334f973449ffe8bdbba1eb51347576c0b39c6b8eacfb8103970726dbc1ec6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580991"
---
# <a name="ice46"></a>ICE46

ICE46 verifica la presenza di proprietà personalizzate in condizioni, testo formattato e altre posizioni che differiscono da una proprietà definita dal sistema solo in base alla distinzione tra maiuscole e minuscole di uno o più caratteri.

## <a name="result"></a>Risultato

ICE46 invia un messaggio informativo se in una condizione è presente una proprietà personalizzata, un testo formattato e un'altra posizione che differisce da una proprietà definita dal sistema solo nel caso di uno o più caratteri.

## <a name="example"></a>Esempio

ICE46 segnala gli errori seguenti per l'esempio illustrato.



| Errore ICE46                                                                                                                                            | Descrizione                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Property ReinstallMode definito nella tabella delle proprietà differisce da un'altra proprietà definita solo per maiuscole e minuscole.                                                   | Il nome della proprietà definita dal sistema **REINSTALLMODE** differisce dalla proprietà personalizzata solo in base alla distinzione tra maiuscole e minuscole. Per le proprietà viene fatto distinzione tra maiuscole e minuscole, pertanto la proprietà personalizzata non corrisponde alla proprietà di sistema. Si tratta di una causa comune di errori. |
| Proprietà 'Myproperty' a cui viene fatto riferimento nella colonna 'InstallExecuteSequence'. Condition' della riga 'InstallFinalize' differisce da una proprietà definita solo in base alla distinzione tra maiuscole e minuscole. | La tabella delle proprietà definisce la tabella MyProperty, ma la proprietà a cui si fa riferimento è Myproperty. Per le proprietà viene fatto distinzione tra maiuscole e minuscole, quindi le due proprietà NON sono uguali. Si tratta di una causa comune di errori.                          |



 

[Tabella delle proprietà](property-table.md)



| Proprietà      | Valore   |
|---------------|---------|
| ReinstallazioneMode | omus    |
| Myproperty    | un valore |



 

[Tabella InstallExecuteSequence](installexecutesequence-table.md) (parziale)



| Azione          | Condition  |
|-----------------|------------|
| InstallFinalize | Myproperty |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 



