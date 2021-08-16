---
title: Funzioni di callback Yield
description: Funzioni di callback Yield
ms.assetid: 8c9b43ea-fdba-41a2-ba2d-1eaa4516e14f
keywords:
- Funzioni di callback AVICap, yield
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e87a3c986378bee05078b8cab28a0647827a1102ef1809558a47dcd5123af2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118369135"
---
# <a name="yield-callback-functions"></a>Funzioni di callback Yield

Le applicazioni possono usare funzioni di callback yield durante l'acquisizione di streaming. Una funzione di callback yield è in genere costituita da un ciclo di messaggi che chiama [PeekMessage,](/windows/win32/api/winuser/nf-winuser-peekmessagea) [TranslateMessage](/windows/win32/api/winuser/nf-winuser-translatemessage)e [DispatchMessage.](/windows/win32/api/winuser/nf-winuser-dispatchmessage) La finestra di acquisizione chiama la funzione di callback yield almeno una volta per ogni fotogramma video acquisito, ma la frequenza esatta dipende dalla frequenza dei fotogrammi e dall'overhead del driver di acquisizione e del disco.

 

 