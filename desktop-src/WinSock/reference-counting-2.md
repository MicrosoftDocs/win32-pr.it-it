---
description: Un processo può chiamare WSPCloseSocket su un socket duplicato e il descrittore verrà deallocato. Il socket sottostante, tuttavia, rimarrà aperto fino a quando non viene chiamato WSPCloseSocket sull'ultimo descrittore rimanente.
ms.assetid: dff1e932-5e87-4ec5-995d-686d20ba6236
title: Conteggio dei riferimenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c8cd281363636cc2022725b4921d3b2d2b300e7262173e157a2be1610f6af0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996661"
---
# <a name="reference-counting"></a>Conteggio dei riferimenti

Un processo può chiamare [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) su un socket duplicato e il descrittore verrà deallocato. Il socket sottostante, tuttavia, rimarrà aperto fino a quando non viene chiamato **WSPCloseSocket** sull'ultimo descrittore rimanente.

 

 
