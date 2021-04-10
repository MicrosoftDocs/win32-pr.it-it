---
description: Più moduli di linguaggio possono fornire componenti con diverse lingue come un unico file composto.
ms.assetid: b3a0b635-49c7-4f95-b31f-6c8688466dd2
title: Moduli unione a più lingue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d414cce484022bf81647110ac032d0db270d383
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967140"
---
# <a name="multiple-language-merge-modules"></a>Moduli unione a più lingue

Più moduli di linguaggio possono fornire componenti con diverse lingue come un unico file composto. La progettazione e le funzionalità dei moduli unione con più linguaggi sono simili ai moduli a linguaggio singolo. Un modulo di merge a più lingue include più lingue elencate nella proprietà di [**Riepilogo del modello**](template-summary.md) . Il database di un modulo di Unione a più lingue contiene tutte le informazioni di configurazione per più lingue. Il cabinet MergeModule.CABinet all'interno di un modulo di Unione a più lingue contiene tutti i file per tutte le lingue supportate.

Quando si applica un file con estensione MSM a più lingue a un file con estensione msi, è necessario indicare la lingua finale del pacchetto di installazione dopo l'Unione. Nel caso di un singolo modulo di merge della lingua, la [tabella file](file-table.md) del modulo merge elenca tutti i file presenti nel file CAB MergeModule.CABinet. Nel caso di un modulo di Unione a più lingue, MergeModule.CABinet contiene tutti i file per ogni lingua supportata dal modulo, ma solo il subset di file per la lingua finale passa alla tabella file del modulo. Lo strumento di merge deve garantire che il modulo fornisca il subset di informazioni e file necessari per la lingua finale richiesta.

Ogni modulo merge ha una lingua predefinita specificata nella colonna language della [tabella ModuleSignature](modulesignature-table.md). La lingua predefinita di un modulo merge viene visualizzata anche come prima o solo lingua nella proprietà di riepilogo del [**modello**](template-summary.md) . A seconda della lingua finale richiesta e della lingua predefinita del modulo, lo strumento merge può applicare le trasformazioni della lingua a un modulo di merge a più lingue, in modo che possa essere aperto nella lingua richiesta o un'approssimazione della lingua richiesta. Le trasformazioni del linguaggio vengono incorporate all'interno del modulo merge. Gli strumenti di merge devono applicare le trasformazioni del linguaggio in conformità alle regole generali seguenti:

-   Se le lingue predefinite e finali sono le stesse, è possibile unire il modulo senza usare le trasformazioni del linguaggio.
-   Se la lingua predefinita è 0 (un modulo indipendente dalla lingua), è possibile unire il modulo senza usare le trasformazioni della lingua.
-   Se il linguaggio finale non è la lingua predefinita, lo strumento di merge deve applicare una delle trasformazioni del linguaggio incorporate nel modulo per modificare il modulo in modo che sia la lingua finale o un'approssimazione della lingua finale.

Ad esempio, non sono necessarie trasformazioni di lingua se la lingua finale è 1033 (Inglese Stati Uniti) e la lingua predefinita del modulo è 1033 (Inglese (Stati Uniti), 0 (indipendente dalla lingua) o 9 (inglese generico).

Le trasformazioni della lingua sono necessarie se la lingua finale è 1033 (Inglese Stati Uniti) e la lingua predefinita è 1031 (tedesco). In questo caso, è possibile che lo strumento di merge cerchi innanzitutto il modulo a più lingue per una trasformazione lingua incorporata su 1033 (Stati Uniti). Se l'operazione ha esito negativo, può cercare una trasformazione in un linguaggio con un LANGID primario corrispondente, anche se il LANGID secondario non corrisponde. Se, ad esempio, lo strumento non è in grado di trovare una trasformazione su 1033 (Inglese Stati Uniti), Cerca una trasformazione su 9 (inglese generico). Se l'operazione non riesce, lo strumento di merge cerca una trasformazione in 0 (indipendente dalla lingua). Se tutte le ricerche di una trasformazione appropriata hanno esito negativo, non è possibile aprire il modulo.

Per ulteriori informazioni, vedere la pagina relativa alla creazione di modelli di [Unione di più linguaggi](authoring-multiple-language-merge-modules.md).

 

 



