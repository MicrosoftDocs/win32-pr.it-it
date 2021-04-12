---
title: Enumerazione del formato di input
description: Enumerazione del formato di input
ms.assetid: 75264598-0226-435a-b71f-6997ff0fcaff
keywords:
- Windows Media Format SDK, enumerazioni del formato di input
- Windows Media Format SDK, enumerazione dei formati di input
- Advanced Systems Format (ASF), enumerazioni del formato di input
- ASF (formato avanzato dei sistemi), enumerazioni del formato di input
- Formato di sistemi avanzati (ASF), enumerazione dei formati di input
- ASF (Advanced Systems Format), enumerazione dei formati di input
- enumerazioni del formato di input
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e853aeeac5ca470f1b33b611b287cba8fa025dc0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471694"
---
# <a name="input-format-enumeration"></a>Enumerazione del formato di input

L'oggetto writer ottiene le informazioni sul formato del flusso dal profilo fornito. Il flusso di informazioni di configurazione in un profilo fornisce al writer tutte le informazioni necessarie sulla modalità di scrittura dei dati nel file. Il profilo non fornisce al writer informazioni sul formato degli esempi di input che l'applicazione recapita. I formati di input saranno sconosciuti solo per i flussi compressi con uno dei codec Windows Media. gli input per i tipi di flusso arbitrari sono prevedibili in base alle informazioni contenute nel profilo.

L'oggetto writer può comunicare con il codec per un flusso per determinare i tipi di input che è possibile usare. Vengono forniti metodi per enumerare i possibili tipi di input. È sempre necessario trovare il tipo di input che corrisponde al supporto di input enumerando i tipi supportati anziché impostare manualmente le proprietà del supporto di input. Per ulteriori informazioni, vedere [per enumerare i formati di input](to-enumerate-input-formats.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità di scrittura di file**](file-writing-features.md)
</dt> <dt>

[**Utilizzo degli input**](working-with-inputs.md)
</dt> </dl>

 

 




