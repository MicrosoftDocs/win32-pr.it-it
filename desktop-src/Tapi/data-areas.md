---
description: Alcuni set di telefoni supportano la nozione di download o di caricamento dei dati nel dispositivo telefonico, che consente la programmazione del telefono in diversi modi.
ms.assetid: 5734107d-8104-4d8a-b3f7-3cc2a48f71ca
title: Aree dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81376549c63b4fcea92f705246cd58161faeac94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311910"
---
# <a name="data-areas"></a>Aree dati

Alcuni set di telefoni supportano la nozione di download o di caricamento dei dati nel dispositivo telefonico, che consente la programmazione del telefono in diversi modi. Questi set di telefono vengono modellati da TAPI con una o più aree di download o di caricamento. Ogni area è identificata da un numero compreso tra zero e il numero di aree dati disponibili sul telefono meno uno. Le dimensioni di ogni area possono variare. Il formato dei dati è specifico del dispositivo.

La funzione [**phoneSetData**](/windows/desktop/api/Tapi/nf-tapi-phonesetdata) di TAPI Scarica un buffer di dati in una determinata area dati del dispositivo telefonico e la funzione [**phoneGetData**](/windows/desktop/api/Tapi/nf-tapi-phonegetdata) carica il contenuto di una determinata area dati del dispositivo telefonico in un buffer.

Quando viene modificata un'area dati di un dispositivo telefonico, all'applicazione viene inviato un messaggio di [**\_ stato telefonico**](phone-state.md) per notificare all'applicazione la modifica dello stato. I parametri di questo messaggio forniscono un'indicazione della modifica.

 

 



