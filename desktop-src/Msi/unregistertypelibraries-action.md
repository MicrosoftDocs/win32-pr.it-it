---
description: L'azione UnregisterTypeLibraries annulla la registrazione delle librerie dei tipi dal sistema. Questa azione viene applicata a ogni file elencato nella tabella TypeLib che viene attivata per la disinstallazione.
ms.assetid: fea5bdc1-ac27-4d02-bcea-5c97366dd394
title: Azione UnregisterTypeLibraries
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6066dbac7e63696f838375261fbb63e8348faf630a7439ec7531cdd71d4ace97
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810121"
---
# <a name="unregistertypelibraries-action"></a>Azione UnregisterTypeLibraries

L'azione UnregisterTypeLibraries annulla la registrazione delle librerie dei tipi dal sistema. Questa azione viene applicata a ogni file elencato nella [tabella TypeLib](typelib-table.md) che viene attivata per la disinstallazione.

## <a name="sequence-restrictions"></a>Restrizioni relative alle sequenze

L'azione UnregisterTypeLibraries deve essere eseguita prima [dell'azione RemoveFiles.](removefiles-action.md)

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione                        |
|-------|---------------------------------------------------|
| \[1\] | [GUID](guid.md) di una libreria dei tipi non registrata. |



 

 

 



