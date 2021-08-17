---
description: Alcuni set di telefoni supportano la nozione di download o caricamento di dati nel dispositivo telefonico, che consente di programmare il set di telefoni in diversi modi.
ms.assetid: 5734107d-8104-4d8a-b3f7-3cc2a48f71ca
title: Aree dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed05d6233a8c8ed31a2d00d28970a517ef181f00689c7da34673d3044fffb4dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117946144"
---
# <a name="data-areas"></a>Aree dati

Alcuni set di telefoni supportano la nozione di download o caricamento di dati nel dispositivo telefonico, che consente di programmare il set di telefoni in diversi modi. TAPI modella questi set di telefoni come con una o più aree di download o caricamento. Ogni area è identificata da un numero compreso tra zero e il numero di aree dati disponibili sul telefono meno uno. Le dimensioni di ogni area possono variare. Il formato dei dati è specifico del dispositivo.

La funzione TAPI [**phoneSetData**](/windows/desktop/api/Tapi/nf-tapi-phonesetdata) scarica un buffer di dati in una determinata area dati nel dispositivo telefonico e la funzione [**phoneGetData**](/windows/desktop/api/Tapi/nf-tapi-phonegetdata) carica il contenuto di una determinata area dati nel dispositivo telefono in un buffer.

Quando un'area dati di un dispositivo telefono viene modificata, viene inviato un messaggio [**PHONE \_ STATE**](phone-state.md) all'applicazione per notificare all'applicazione la modifica dello stato. I parametri di questo messaggio forniscono un'indicazione della modifica.

 

 



