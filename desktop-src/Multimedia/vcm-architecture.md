---
title: Architettura VCM
description: Architettura VCM
ms.assetid: cb0b036d-b8b1-4611-965f-08f932dbddb7
keywords:
- Video per Windows (VFW), architettura VCM
- VFW (video per Windows), architettura VCM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89b672c86053086f63127aae586517fac4906326
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331055"
---
# <a name="vcm-architecture"></a>Architettura VCM

VCM è un intermediario tra un'applicazione e i driver di compressione e decompressione. I driver di compressione e decompressione comprimeno e decomprimeno singoli frame di dati.

Quando un'applicazione effettua una chiamata a VCM, VCM converte la chiamata in un messaggio. Il messaggio viene inviato tramite la funzione [**ICSendMessage**](/windows/desktop/api/Vfw/nf-vfw-icsendmessage) al commediatore o al decompressore appropriato, che comprime o decomprime i dati. VCM riceve il valore restituito dal driver di compressione o decompressione e quindi restituisce il controllo all'applicazione.

Se una macro viene definita per un messaggio, la macro si espande in una chiamata di funzione **ICSendMessage** che fornisce parametri appropriati per il messaggio. Se viene definita una macro per un messaggio, l'applicazione deve utilizzarla anziché il messaggio. In questa panoramica queste macro seguono i messaggi tra parentesi.

 

 




