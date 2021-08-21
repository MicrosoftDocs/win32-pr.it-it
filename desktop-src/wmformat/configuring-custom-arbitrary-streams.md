---
title: Configurazione di modelli arbitrari personalizzati Flussi
description: Configurazione di modelli arbitrari personalizzati Flussi
ms.assetid: 09b28fd3-a0a3-44d9-b664-7421290abf02
keywords:
- flussi, configurazione di flussi arbitrari personalizzati
- codec, configurazione di flussi arbitrari personalizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b9b98b25ae9f973682ee3987ed8b590d485288e72e0b5ef7977eb7f3da0d1da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809811"
---
# <a name="configuring-custom-arbitrary-streams"></a>Configurazione di modelli arbitrari personalizzati Flussi

Quando si usa un tipo di dati arbitrario personalizzato, è necessario creare un valore GUID da usare come identificatore del tipo di supporto principale. Quando il writer rileva un flusso in un profilo con un tipo principale che non riconosce, presuppone che il flusso sia dati arbitrari personalizzati. Accetta gli esempi, li in pacchetto e li combina con gli esempi degli altri flussi nel file senza verificare i dati in alcun modo.

È anche possibile creare identificatori GUID di sottotipo personalizzati per definire sottocategorie dei dati personalizzati. Il writer ignorerà completamente questi sottotipi, ma verranno mantenuti nella sezione di intestazione del file ASF, in modo che l'applicazione di lettura possa recuperarli e prendere decisioni in base a essi.

Un flusso arbitrario richiede una velocità in bit e una finestra del buffer e deve avere una struttura [**MEDIA \_ \_ TYPE WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) con i valori cancellati, ad eccezione del tipo di supporto principale e del sottotipo (se ne usa uno).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Configurazione comune a tutti Flussi**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configurazione di tipi di flusso arbitrari**](configuring-arbitrary-stream-types.md)
</dt> <dt>

[**Dati arbitrari personalizzati Flussi**](custom-arbitrary-data-streams.md)
</dt> </dl>

 

 




