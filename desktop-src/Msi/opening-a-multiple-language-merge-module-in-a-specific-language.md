---
description: Quando si esegue il merge di un modulo in un database di installazione, sono disponibili due linguaggi importanti.
ms.assetid: e815854f-a379-497a-ae37-b13de39dd516
title: Apertura di un modulo merge Multiple-Language in una lingua specifica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b552c41d7696b29a86987d027e00ef4cb19bbb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049624"
---
# <a name="opening-a-multiple-language-merge-module-in-a-specific-language"></a>Apertura di un modulo merge Multiple-Language in una lingua specifica

Quando si esegue il merge di un modulo in un database di installazione, sono disponibili due linguaggi importanti. Il primo è la lingua del pacchetto di installazione di destinazione specificato da [**ProductLanguage**](productlanguage.md) nella [tabella delle proprietà](property-table.md). Il secondo è il linguaggio del modulo merge visualizzato nella colonna language della [tabella ModuleSignature](modulesignature-table.md).

La lingua del pacchetto di installazione può essere passata al modulo dallo strumento di merge quando il pacchetto viene aperto per un'operazione di merge. Tuttavia, a volte potrebbe essere necessario ignorare la lingua della destinazione e richiedere che il modulo venga aperto in un'altra lingua, ad esempio un pacchetto inglese che installa sia le risorse inglesi che quelle tedesche dal modulo.

Quando si apre un modulo con una richiesta di lingua, lo strumento di merge controlla la lingua richiesta rispetto alle lingue specificate nella colonna lingua della [tabella ModuleSignature](modulesignature-table.md).

Il processo seguente viene usato per determinare la lingua da usare.

**Per determinare la lingua da usare**

1.  Se la lingua nella [tabella ModuleSignature](modulesignature-table.md) è uguale o più generale rispetto alla lingua richiesta, viene aperto il modulo.
2.  Se il modulo supporta la lingua esatta richiesta, viene usata tale lingua.
3.  Se il modulo supporta il gruppo di lingue della lingua richiesta dal gruppo di lingue, ad esempio, controllare 9 se 1033 è stato richiesto ma non è stato trovato nel passaggio 2.
4.  Controllare se è presente una trasformazione del linguaggio che modifica il modulo in neutro.
5.  Se nessuno dei passaggi precedenti ha esito positivo, il modulo non supporta la lingua richiesta e l'Unione ha esito negativo.

 

 



