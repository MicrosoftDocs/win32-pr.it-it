---
description: Media streaming Terminal (MST) è un terminale dinamico basato sull'utilizzo di filtri DirectShow. Un MSP scritto usando le classi base MSP di TAPI 3 includerà un'MST, ma gli autori MSP potranno scegliere di implementarla senza usare le classi base.
ms.assetid: 21015c33-2ad1-4472-b346-167953d06a21
title: Media streaming Terminal (MST)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2afb9bb4b97d0e741aec96454b187beefe2d21eb
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103968908"
---
# <a name="media-streaming-terminal-mst"></a>Media streaming Terminal (MST)

Media streaming Terminal (MST) è un terminale dinamico basato sull'utilizzo di filtri DirectShow. Un MSP scritto usando le [classi base msp di TAPI 3](tapi-3-msp-base-classes.md) includerà un'MST, ma gli autori msp potranno scegliere di implementarla senza usare le classi base.

Per richiamare la creazione dell'MST, un'applicazione effettua una chiamata a [**ITTerminalSupport:: CreateTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal) usando *PTERMINALCLASS* impostato su CLSID \_ MediaStreamTerminal.

Le interfacce [**ITAMMediaFormat**](/windows/win32/api/tapi3/nn-tapi3-itammediaformat) e [**ITAllocatorProperties**](/windows/win32/api/tapi3/nn-tapi3-itallocatorproperties) vengono quindi esposte nel terminale, consentendo a un'applicazione di ottimizzare le prestazioni di streaming. Queste interfacce sono dichiarate in Tapi3. h.

Per l'implementazione e l'uso di un'MST è necessaria una certa familiarità con i filtri DirectShow e la gestione dei filtri. Vedere il materiale DirectShow sotto il nodo grafico e servizi multimediali della piattaforma Software Development Kit (SDK). Il riferimento al flusso multimediale sarà particolarmente utile per gli autori MSP.

 

 
