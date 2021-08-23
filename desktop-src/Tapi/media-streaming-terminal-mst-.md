---
description: Il terminale di streaming multimediale (MST) è un terminale dinamico basato sull'uso DirectShow filtri. Un msp scritto usando le classi di base MSP TAPI 3 incorporerà un MST, ma gli autori di MSP possono scegliere di implementarla senza usare le classi di base.
ms.assetid: 21015c33-2ad1-4472-b346-167953d06a21
title: Terminale di streaming multimediale (MST)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8eeb9ad231c114ca18b4dea0926b861360ab5a359cd9ee8c48fd1c388a941a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002909"
---
# <a name="media-streaming-terminal-mst"></a>Terminale di streaming multimediale (MST)

Il terminale di streaming multimediale (MST) è un terminale dinamico basato sull'uso DirectShow filtri. Un msp scritto usando le classi di [base MSP TAPI 3](tapi-3-msp-base-classes.md) incorporerà un MST, ma gli autori msp possono scegliere di implementarla senza usare le classi di base.

Per richiamare la creazione MST, un'applicazione effettua una chiamata a [**ITTerminalSupport::CreateTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal) usando *pTerminalClass* impostato su CLSID \_ MediaStreamTerminal.

Le [**interfacce ITAMMediaFormat**](/windows/win32/api/tapi3/nn-tapi3-itammediaformat) [**e ITAllocatorProperties**](/windows/win32/api/tapi3/nn-tapi3-itallocatorproperties) vengono quindi esposte nel terminale, consentendo a un'applicazione di ottimizzare le prestazioni di streaming. Queste interfacce vengono dichiarate in Tapi3.h.

L'implementazione e l'uso di una MST richiedono familiarità con DirectShow e la gestione dei grafi dei filtri. Fare riferimento al materiale DirectShow nel nodo Servizi grafici e multimediali di Platform Software Development Kit (SDK). Le informazioni di riferimento sul flusso multimediale saranno particolarmente utili per gli autori MSP.

 

 
