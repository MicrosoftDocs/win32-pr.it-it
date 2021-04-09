---
title: Sviluppo rispetto alla distribuzione in rete
description: La maggior parte degli sviluppatori scrive e testa il software in una LAN affidabile veloce.
ms.assetid: 9458162c-1046-4554-bafa-b455f2957d58
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a83210db66133329d6c6b38b67ec7ecb29c0595
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044590"
---
# <a name="development-vs-deployment-in-the-network"></a>Sviluppo rispetto alla distribuzione in rete

La maggior parte degli sviluppatori scrive e testa il software in una LAN affidabile veloce. Il client e il server sono spesso nello stesso segmento di rete. In questi casi la rete non risponde raramente e la connettività si interrompe raramente. Quando vengono distribuiti in un ambiente cliente, tuttavia, il client e il server si trovano spesso in segmenti di rete diversi, possibilmente geograficamente remoti, e il server viene caricato molto con altri client. In altre parole, non è possibile presupporre la velocità di risposta della rete.

In questo articolo viene illustrato come costruire solide architetture client/server in presenza di incertezze introdotte da una rete intrinsecamente inaffidabile e da server potenzialmente non disponibili.

 

 




