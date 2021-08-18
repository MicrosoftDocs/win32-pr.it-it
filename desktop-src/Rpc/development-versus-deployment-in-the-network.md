---
title: Sviluppo e distribuzione in rete
description: La maggior parte degli sviluppatori scrive e testa il proprio software su una rete LAN veloce e affidabile.
ms.assetid: 9458162c-1046-4554-bafa-b455f2957d58
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70ff9da31ecd80b9e0a699d9ec0eb450e885a423b9380b85e2015e9ef7c1af7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930621"
---
# <a name="development-vs-deployment-in-the-network"></a>Sviluppo e distribuzione in rete

La maggior parte degli sviluppatori scrive e testa il proprio software su una rete LAN veloce e affidabile. Il client e il server si trovano spesso nello stesso segmento di rete. In tali circostanze la rete raramente non risponde e la connettività raramente si perde. Quando vengono distribuiti in un ambiente del cliente, tuttavia, client e server si trovano spesso in segmenti di rete diversi, possibilmente geograficamente remoti, e il server è molto caricato con altri client. In altre parole, non è possibile presunirsi la velocità di risposta della rete.

Questo articolo illustra come costruire architetture client/server affidabili di fronte all'incertezza introdotta da una rete intrinsecamente inaffidabile e da server potenzialmente non disponibili.

 

 




