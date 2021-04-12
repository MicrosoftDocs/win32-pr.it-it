---
description: ICE84 controlla la tabella AdvtExecuteSequence, la tabella AdminExecuteSequence e la tabella InstallExecuteSequence per verificare che le azioni standard seguenti non siano state impostate con le condizioni nel campo condizione.
ms.assetid: 0d1bbf4b-ffab-409e-a292-891dfa823433
title: ICE84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8960f53f5a01e9bec95a02bb3241487aa31aaae5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347776"
---
# <a name="ice84"></a>ICE84

ICE84 controlla la tabella [AdvtExecuteSequence](advtexecutesequence-table.md), la [tabella AdminExecuteSequence](adminexecutesequence-table.md)e la [tabella InstallExecuteSequence](installexecutesequence-table.md) per verificare che le [azioni standard](standard-actions.md) seguenti non siano state impostate con le condizioni nel campo condizione.

-   [Azione CostInitialize](costinitialize-action.md)
-   [Azione CostFinalize secondo](costfinalize-action.md)
-   [Azione filecost](filecost-action.md)
-   [Azione InstallValidate](installvalidate-action.md)
-   [Azione InstallInitialize](installinitialize-action.md)
-   [Azione InstallFinalize](installfinalize-action.md)
-   [Azione ProcessComponents](processcomponents-action.md)
-   [Azione PublishFeatures](publishfeatures-action.md)
-   [Azione PublishProduct](publishproduct-action.md)
-   [Azione RegisterProduct](registerproduct-action.md)
-   [Azione UnpublishFeatures](unpublishfeatures-action.md)

Se vengono rilevate condizioni, ICE84 pubblica un avviso.

## <a name="result"></a>Risultato

ICE84 invia il seguente avviso.



| Errore ICE84                                                             | Descrizione                                           |
|-------------------------------------------------------------------------|-------------------------------------------------------|
| L'azione ' \[ 1 \] ' trovata nella tabella% s è un'azione obbligatoria con una condizione. | È stata creata un'azione obbligatoria con una condizione. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



