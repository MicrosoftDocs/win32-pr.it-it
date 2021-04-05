---
title: Configurazione di flussi arbitrari personalizzati
description: Configurazione di flussi arbitrari personalizzati
ms.assetid: 09b28fd3-a0a3-44d9-b664-7421290abf02
keywords:
- flussi, configurazione di flussi arbitrari personalizzati
- codec, configurazione di flussi arbitrari personalizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29d5cf3e95a5514ddeede9eb3c25df01ed4cd2ae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710162"
---
# <a name="configuring-custom-arbitrary-streams"></a>Configurazione di flussi arbitrari personalizzati

Quando si usa un tipo di dati arbitrario personalizzato, è necessario creare un valore GUID che funga da identificatore principale del tipo di supporto. Quando il writer rileva un flusso in un profilo con un tipo principale non riconosce, presuppone che il flusso sia dati arbitrari personalizzati. Accetta gli esempi, li packetize e li combina con esempi dagli altri flussi del file senza verificare i dati in alcun modo.

È anche possibile creare identificatori GUID di sottotipo personalizzati per definire sottocategorie dei dati personalizzati. Il writer ignorerà completamente questi sottotipi, ma verrà mantenuto nella sezione di intestazione del file ASF, in modo che l'applicazione di lettura possa recuperarli e prendere decisioni in base a tali sottotipi.

Un flusso arbitrario richiede una velocità in bit e una finestra del buffer e deve avere una struttura di [**\_ \_ tipo di supporto WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) con i valori deselezionati, ad eccezione del tipo di supporto principale e del sottotipo (se ne viene usato uno).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Configurazione comune a tutti i flussi**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configurazione di tipi di flusso arbitrari**](configuring-arbitrary-stream-types.md)
</dt> <dt>

[**Flussi di dati arbitrari personalizzati**](custom-arbitrary-data-streams.md)
</dt> </dl>

 

 




