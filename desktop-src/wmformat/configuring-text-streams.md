---
title: Configurazione di flussi di testo
description: Configurazione di flussi di testo
ms.assetid: d99baac5-69e5-4e0a-9cd6-35b288d8181a
keywords:
- flussi, configurazione di flussi di testo
- codec, configurazione di flussi di testo
- flussi di testo, configurazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 460369eaae02f636f8ddda8bcca4f29ecfc2e1e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471302"
---
# <a name="configuring-text-streams"></a>Configurazione di flussi di testo

I flussi di testo sono essenzialmente uguali ai flussi arbitrari personalizzati. Non sono presenti informazioni di configurazione associate a un flusso di testo per identificare il tipo di codifica del testo, pertanto l'oggetto writer non è in grado di verificare gli esempi.

Per configurare un flusso di testo, è necessario assicurarsi che la struttura del [**\_ \_ tipo di supporto WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) contenga un tipo di supporto principale del \_ testo WMMEDIATYPE. È inoltre necessario impostare una velocità in bit e una finestra del buffer per il flusso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Calcolo dei valori della velocità in bit e della finestra del buffer per flussi arbitrari**](calculating-bit-rate-and-buffer-window-values-for-arbitrary-streams.md)
</dt> <dt>

[**Configurazione comune a tutti i flussi**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configurazione di tipi di flusso arbitrari**](configuring-arbitrary-stream-types.md)
</dt> <dt>

[**Flussi di testo**](text-streams.md)
</dt> </dl>

 

 




