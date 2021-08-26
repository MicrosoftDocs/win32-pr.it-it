---
description: L'azione InstallInitialize e l'azione InstallFinalize contrassegnano l'inizio e la fine di una sequenza di azioni che modificano il sistema.
ms.assetid: c2637070-3fd9-422c-9252-cf15045c6485
title: Azione InstallInitialize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7031ab79bc099ea067fd8d83cb83d8cefd1f36a1e83f696a1ee3b4487b3cac88
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996571"
---
# <a name="installinitialize-action"></a>Azione InstallInitialize

L'azione InstallInitialize e [l'azione InstallFinalize](installfinalize-action.md) contrassegnano l'inizio e la fine di una sequenza di azioni che modificano il sistema.

## <a name="sequence-restrictions"></a>Restrizioni relative alle sequenze

L'azione InstallInitialize deve essere sequenziata prima di qualsiasi azione che modifica il sistema, ad esempio [l'azione InstallFiles,](installfiles-action.md) [l'azione WriteRegistryValues,](writeregistryvalues-action.md) [l'azione SelfRegModules](selfregmodules-action.md) e l'azione [ProcessComponents.](processcomponents-action.md) L'azione InstallInitialize deve quindi essere sequenziata prima [dell'azione InstallFinalize](installfinalize-action.md) e [dell'azione InstallExecute.](installexecute-action.md)

[](custom-actions.md) Le azioni personalizzate che modificano il pacchetto del programma di installazione di Windows, ad esempio aggiungendo righe a una tabella che gestisce le risorse installabili, ad esempio la tabella [Del](registry-table.md) Registro di sistema o la tabella [DuplicateFile,](duplicatefile-table.md) devono essere sequenziate prima dell'azione InstallInitialize.

## <a name="actiondata-messages"></a>Messaggi ActionData

Non sono presenti messaggi ActionData.

 

 



