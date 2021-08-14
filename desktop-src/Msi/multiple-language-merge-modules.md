---
description: Più moduli linguistici possono distribuire componenti con più linguaggi diversi come un singolo file composto.
ms.assetid: b3a0b635-49c7-4f95-b31f-6c8688466dd2
title: Più moduli unione in linguaggio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17f32d219e1071cd431117919d3eb3f3361d30213f59a26f9ec2cdf2e81e591b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118943422"
---
# <a name="multiple-language-merge-modules"></a>Più moduli unione in linguaggio

Più moduli linguistici possono distribuire componenti con più linguaggi diversi come un singolo file composto. La progettazione e la funzionalità di più moduli unione linguistici sono simili ai moduli per un singolo linguaggio. In un modulo unione in più lingue sono elencate più lingue nella [**proprietà Riepilogo**](template-summary.md) modello. Il database di un modulo unione in più lingue contiene tutte le informazioni di installazione per più lingue. Il MergeModule.CABinet cabinet all'interno di un modulo unione in più lingue contiene tutti i file per tutte le lingue supportate.

Quando si applica un file con estensione msm in più lingue a un file .msi, è necessario indicare la lingua finale del pacchetto di installazione dopo l'unione. Nel caso di un singolo modulo unione linguistico, nella tabella [File](file-table.md) del modulo unione sono elencati tutti i file presenti nell'MergeModule.CABinet cabinet. Nel caso di un modulo unione in più lingue, MergeModule.CABinet contiene tutti i file per ogni lingua supportata dal modulo, ma solo il subset di file per il linguaggio finale viene inserito nella tabella File del modulo. Lo strumento di unione deve garantire che il modulo ofni il subset di informazioni e file necessari per il linguaggio finale richiesto.

Ogni modulo unione ha una lingua predefinita specificata nella colonna Language della [tabella ModuleSignature](modulesignature-table.md). La lingua predefinita di un modulo unione viene visualizzata anche come prima o unica lingua nella [**proprietà Riepilogo**](template-summary.md) modello. A seconda del linguaggio finale richiesto e del linguaggio predefinito del modulo, lo strumento di unione può applicare trasformazioni del linguaggio a un modulo unione in più lingue in modo che possa essere aperto nella lingua richiesta o un'approssimazione della lingua richiesta. Le trasformazioni del linguaggio sono incorporate all'interno del modulo di unione. Gli strumenti di unione devono applicare trasformazioni del linguaggio in conformità alle regole generali seguenti:

-   Se le lingue predefinite e finali sono uguali, il modulo può essere unito senza usare trasformazioni del linguaggio.
-   Se la lingua predefinita è 0 (un modulo indipendente dalla lingua), il modulo può essere unito senza usare trasformazioni del linguaggio.
-   Se la lingua finale non è quella predefinita, lo strumento di unione deve applicare una delle trasformazioni del linguaggio incorporate nel modulo per passare al linguaggio finale o a un'approssimazione del linguaggio finale.

Ad esempio, non sono necessarie trasformazioni della lingua se la lingua finale è 1033 (inglese Stati Uniti) e la lingua predefinita del modulo è 1033 (inglese Stati Uniti), 0 (indipendente dalla lingua) o 9 (inglese generico).

Le trasformazioni della lingua sono necessarie se la lingua finale è 1033 (inglese Stati Uniti) e la lingua predefinita è 1031 (tedesco). In questo caso, lo strumento di unione può prima cercare nel modulo in più lingue una trasformazione della lingua incorporata in 1033 (inglese Stati Uniti). In caso di esito negativo, può quindi cercare una trasformazione in una lingua con un LANGID primario corrispondente, anche se il LANGID secondario non corrisponde. Ad esempio, se lo strumento non trova una trasformazione in 1033 (inglese Stati Uniti), cerca una trasformazione in 9 (inglese generico). Se l'operazione non riesce, lo strumento di unione cerca una trasformazione in 0 (indipendente dalla lingua). Se tutte queste ricerche per una trasformazione appropriata hanno esito negativo, l'apertura del modulo non riesce.

Per altre informazioni, vedere [Authoring Multiple Language Merge Modules](authoring-multiple-language-merge-modules.md).

 

 



