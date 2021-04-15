---
description: L'azione ExecuteAction avvia la sequenza di esecuzione usando la proprietà EXECUTEACTION per determinare il tipo di installazione da eseguire.
ms.assetid: 61878317-ac87-4f6e-9375-12a78969e29e
title: Azione ExecuteAction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2970a0fb4e9297264071769ac7415cd2acf866b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485388"
---
# <a name="executeaction-action"></a>Azione ExecuteAction

L'azione ExecuteAction avvia la sequenza di esecuzione usando la proprietà [**ExecuteAction**](executeaction.md) per determinare il tipo di installazione da eseguire.

## <a name="sequence-restrictions"></a>Restrizioni sequenza

Questa azione deve essere sequenziata dopo il completamento di tutte le raccolte di informazioni necessarie per iniziare l'installazione. Le azioni aggiuntive possono essere sequenziate dopo l'azione ExecuteAction nella [tabella InstallUISequence](installuisequence-table.md)e la [tabella AdminUISequence](adminuisequence-table.md). Una sequenza inizierà in genere con le azioni di [*determinazione del costo*](c-gly.md) , ad esempio l' [azione CostInitialize](costinitialize-action.md), seguita dalle azioni dell'interfaccia utente e quindi dall'azione ExecuteAction.

## <a name="actiondata-messages"></a>Messaggi ActionData

Nessun messaggio ActionData.

## <a name="remarks"></a>Commenti

L'azione ExecuteAction viene eseguita con i privilegi di sistema se il servizio del programma di installazione è abilitato. Le azioni di primo livello, ad esempio l'azione di [installazione](install-action.md), l'azione di [annuncio](advertise-action.md)e l' [azione amministrativa](admin-action.md) includono la logica interna che determina se la chiamata dell'azione ExecuteAction richiede la sequenza di esecuzione o la sequenza dell'interfaccia utente da eseguire.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tabella InstallUISequence](installuisequence-table.md)
</dt> <dt>

[Tabella AdminUISequence](adminuisequence-table.md)
</dt> <dt>

[Azione CostInitialize](costinitialize-action.md)
</dt> </dl>

 

 



