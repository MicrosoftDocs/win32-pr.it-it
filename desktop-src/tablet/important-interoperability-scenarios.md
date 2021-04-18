---
description: "Affinché un'applicazione Tablet PC funzioni con l'input penna in modo efficace, l'applicazione deve essere in grado di:"
ms.assetid: 64a7b773-35c9-42f7-aec4-7fed34fa84d9
title: Scenari di interoperabilità importanti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6dca3bcbf52d673131122615fa5a08317dbf10c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306062"
---
# <a name="important-interoperability-scenarios"></a>Scenari di interoperabilità importanti

Affinché un'applicazione Tablet PC funzioni con l'input penna in modo efficace, l'applicazione deve essere in grado di:

-   Salvare un documento nel formato binario nativo dell'applicazione senza perdere l'input penna del documento.
-   Salvare un documento in qualsiasi formato supportato normalmente dall'applicazione, ad esempio HTML o RTF (Rich Text Format) senza perdere l'input penna del documento.
-   Copiare l'input penna da un'applicazione a un'altra usando gli Appunti. Questa operazione funziona se l'altra applicazione riconosce solo un formato specifico, ad esempio HTML, RTF o bitmap (BMP). Funziona anche se l'applicazione di destinazione riconosce l'input penna. Se riconosce l'input penna, l'applicazione di destinazione è in grado di interpretare l'input penna copiato come input penna e non solo come immagine.
-   Copiare l'input penna, insieme al testo, tra due applicazioni che riconoscono l'input penna, ognuna delle quali contiene più di un oggetto [**input penna**](inkdisp-class.md) . Questa operazione richiede un formato HTML, RTF o simile.
-   Copiare l'input penna tra due applicazioni, ognuna con un oggetto [**input penna**](inkdisp-class.md) . Il formato ISF (Ink Serialized Format) è sufficiente per questa operazione.
-   Copiare l'input penna da un'applicazione che dispone di più di un oggetto [**input penna**](inkdisp-class.md) in un'applicazione che dispone di un solo oggetto **input penna** . In questo caso, l'applicazione con più di un oggetto **input penna** deve essere in grado di produrre il formato ISF (Ink Serialized Format).
-   Copiare l'input penna da un'applicazione che dispone di un oggetto [**input penna**](inkdisp-class.md) in un'applicazione con più di un oggetto **input penna** . In questo caso, l'applicazione che dispone di più di un oggetto **Ink** deve essere in grado di riconoscere ISF.

 

 



