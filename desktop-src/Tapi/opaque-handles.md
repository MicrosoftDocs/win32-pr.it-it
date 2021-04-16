---
description: Alcuni tipi definiti da TSPI sono handle opachi.
ms.assetid: e52ed691-0479-48da-9e06-c6a0d7a20e10
title: Handle opachi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2df2e0b0f608b9cefc8f0f4f538bffd452a8aab6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527097"
---
# <a name="opaque-handles"></a>Handle opachi

Alcuni tipi definiti da TSPI sono handle opachi. Questi vengono usati in TSPI come riferimenti pubblici a strutture di dati private. In questo modo è possibile controllare il tipo dei parametri forniti alle procedure dell'interfaccia, fornendo comunque una misura di protezione dei tipi. Solo il proprietario della struttura di dati privata è in grado di interpretare il tipo opaco come riferimento alla relativa rappresentazione della struttura di dati. Per un esempio di come vengono usati gli handle opachi, prendere in considerazione un dispositivo telefonico. Sia TAPI che il provider di servizi mantengono in genere le strutture dei dati che rappresentano le rispettive visualizzazioni del dispositivo.

Nelle tipiche strutture di dati del telefono gestite da TAPI e da un provider di servizi, ciascuna contiene un handle opaco per l'altra struttura di dati. Questi sono stati scambiati in un passaggio di inizializzazione iniziale. Quando TAPI chiama una funzione TSPI, passa l'handle opaco per fare riferimento al dispositivo. Il provider di servizi è in grado di risolvere questo problema come riferimento (freccia) alla struttura dei dati. Un processo simile si verifica quando il provider di servizi chiama una funzione di callback in TAPI.

 

 



