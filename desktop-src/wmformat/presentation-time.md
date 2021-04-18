---
title: Ora di presentazione
description: Ora di presentazione
ms.assetid: 856e1783-85b4-4195-970f-3d7b5612672b
keywords:
- Windows Media Format SDK, tempi di presentazione
- Formato avanzato dei sistemi (ASF), tempi di presentazione
- ASF (formato avanzato dei sistemi), tempi di presentazione
- tempi di presentazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bc88dbba93d1fc68905a4bfea92328a4ef600eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331708"
---
# <a name="presentation-time"></a>Ora di presentazione

Un'ora di presentazione è una misurazione del tempo dal primo campione del primo flusso in un file ASF. Questa misurazione, oltre alla maggior parte delle altre misurazioni del tempo usato dagli oggetti di questo SDK, si trova in unità di 100 nanosecondi. I tempi di presentazione sono importanti perché consentono la sincronizzazione dei vari flussi in un file. È necessario fornire un'ora di presentazione per ogni esempio di input passato al writer. A ogni oggetto dati nella sezione dati di un file ASF è associato un tempo di presentazione. Ogni esempio di output recuperato dal lettore dispone anche di un'ora di presentazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Concetti**](concepts.md)
</dt> <dt>

[**Input, flussi e output**](inputs-streams-and-outputs.md)
</dt> <dt>

[**Esempi di supporti**](media-samples.md)
</dt> </dl>

 

 




