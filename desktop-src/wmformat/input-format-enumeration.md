---
title: Enumerazione del formato di input
description: Enumerazione del formato di input
ms.assetid: 75264598-0226-435a-b71f-6997ff0fcaff
keywords:
- Windows Media Format SDK, enumerazioni del formato di input
- Windows Media Format SDK, enumerazione dei formati di input
- Advanced Systems Format (ASF), enumerazioni del formato di input
- ASF (Advanced Systems Format), enumerazioni del formato di input
- Advanced Systems Format (ASF), enumerazione dei formati di input
- ASF (Advanced Systems Format), enumerazione dei formati di input
- Enumerazioni del formato di input
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a261b2edae285a970bead5d039c4e85076530eb363aa025289b75ec56618406
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809041"
---
# <a name="input-format-enumeration"></a>Enumerazione del formato di input

L'oggetto writer ottiene le informazioni sul formato del flusso dal profilo specificato. Le informazioni di configurazione del flusso in un profilo fornisce al writer tutte le informazioni necessarie sulla modalità di scrittura dei dati nel file. Il profilo non fornisce al writer informazioni sul formato degli esempi di input forniti dall'applicazione. I formati di input saranno sconosciuti solo per i flussi compressi con uno dei codec Windows media; Gli input per i tipi di flusso arbitrari sono prevedibili in base alle informazioni nel profilo.

L'oggetto writer può comunicare con il codec per un flusso per determinare i tipi di input che possono essere usati. Vengono forniti metodi per enumerare i tipi di input possibili. È sempre necessario trovare il tipo di input che corrisponde al supporto di input enumerando i tipi supportati anziché impostando manualmente le proprietà dei supporti di input. Per altre informazioni, vedere [Per enumerare i formati di input.](to-enumerate-input-formats.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità di scrittura di file**](file-writing-features.md)
</dt> <dt>

[**Uso degli input**](working-with-inputs.md)
</dt> </dl>

 

 




