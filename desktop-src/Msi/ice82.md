---
description: ICE82 verifica che l'azione RegisterProduct, l'azione RegisterUser, l'azione PublishProduct e l'azione PublishFeatures siano presenti nella tabella InstallExecuteSequence. Il pacchetto viene convalidato se sono presenti tutte le azioni.
ms.assetid: b41a56f9-b57e-4133-ae7d-c51b36bab44f
title: ICE82
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aa6ba2e0bd07af06bf90c604c333966b5581ba3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758414"
---
# <a name="ice82"></a>ICE82

ICE82 verifica che l'azione [RegisterProduct](registerproduct-action.md), l'azione [RegisterUser](registeruser-action.md), l'azione [PublishProduct](publishproduct-action.md)e l' [azione PublishFeatures](publishfeatures-action.md) siano presenti nella [tabella InstallExecuteSequence](installexecutesequence-table.md). Il pacchetto viene convalidato se sono presenti tutte le azioni.

ICE82 pubblica un avviso se sono presenti due azioni con lo stesso numero di sequenza elencato nelle tabelle InstallExecuteSequence, InstallUISequence, AdminExecuteSequence, AdminUISequence o AdvtExecuteSequence.

## <a name="result"></a>Risultato

ICE82 invia gli avvisi seguenti.



| Avviso di ICE82                                                                                                                                                                                                                 | Descrizione                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| La tabella InstallExecuteSequence non contiene il set di azioni indicato di seguito: azioni mancanti:<br/> Funzionalità di pubblicazione<br/> Pubblica prodotto<br/> Registrare il prodotto<br/> Registra utente<br/> | L'azione personalizzata ICE82 Invia un avviso se tutte e quattro le azioni sono assenti.                                                                                                                                         |
| Questa azione \[ 1 \] presenta il numero di sequenza 2 duplicato \[ \] nella tabella \[ 3 \] .                                                                                                                                                     | ICE82 pubblica un avviso se sono presenti due azioni con lo stesso numero di sequenza elencato nelle tabelle InstallExecuteSequence, InstallUISequence, AdminExecuteSequence, AdminUISequence o AdvtExecuteSequence. |



 

ICE82 invia i seguenti errori.



| Errore ICE82                                                                                                                                                                                                                                        | Descrizione                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| InstallExecuteSequence deve contenere tutte le azioni indicate di seguito oppure nessuna delle azioni presenti<br/> <List of actions present> <br/> Azioni mancanti:<br/> <List of actions missing> <br/> | ICE82 Invia un errore se alcune delle quattro azioni sono presenti e altre sono assenti. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 




