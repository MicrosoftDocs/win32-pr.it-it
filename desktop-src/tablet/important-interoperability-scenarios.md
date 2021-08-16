---
description: "Per un'applicazione Tablet PC che funziona con l'input penna in modo efficace, l'applicazione deve essere in grado di:"
ms.assetid: 64a7b773-35c9-42f7-aec4-7fed34fa84d9
title: Scenari di interoperabilità importanti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b42f021cd1a8dbb3a8b65780b71db66a4c43fa18097f967f794c1a2b2c3ce16b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118718960"
---
# <a name="important-interoperability-scenarios"></a>Scenari di interoperabilità importanti

Per un'applicazione Tablet PC che funziona con l'input penna in modo efficace, l'applicazione deve essere in grado di:

-   Salvare un documento nel formato binario nativo dell'applicazione senza perdere l'input penna del documento.
-   Salvare un documento in qualsiasi formato supportato normalmente dall'applicazione (ad esempio, HTML o RTF (Rich Text Format) senza perdere l'input penna del documento.
-   Copiare l'input penna da un'applicazione a un'altra usando gli Appunti. Questa operazione funziona se l'altra applicazione riconosce solo un formato specifico, ad esempio HTML, RTF o bitmap (BMP). Funziona anche se l'applicazione di destinazione riconosce l'input penna. Se riconosce l'input penna, l'applicazione di destinazione è in grado di interpretare l'input penna copiato come input penna e non solo come immagine.
-   Copiare l'input penna, insieme al testo, tra due applicazioni che riconoscono l'input penna, ognuna delle quali ha più di un [**oggetto Ink.**](inkdisp-class.md) Questa operazione richiede HTML, RTF o un formato simile.
-   Copiare l'input penna tra due applicazioni, ognuna delle quali ha un [**oggetto Ink.**](inkdisp-class.md) Ink Serialized Format (ISF) è sufficiente a questo scopo.
-   Copiare l'input penna da un'applicazione che dispone di più di un [**oggetto Ink**](inkdisp-class.md) in un'applicazione con un solo oggetto **Ink.** In questo caso, l'applicazione con più di un oggetto **Ink** deve essere in grado di produrre Ink Serialized Format (ISF).
-   Copiare l'input penna da un'applicazione che dispone [**di un oggetto Ink**](inkdisp-class.md) in un'applicazione con più di un oggetto **Ink.** In questo caso, l'applicazione con più di un **oggetto Ink** deve essere in grado di riconoscere ISF.

 

 



