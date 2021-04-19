---
description: L'azione CostFinalize secondo termina il processo di determinazione dei costi di installazione interna iniziato dall'azione CostInitialize.
ms.assetid: ae69ad03-5acc-4a62-ba71-3a4e477d34ab
title: Azione CostFinalize secondo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72a5423f1050f9c9d755d33e492b9b65cfcaa08b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317766"
---
# <a name="costfinalize-action"></a>Azione CostFinalize secondo

L'azione CostFinalize secondo termina il processo di [*determinazione dei costi*](c-gly.md) di installazione interna iniziato dall'azione [CostInitialize](costinitialize-action.md) .

## <a name="sequence-restrictions"></a>Restrizioni sequenza

Tutte le azioni standard o [personalizzate](custom-actions.md) che influiscono sui costi devono essere sequenziate prima dell'azione [CostInitialize](costinitialize-action.md) . Chiamare l'azione [filecost](filecost-action.md) immediatamente dopo l'azione CostInitialize, quindi chiamare l'azione CostFinalize secondo per rendere disponibili al programma di installazione tutti i calcoli dei costi finali tramite la tabella [Component](component-table.md) .

È necessario eseguire l'azione CostFinalize secondo prima di avviare qualsiasi sequenza dell'interfaccia utente che consente all'utente di visualizzare o modificare selezioni o directory della tabella delle [funzionalità](feature-table.md) .

## <a name="actiondata-messages"></a>Messaggi ActionData

Nessun messaggio ActionData.

## <a name="remarks"></a>Commenti

L'azione CostFinalize secondo esegue una query sulla tabella [Condition](condition-table.md) per determinare quali funzionalità sono pianificate per l'installazione. Il costo viene eseguito per ogni componente della tabella dei [componenti](component-table.md) .

L'azione CostFinalize secondo verifica anche che tutte le directory di destinazione siano scrivibili prima di consentire l'installazione per continuare.

> [!Note]  
> Durante un' [installazione amministrativa](administrative-installation.md), CostFinalize secondo imposta tutte le funzionalità per l'installazione ad eccezione delle funzionalità con 0 create nella colonna livello della [tabella delle funzionalità](feature-table.md).

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costo file](file-costing.md)
</dt> </dl>

 

 



