---
description: L'azione RemoveShortcuts gestisce la rimozione di un collegamento annunciato la cui funzionalità è selezionata per la disinstallazione o un collegamento non annunciato il cui componente è selezionato per la disinstallazione. Per ulteriori informazioni, vedere la tabella dei collegamenti.
ms.assetid: 897e8a13-d9c5-4f98-8785-c0f053a11f3d
title: Azione RemoveShortcuts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 151f5fac6733e61b7ba27320a5e79c522abcc3e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313802"
---
# <a name="removeshortcuts-action"></a>Azione RemoveShortcuts

L'azione RemoveShortcuts gestisce la rimozione di un collegamento annunciato la cui funzionalità è selezionata per la disinstallazione o un collegamento non annunciato il cui componente è selezionato per la disinstallazione. Per ulteriori informazioni, vedere la [tabella dei collegamenti](shortcut-table.md).

## <a name="sequence-restrictions"></a>Restrizioni sequenza

L'azione RemoveShortcuts deve precedere l'azione [CreateShortcuts](createshortcuts-action.md) .

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione      |
|-------|---------------------------------|
| \[1\] | Identificatore del collegamento rimosso. |



 

 

 



