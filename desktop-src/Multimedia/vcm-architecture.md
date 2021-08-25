---
title: Architettura di VCM
description: Architettura di VCM
ms.assetid: cb0b036d-b8b1-4611-965f-08f932dbddb7
keywords:
- Video per Windows (VFW), architettura di VCM
- VFW (Video per Windows),Architettura di VCM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7676fe7786b8674ddca957a75c33336294b65a9df18d53fe4b9c7f493092b66f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135599"
---
# <a name="vcm-architecture"></a>Architettura di VCM

VCM è un intermediario tra un'applicazione e i driver di compressione e decompressione. I driver di compressione e decompressione comprimeno e decomprimeno singoli fotogrammi di dati.

Quando un'applicazione esegue una chiamata a VCM, VCM converte la chiamata in un messaggio. Il messaggio viene inviato tramite la [**funzione ICSendMessage**](/windows/desktop/api/Vfw/nf-vfw-icsendmessage) al compressore o decompressore appropriato, che comprime o decomprime i dati. VCM riceve il valore restituito dal driver di compressione o decompressione e quindi restituisce il controllo all'applicazione.

Se per un messaggio è definita una macro, la macro si espande in una chiamata di funzione **ICSendMessage** che fornisce i parametri appropriati per il messaggio. Se per un messaggio è definita una macro, l'applicazione deve usarla anziché il messaggio. In questa panoramica, queste macro seguono i messaggi tra parentesi.

 

 




