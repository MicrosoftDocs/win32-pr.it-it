---
description: L'azione ExecuteAction avvia la sequenza di esecuzione usando la proprietà EXECUTEACTION per determinare il tipo di installazione da eseguire.
ms.assetid: 61878317-ac87-4f6e-9375-12a78969e29e
title: Azione ExecuteAction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20555af337f8774aec6c58769f2235da97ae763e044665e407a8dc29e75de750
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118636888"
---
# <a name="executeaction-action"></a>Azione ExecuteAction

L'azione ExecuteAction avvia la sequenza di esecuzione usando la [**proprietà EXECUTEACTION**](executeaction.md) per determinare il tipo di installazione da eseguire.

## <a name="sequence-restrictions"></a>Restrizioni relative alle sequenze

Questa azione deve essere sequenziata dopo il completamento di tutte le raccolte di informazioni necessarie per avviare l'installazione. Le azioni aggiuntive possono essere sequenziate dopo l'azione ExecuteAction nella [tabella InstallUISequence](installuisequence-table.md)e nella tabella [AdminUISequence](adminuisequence-table.md). Una sequenza inizia in genere con [*azioni di determinazione*](c-gly.md) costi, ad esempio l'azione [CostInitialize](costinitialize-action.md), seguita dalle azioni dell'interfaccia utente e quindi dall'azione ExecuteAction.

## <a name="actiondata-messages"></a>Messaggi ActionData

Non sono presenti messaggi ActionData.

## <a name="remarks"></a>Commenti

L'azione ExecuteAction viene eseguita con privilegi di sistema se il servizio di installazione è abilitato. Le azioni di primo livello, ad esempio l'azione [INSTALL](install-action.md), l'azione [ADVERTISE](advertise-action.md)e l'azione [ADMIN](admin-action.md) includono la logica interna che determina se la chiamata all'azione ExecuteAction richiede l'esecuzione della sequenza di esecuzione o della sequenza dell'interfaccia utente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tabella InstallUISequence](installuisequence-table.md)
</dt> <dt>

[Tabella AdminUISequence](adminuisequence-table.md)
</dt> <dt>

[Azione CostInitialize](costinitialize-action.md)
</dt> </dl>

 

 



