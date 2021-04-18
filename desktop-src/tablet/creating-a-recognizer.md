---
description: Se si sceglie di eseguire questa operazione, l'applicazione può fornire le proprie implementazioni di riconoscimento. In questa sezione vengono descritti i requisiti per la creazione di un sistema di riconoscimento di applicazioni personalizzato per l'applicazione che è possibile utilizzare con l'API della piattaforma Tablet PC.
ms.assetid: 502ef3fb-ba45-4f8b-bbd5-19c24e313439
title: Creazione di un riconoscimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bc71f56dc7095c6c72d18b36c3a12caa493ec9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305347"
---
# <a name="creating-a-recognizer"></a>Creazione di un riconoscimento

Se si sceglie di eseguire questa operazione, l'applicazione può fornire le proprie implementazioni di riconoscimento. In questa sezione vengono descritti i requisiti per la creazione di un sistema di riconoscimento di applicazioni personalizzato per l'applicazione che è possibile utilizzare con l'API della piattaforma Tablet PC.

> [!Note]  
> I sistemi di riconoscimento delle applicazioni personalizzati non vengono utilizzati dal pannello input penna di Tablet PC o da Microsoft Windows Journal. Questi accessori utilizzano solo i riconoscitori per i quali sono stati testati.

 

Le sezioni seguenti illustrano in dettaglio l'implementazione di un sistema di riconoscimento personalizzato:

-   [Architettura dell'API di riconoscimento](recognition-api-architecture.md)
-   [API di riconoscimento richieste](/previous-versions//ms701664(v=vs.85))
-   [HRECOGNIZER e HRECOCONTEXT](hrecognizer-and-hrecocontext.md)
-   [Struttura del reticolo del riconoscitore](recognizer-lattice-structure.md)
-   [Registrazione della DLL del riconoscitore](registering-your-recognizer-dll.md)
-   [Considerazioni sul threading del riconoscimento](recognizer-threading-considerations.md)
-   [Sequenza di chiamata tipica](typical-calling-sequence.md)
-   [Modello di esempio della DLL di riconoscimento](recognizer-dll-sample-template.md)
-   [Valori di intervallo Unicode dei movimenti](unicode-range-values-of-gestures.md)
-   [API di riconoscimento](recognizer-apis.md)

 

 
