---
description: Un thread può, in qualsiasi momento, chiamare WSAIsBlocking per determinare se è in corso o meno una chiamata di blocco.
ms.assetid: 6213ded4-feab-404f-86a0-3db9a0a42769
title: Annullamento di operazioni di blocco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5064948fe7c1c1262acb9f4f8ef25a3ad3e721e77a188f313541595ef75f9ce9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030691"
---
# <a name="canceling-blocking-operations"></a>Annullamento di operazioni di blocco

Un thread può, in qualsiasi momento, chiamare [WSAIsBlocking](/windows/desktop/api/winsock2/nf-winsock2-wsaisblocking) per determinare se è in corso o meno una chiamata di blocco. Questa funzione viene implementata all'interno degli s shims di compatibilità Windows Sockets 1.1 e pertanto non ha controparti SPI. Ovviamente questo è possibile solo quando il provider di servizi utilizza uno pseudo-blocco, anziché un vero blocco. Quando necessario, [**WSPCancelBlockingCall**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85)) può essere chiamato in qualsiasi momento per annullare qualsiasi operazione pseudo-bloccante corrente.

 

 
