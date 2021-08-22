---
description: La tabella Condizione può essere usata per modificare lo stato di selezione di qualsiasi voce nella tabella Funzionalità in base a un'espressione condizionale.
ms.assetid: 8e2d7c8d-5734-49aa-ad29-16d4d32cccb4
title: Tabella delle condizioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09d9ccb265d69f99a58e155657a0e9d058ba61a920088184ec2b67c3e4506a0b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926961"
---
# <a name="condition-table"></a>Tabella delle condizioni

La tabella Condizione può essere usata per modificare lo stato di selezione di qualsiasi voce nella [tabella Funzionalità](feature-table.md) in base a un'espressione condizionale.

La tabella Condizione include le colonne seguenti.



| Colonna    | Tipo                         | Chiave | Nullable |
|-----------|------------------------------|-----|----------|
| Funzionalità\_ | [Identificatore](identifier.md) | S   | N        |
| Level     | [Integer](integer.md)       | S   | N        |
| Condition | [Condition](condition.md)   | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Funzionalità\_
</dt> <dd>

Chiave esterna nella colonna uno della tabella Funzionalità.

</dd> <dt>

<span id="Level"></span><span id="level"></span><span id="LEVEL"></span>Livello
</dt> <dd>

Livello di installazione condizionale per la funzionalità nella colonna \_ Funzionalità di questa tabella. Il programma di installazione imposta il livello di installazione di questa funzionalità sul livello specificato in questa colonna se l'espressione nella colonna Condizione restituisce TRUE.

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condizione
</dt> <dd>

Se questa espressione condizionale restituisce TRUE, la colonna Level nella tabella Feature viene impostata sul livello di installazione condizionale.

L'espressione nella colonna Condizione non deve contenere riferimenti allo stato installato di alcuna funzionalità o componente. Ciò è dovuto al fatto che le espressioni nella colonna Condizione vengono valutate prima che il programma di installazione valuti gli stati installati di funzionalità e componenti. Qualsiasi espressione nella tabella Condition che tenta di controllare lo stato installato di una funzionalità o di un componente restituisce sempre false.

Per informazioni sulla sintassi delle istruzioni condizionali, vedere [Sintassi delle istruzioni condizionali](conditional-statement-syntax.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

Una funzionalità può essere disabilitata in modo permanente impostando la colonna Livello su 0.

Il livello può essere impostato in base a qualsiasi istruzione condizionale, ad esempio un test per la piattaforma, il sistema operativo o un'impostazione di proprietà specifica.

È consigliabile scegliere con attenzione le condizioni in modo che una funzionalità non sia abilitata durante l'installazione e quindi disabilitata durante la disinstallazione. In questo modo la funzionalità sarà orfana e il prodotto non potrà essere disinstallato.

Questa tabella viene indicata quando viene eseguita [l'azione CostFinalize.](costfinalize-action.md)

Se la [**proprietà Preselezionata**](preselected.md) è stata impostata su 1, il programma di installazione non valuta la tabella Condizione. La tabella Condizione influisce solo sull'installazione delle funzionalità quando non è stata impostata nessuna delle proprietà seguenti:

<dl>

[**ADDLOCAL**](addlocal.md)  
[**Rimuovere**](remove.md)  
[**ADDSOURCE**](addsource.md)  
[**ADDDEFAULT**](adddefault.md)  
[**REINSTALL**](reinstall.md)  
[**Pubblicizzare**](advertise.md)  
[**COMPADDLOCAL**](compaddlocal.md)  
[**COMPADDSOURCE**](compaddsource.md)  
[**COMPADDDEFAULT**](compadddefault.md)  
[**FILEADDLOCAL**](fileaddlocal.md)  
[**FILEADDSOURCE**](fileaddsource.md)  
[**FILEADDDEFAULT**](fileadddefault.md)  
</dl>

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE79](ice79.md)  
[ICE86](ice86.md)  
</dl>

 

 



