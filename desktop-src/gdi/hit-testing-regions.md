---
description: Un'applicazione esegue l'hit testing sulle aree per determinare le coordinate della posizione corrente del cursore.
ms.assetid: 861a2558-0967-43f6-be3f-580992da05ff
title: Aree di hit testing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5734ffb886bd2978d3ee0b49773d752d4abf43a4d98dc060f3dfaf2956e3084a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118760977"
---
# <a name="hit-testing-regions"></a>Aree di hit testing

Un'applicazione esegue l'hit testing sulle aree per determinare le coordinate della posizione corrente del cursore. Passa quindi queste coordinate e un handle che identifica l'area alla [**funzione PtInRegion.**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion) Le coordinate del cursore possono essere recuperate elaborando i vari messaggi del mouse, ad esempio [**WM \_ LBUTTONDOWN,**](../inputdev/wm-lbuttondown.md) [**WM \_ LBUTTONUP,**](../inputdev/wm-lbuttonup.md) [**WM \_ RBUTTONDOWN**](../inputdev/wm-rbuttondown.md) e [**WM \_ RBUTTONUP.**](../inputdev/wm-rbuttonup.md) Il valore restituito per PtInRegion indica se la posizione del cursore si trova all'interno dell'area specificata.

 

 
