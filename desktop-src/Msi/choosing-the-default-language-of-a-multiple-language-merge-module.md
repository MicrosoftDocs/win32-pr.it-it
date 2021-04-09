---
description: La lingua predefinita per un modulo merge è la lingua elencata nella tabella ModuleSignature del modulo prima dell'applicazione delle trasformazioni del linguaggio. Si tratta anche del primo linguaggio elencato nella proprietà di riepilogo del modello.
ms.assetid: 4d795727-684c-4dc1-8b46-d72b69c455c3
title: Scelta della lingua predefinita di un modulo merge a più lingue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 758a3b47b7a41777652a11a1cdc1b7f380055cb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881061"
---
# <a name="choosing-the-default-language-of-a-multiple-language-merge-module"></a>Scelta della lingua predefinita di un modulo merge a più lingue

La lingua predefinita per un modulo merge è la lingua elencata nella [tabella ModuleSignature](modulesignature-table.md) del modulo prima dell'applicazione delle trasformazioni del linguaggio. Si tratta anche del primo linguaggio elencato nella proprietà di [**Riepilogo del modello**](template-summary.md) .

La lingua predefinita per il modulo deve essere uno dei linguaggi più specifici supportati, perché la lingua predefinita viene sempre controllata per prima e, se soddisfa la lingua richiesta, viene usata anche se un'altra lingua è una corrispondenza migliore. Se, ad esempio, un modulo supporta 1033 e 0, 1033 deve essere la lingua predefinita. Se 0 era la lingua predefinita, soddisfa sempre qualsiasi richiesta e la trasformazione 1033 non verrebbe mai utilizzata, anche se 1033 è la lingua esatta richiesta.

 

 



