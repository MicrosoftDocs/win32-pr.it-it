---
description: Quando si unisce un modulo in un database di installazione, esistono due lingue importanti.
ms.assetid: e815854f-a379-497a-ae37-b13de39dd516
title: Apertura di un Multiple-Language merge in un linguaggio specifico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc4dd46009f0cbe4f8c0f2cfd8b4f5dcd2caf91c7987ece7b3b032f61d9161ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942872"
---
# <a name="opening-a-multiple-language-merge-module-in-a-specific-language"></a>Apertura di un Multiple-Language merge in un linguaggio specifico

Quando si unisce un modulo in un database di installazione, esistono due lingue importanti. Il primo è la lingua del pacchetto di installazione di destinazione specificato da [**ProductLanguage**](productlanguage.md) nella [tabella delle proprietà](property-table.md). Il secondo è la lingua del modulo unione visualizzata nella colonna Lingua della [tabella ModuleSignature](modulesignature-table.md).

La lingua del pacchetto di installazione può essere passata al modulo dallo strumento di unione quando il pacchetto viene aperto per un'unione. Tuttavia, a volte può essere necessario ignorare la lingua della destinazione e richiedere che il modulo venga aperto in un'altra lingua, ad esempio un pacchetto in inglese che installa le risorse inglese e tedesco dal modulo.

Quando si apre un modulo con una richiesta di lingua, lo strumento di unione controlla la lingua richiesta rispetto alle lingue specificate nella colonna Lingua della [tabella ModuleSignature](modulesignature-table.md).

Il processo seguente viene usato per determinare la lingua da usare.

**Per determinare la lingua da usare**

1.  Se la lingua nella [tabella ModuleSignature è](modulesignature-table.md) uguale o più generale della lingua richiesta, viene aperto il modulo.
2.  Se il modulo supporta la lingua esatta richiesta, viene usata tale lingua.
3.  Se il modulo supporta il gruppo di lingue della lingua richiesta, ad esempio, controllare 9 se è stato richiesto 1033 ma non è stato trovato nel passaggio 2.
4.  Verificare se è presente una trasformazione del linguaggio che modifica il modulo in neutro.
5.  Se nessuno dei passaggi precedenti ha esito positivo, il modulo non supporta la lingua richiesta e l'unione non riesce.

 

 



