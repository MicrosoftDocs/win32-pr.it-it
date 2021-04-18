---
description: L'azione CostInitialize avvia il processo di determinazione dei costi di installazione.
ms.assetid: be9a8382-c892-44ae-8b59-c665b5cca2d2
title: Azione CostInitialize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 251bb0ae7508c87cd0af7ab81196c5d739e923a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313815"
---
# <a name="costinitialize-action"></a>Azione CostInitialize

L'azione CostInitialize avvia il processo di [*determinazione dei costi*](c-gly.md) di installazione.

## <a name="sequence-restrictions"></a>Restrizioni sequenza

Tutte le azioni standard o [personalizzate](custom-actions.md) che influiscono sui costi devono essere sequenziate prima dell'azione CostInitialize. Chiamare l'azione [filecost](filecost-action.md) immediatamente dopo l'azione CostInitialize. Chiamare quindi l'azione [CostFinalize secondo](costfinalize-action.md) dopo l'azione CostInitialize azione per rendere disponibili al programma di installazione tutti i calcoli dei costi finali tramite la tabella dei [componenti](component-table.md) .

## <a name="actiondata-messages"></a>Messaggi ActionData

Nessun messaggio ActionData.

## <a name="remarks"></a>Commenti

L'azione CostInitialize carica la tabella dei componenti e la tabella delle [funzionalità](feature-table.md) in memoria.

Per ulteriori informazioni sul processo di [*determinazione dei costi*](c-gly.md) nel programma di installazione, vedere [Costing di file](file-costing.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costo file](file-costing.md)
</dt> </dl>

 

 



