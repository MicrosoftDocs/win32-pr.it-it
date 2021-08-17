---
description: L'azione CostFinalize termina il processo di determinazione costi dell'installazione interna avviato dall'azione CostInitialize.
ms.assetid: ae69ad03-5acc-4a62-ba71-3a4e477d34ab
title: Azione CostFinalize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24f6b8fb49218925d3f517a9d198a638bc9dff5a1184beef24a487de0112830f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118638355"
---
# <a name="costfinalize-action"></a>Azione CostFinalize

L'azione CostFinalize termina il processo di determinazione costi [*dell'installazione*](c-gly.md) interna avviato [dall'azione CostInitialize.](costinitialize-action.md)

## <a name="sequence-restrictions"></a>Restrizioni di sequenza

Tutte le azioni standard [o personalizzate che](custom-actions.md) influiscono sulla determinazione dei costi devono essere sequenziate prima [dell'azione CostInitialize.](costinitialize-action.md) Chiamare [l'azione FileCost](filecost-action.md) immediatamente dopo l'azione CostInitialize e quindi chiamare l'azione CostFinalize per rendere disponibili tutti i calcoli dei costi finali al programma di installazione tramite la [tabella Component.](component-table.md)

L'azione CostFinalize deve essere eseguita prima di avviare qualsiasi [](feature-table.md) sequenza dell'interfaccia utente che consenta all'utente di visualizzare o modificare le selezioni o le directory delle tabelle delle funzionalità.

## <a name="actiondata-messages"></a>Messaggi ActionData

Non sono presenti messaggi ActionData.

## <a name="remarks"></a>Commenti

L'azione CostFinalize esegue una query [nella tabella Condizione](condition-table.md) per determinare le funzionalità pianificate per l'installazione. La determinazione dei costi viene eseguita per ogni componente nella [tabella](component-table.md) Componente.

L'azione CostFinalize verifica anche che tutte le directory di destinazione siano scrivibili prima di consentire la continuazione dell'installazione.

> [!Note]  
> Durante [un'installazione amministrativa,](administrative-installation.md)CostFinalize imposta tutte le funzionalità per l'installazione, ad eccezione delle funzionalità con 0 creato nella colonna Livello della [tabella Funzionalità](feature-table.md).

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Determinazione dei costi dei file](file-costing.md)
</dt> </dl>

 

 



