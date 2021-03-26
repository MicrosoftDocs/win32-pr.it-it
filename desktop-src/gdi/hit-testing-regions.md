---
description: Un'applicazione esegue l'hit test sulle aree per determinare le coordinate della posizione corrente del cursore.
ms.assetid: 861a2558-0967-43f6-be3f-580992da05ff
title: Aree di hit testing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe136c3ba9ab4babfc1150ae4c3eee878cb42327
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226691"
---
# <a name="hit-testing-regions"></a>Aree di hit testing

Un'applicazione esegue l'hit test sulle aree per determinare le coordinate della posizione corrente del cursore. Passa quindi queste coordinate e un handle che identifica l'area alla funzione [**PtInRegion**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion) . Le coordinate del cursore possono essere recuperate elaborando i vari messaggi del mouse, ad esempio [**WM \_ LBUTTONDOWN**](../inputdev/wm-lbuttondown.md) , [**WM \_ LBUTTONUP**](../inputdev/wm-lbuttonup.md) , [**WM \_ RBUTTONDOWN**](../inputdev/wm-rbuttondown.md) e [**WM \_ RBUTTONUP**](../inputdev/wm-rbuttonup.md). Il valore restituito per PtInRegion indica se la posizione del cursore si trova all'interno dell'area specificata.

 

 
