---
description: L'elenco seguente contiene gli obiettivi di progettazione dell'MSP di TAPI.
ms.assetid: 286b96c1-047b-4cb9-a189-af2818cfec58
title: Obiettivi di progettazione generali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 052bbf607e71986678acca29d17d587bfa5bccf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308082"
---
# <a name="general-design-goals"></a>Obiettivi di progettazione generali

L'elenco seguente contiene gli obiettivi di progettazione dell'MSP di TAPI.

-   Le classi base sono state mantenute semplici, con membri e metodi introdotti solo quando strettamente necessario.
-   Ereditarietà semplice. Nessuna ereditarietà multipla tra le classi, sebbene venga utilizzata più ereditarietà per le interfacce.
-   Il blocco si verifica solo in una direzione per impedire il deadlock. I metodi sull'oggetto chiamata che richiedono il blocco sulla chiamata potrebbero chiamare metodi sul flusso che richiedono il blocco sul flusso. Tuttavia, i metodi nel flusso che richiedono il blocco sul flusso non chiameranno mai un metodo sulla chiamata che richiede un blocco sulla chiamata.
-   RefCounts vengono usati per proteggere l'accesso. Tutti i callback inviati al pool di thread contengono refCounts. Refcount viene annullato quando l'attesa viene annullata. L'oggetto Address ha refCounts nei terminali. Gli oggetti Call hanno refCounts sull'indirizzo e sui flussi. Gli oggetti Stream hanno refCounts su chiamate e terminali. I terminali hanno refCounts sui flussi. Il refCounts circolare si interrompe quando viene chiamato il metodo Shutdown sugli oggetti Address e call.

 

 



