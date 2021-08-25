---
title: Ora di presentazione
description: Ora di presentazione
ms.assetid: 856e1783-85b4-4195-970f-3d7b5612672b
keywords:
- Windows MEDIA Format SDK, orari di presentazione
- Advanced Systems Format (ASF), tempi di presentazione
- ASF (Advanced Systems Format),presentation times
- orari di presentazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2dea9181552b42508745b256768b2c5ceb4443a057fc5d7d7a5a44410c788fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807911"
---
# <a name="presentation-time"></a>Ora di presentazione

Un'ora di presentazione è una misurazione dell'ora del primo esempio del primo flusso in un file ASF. Questa misura, così come la maggior parte delle altre misurazioni del tempo usate dagli oggetti di questo SDK, si trova in unità di 100 nanosecondi. I tempi di presentazione sono importanti perché consentono la sincronizzazione dei vari flussi in un file. È necessario specificare un'ora di presentazione per ogni esempio di input passato al writer. A ogni oggetto dati nella sezione data di un file ASF è associata un'ora di presentazione. Ogni esempio di output recuperato dal lettore ha anche un'ora di presentazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Concetti**](concepts.md)
</dt> <dt>

[**Input, Flussi e output**](inputs-streams-and-outputs.md)
</dt> <dt>

[**Esempi di supporti**](media-samples.md)
</dt> </dl>

 

 




