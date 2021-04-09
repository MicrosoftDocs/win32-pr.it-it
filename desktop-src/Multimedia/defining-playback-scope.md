---
title: Definizione dell'ambito di riproduzione
description: Definizione dell'ambito di riproduzione
ms.assetid: f2563226-7af1-4cb3-b468-c59738feeda2
keywords:
- MCIWndPlayFrom (macro)
- MCIWndPlayTo (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 518fc80588147c4ccbbca619452b714333a8a34d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955443"
---
# <a name="defining-playback-scope"></a>Definizione dell'ambito di riproduzione

MCIWnd fornisce macro che consentono di definire l' *ambito* di riproduzione. L'ambito è la parte della riproduzione che si desidera riprodurre. Ad esempio, è possibile riprodurre il contenuto da una posizione diversa dalla posizione iniziale usando la macro [**MCIWndPlayFrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom) . Questa macro viene spostata nella posizione specificata, inizia la riproduzione e continua fino alla fine del contenuto. Analogamente, è possibile riprodurre il contenuto in un endpoint specificato utilizzando la macro [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) . Questa macro inizia in corrispondenza della posizione di riproduzione corrente e viene riprodotta fino a quando non raggiunge la posizione specificata o viene raggiunta la fine del contenuto, a seconda di quale si verifica per primo.

Inoltre, è possibile definire le posizioni iniziale e finale usando la macro [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) . Questa macro viene spostata nella posizione iniziale specificata e viene riprodotta fino a quando non viene raggiunta la posizione finale specificata o la fine del contenuto.

 

 




