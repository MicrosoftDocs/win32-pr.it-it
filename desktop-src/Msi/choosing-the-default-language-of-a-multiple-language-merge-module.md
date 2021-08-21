---
description: Il linguaggio predefinito per un modulo unione è il linguaggio elencato nella tabella ModuleSignature del modulo prima dell'applicazione delle trasformazioni del linguaggio. Questa è anche la prima lingua elencata nella proprietà Riepilogo modello.
ms.assetid: 4d795727-684c-4dc1-8b46-d72b69c455c3
title: Scelta della lingua predefinita di un modulo unione in più lingue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c174a3917538b1562626819f8ba2bf07864c9169c27e717a078cca8d64992ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118145657"
---
# <a name="choosing-the-default-language-of-a-multiple-language-merge-module"></a>Scelta della lingua predefinita di un modulo unione in più lingue

Il linguaggio predefinito per un modulo unione è il linguaggio elencato nella tabella [ModuleSignature](modulesignature-table.md) del modulo prima dell'applicazione delle trasformazioni del linguaggio. Questa è anche la prima lingua elencata nella proprietà [**Riepilogo**](template-summary.md) modello.

La lingua predefinita per il modulo deve essere una delle lingue più specifiche supportate, perché la lingua predefinita viene sempre controllata per prima e, se soddisfa la lingua richiesta, viene usata anche se un'altra lingua è una corrispondenza migliore. Ad esempio, se un modulo supporta 1033 e 0, 1033 deve essere la lingua predefinita. Se 0 fosse la lingua predefinita, verrebbe sempre soddisfatta qualsiasi richiesta e la trasformazione 1033 non verrebbe mai usata, anche se 1033 è la lingua esatta richiesta.

 

 



