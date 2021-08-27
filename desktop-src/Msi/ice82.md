---
description: ICE82 verifica che le azioni RegisterProduct Action, RegisterUser Action, PublishProduct Action e PublishFeatures siano tutte presenti nella tabella InstallExecuteSequence. Il pacchetto viene convalidato se sono presenti tutte le azioni.
ms.assetid: b41a56f9-b57e-4133-ae7d-c51b36bab44f
title: ICE82
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf620bd58ca59315796941c6e8d9d3e4c12cdca9064d2be79058c89201a91bad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105231"
---
# <a name="ice82"></a>ICE82

ICE82 verifica che le azioni [RegisterProduct Action](registerproduct-action.md), [RegisterUser Action](registeruser-action.md), [PublishProduct Action](publishproduct-action.md)e [PublishFeatures Action](publishfeatures-action.md) siano tutte presenti nella tabella [InstallExecuteSequence](installexecutesequence-table.md). Il pacchetto viene convalidato se sono presenti tutte le azioni.

ICE82 invia un avviso se sono presenti due azioni con lo stesso numero di sequenza elencate nelle tabelle InstallExecuteSequence, InstallUISequence, AdminExecuteSequence, AdminUISequence o AdvtExecuteSequence .

## <a name="result"></a>Risultato

ICE82 invia gli avvisi seguenti.



| Avviso ICE82                                                                                                                                                                                                                 | Descrizione                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| La tabella InstallExecuteSequence non contiene il set di azioni indicato di seguito: Azioni mancanti:<br/> Funzionalità di pubblicazione<br/> Pubblicare il prodotto<br/> Registrare il prodotto<br/> Registrare l'utente<br/> | L'azione personalizzata ICE82 invia un avviso se tutte e quattro le azioni sono assenti.                                                                                                                                         |
| Questa azione \[ 1 \] ha il numero di sequenza \[ 2 \] duplicato nella tabella \[ \] 3.                                                                                                                                                     | ICE82 invia un avviso se sono presenti due azioni con lo stesso numero di sequenza elencate nelle tabelle InstallExecuteSequence, InstallUISequence, AdminExecuteSequence, AdminUISequence o AdvtExecuteSequence. |



 

ICE82 registra gli errori seguenti.



| Errore ICE82                                                                                                                                                                                                                                        | Descrizione                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| InstallExecuteSequence deve contenere tutte le azioni indicate di seguito o nessuna delle azioni presenti<br/> <List of actions present> <br/> Azioni mancanti:<br/> <List of actions missing> <br/> | ICE82 invia un errore se alcune delle quattro azioni sono presenti e altre sono assenti. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 




