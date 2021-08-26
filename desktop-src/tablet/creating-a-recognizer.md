---
description: Se si sceglie di eseguire questa operazione, l'applicazione può fornire implementazioni del riconoscitore proprie. Questa sezione descrive i requisiti per la creazione di un sistema di riconoscimento dell'applicazione personalizzato per l'applicazione che è possibile usare con l'API della piattaforma Tablet PC.
ms.assetid: 502ef3fb-ba45-4f8b-bbd5-19c24e313439
title: Creazione di un riconoscitore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab9f35277c32c40658adb5530f4521c945df12152aa214167573e111eccdca13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941051"
---
# <a name="creating-a-recognizer"></a>Creazione di un riconoscitore

Se si sceglie di eseguire questa operazione, l'applicazione può fornire implementazioni del riconoscitore proprie. Questa sezione descrive i requisiti per la creazione di un sistema di riconoscimento dell'applicazione personalizzato per l'applicazione che è possibile usare con l'API della piattaforma Tablet PC.

> [!Note]  
> I riconoscitori di applicazioni personalizzati non vengono usati dal Pannello di input di Tablet PC o da Microsoft Windows Journal. Questi accessori usano solo i riconoscitori con cui sono stati testati.

 

Le sezioni seguenti illustrano in dettaglio l'implementazione di un sistema di riconoscimento personalizzato:

-   [Architettura dell'API Di riconoscimento](recognition-api-architecture.md)
-   [API di riconoscimento necessarie](/previous-versions//ms701664(v=vs.85))
-   [HRECOGNIZER e HRECOCONTEXT](hrecognizer-and-hrecocontext.md)
-   [Struttura del reticolo del riconoscitore](recognizer-lattice-structure.md)
-   [Registrazione della DLL del riconoscitore](registering-your-recognizer-dll.md)
-   [Considerazioni sul threading del riconoscitore](recognizer-threading-considerations.md)
-   [Sequenza di chiamata tipica](typical-calling-sequence.md)
-   [Modello di esempio di DLL di riconoscimento](recognizer-dll-sample-template.md)
-   [Valori di intervallo Unicode dei movimenti](unicode-range-values-of-gestures.md)
-   [API di riconoscimento](recognizer-apis.md)

 

 
