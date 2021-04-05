---
description: L'azione InstallInitialize e l'azione InstallFinalize contrassegnano l'inizio e la fine di una sequenza di azioni che modificano il sistema.
ms.assetid: c2637070-3fd9-422c-9252-cf15045c6485
title: Azione InstallInitialize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80d500779ed018905edfc5347d85d21cc40e6175
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752202"
---
# <a name="installinitialize-action"></a>Azione InstallInitialize

L'azione InstallInitialize e l'azione [InstallFinalize](installfinalize-action.md) contrassegnano l'inizio e la fine di una sequenza di azioni che modificano il sistema.

## <a name="sequence-restrictions"></a>Restrizioni sequenza

L'azione InstallInitialize deve essere sequenziata prima di qualsiasi azione che modifichi il sistema, ad esempio l'azione [InstallFiles](installfiles-action.md) , l'azione [WriteRegistryValori consente](writeregistryvalues-action.md) , l'azione [SelfRegModules](selfregmodules-action.md) e l'azione [ProcessComponents](processcomponents-action.md) . L'azione InstallInitialize deve quindi essere sequenziata prima dell'azione [InstallFinalize](installfinalize-action.md) e [InstallExecute](installexecute-action.md) .

Le [azioni personalizzate](custom-actions.md) che modificano il pacchetto di Windows Installer, ad esempio l'aggiunta di righe a una tabella che gestisce le risorse installabili, ad esempio la tabella [del registro di sistema](registry-table.md) o la tabella [DuplicateFile](duplicatefile-table.md) , devono essere sequenziate prima dell'azione InstallInitialize.

## <a name="actiondata-messages"></a>Messaggi ActionData

Nessun messaggio ActionData.

 

 



