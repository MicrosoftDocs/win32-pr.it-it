---
description: L'azione UnregisterTypeLibraries Annulla la registrazione delle librerie dei tipi dal sistema. Questa azione viene applicata a ogni file elencato nella tabella TypeLib attivata per la disinstallazione.
ms.assetid: fea5bdc1-ac27-4d02-bcea-5c97366dd394
title: Azione UnregisterTypeLibraries
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b399f80d940839c5e94028a9c32e706f4826341a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319417"
---
# <a name="unregistertypelibraries-action"></a>Azione UnregisterTypeLibraries

L'azione UnregisterTypeLibraries Annulla la registrazione delle librerie dei tipi dal sistema. Questa azione viene applicata a ogni file elencato nella tabella [typelib](typelib-table.md) attivata per la disinstallazione.

## <a name="sequence-restrictions"></a>Restrizioni sequenza

L'azione UnregisterTypeLibraries deve precedere l'azione [RemoveFiles](removefiles-action.md) .

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione                        |
|-------|---------------------------------------------------|
| \[1\] | [GUID](guid.md) di una libreria dei tipi non registrata. |



 

 

 



