---
description: L'azione WriteRegistryValori consente configura le informazioni del registro di sistema di un'applicazione.
ms.assetid: ab121de3-f07d-401a-b52a-246a555c142c
title: Azione WriteRegistryValori consente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be13cc5cf5a817e44caa34b9084115b7dda8cee3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313771"
---
# <a name="writeregistryvalues-action"></a>Azione WriteRegistryValori consente

L'azione WriteRegistryValori consente configura le informazioni del registro di sistema di un'applicazione. Le informazioni del registro di sistema sono gestite dalla [tabella dei componenti](component-table.md). Un valore del registro di sistema viene scritto nel registro di sistema se il componente corrispondente è stato impostato per essere installato localmente o come eseguito dall'origine. Per altre informazioni, vedere [tabella del registro di sistema](registry-table.md).

## <a name="sequence-restrictions"></a>Restrizioni sequenza

L' [azione InstallValidate](installvalidate-action.md) deve precedere l'azione WriteRegistryValori consente. Se è presente un' [azione RemoveRegistryValues](removeregistryvalues-action.md), è necessario che venga eseguita prima dell'azione WriteRegistryValori consente.

È possibile utilizzare un'azione personalizzata per aggiungere righe alla [tabella del registro di sistema](registry-table.md) durante un'installazione, una disinstallazione o una transazione di ripristino. Queste righe non vengono mantenute nella tabella del registro di sistema e le informazioni sono disponibili solo durante la transazione corrente. L'azione personalizzata deve pertanto essere eseguita in ogni installazione, disinstallazione o ripristino della transazione che richiede le informazioni contenute in queste righe aggiuntive. L'azione personalizzata deve precedere le azioni [RemoveRegistryValues](removeregistryvalues-action.md) e WriteRegistryValori consente nella sequenza di azione.

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione                               |
|-------|----------------------------------------------------------|
| \[1\] | Percorso della chiave del registro di sistema del valore scritto nel registro di sistema.       |
| \[2\] | Nome della stringa di testo formattato del valore scritto nel registro di sistema. |
| \[3\] | Stringa di testo formattata del valore scritto nel registro di sistema.      |



 

 

 



