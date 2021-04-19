---
description: Un thread può, in qualsiasi momento, chiamare WSAIsBlocking per determinare se una chiamata di blocco è attualmente in corso.
ms.assetid: 6213ded4-feab-404f-86a0-3db9a0a42769
title: Annullamento di operazioni di blocco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 502870b8935dc97c1d6c3714808d1c6532780f7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307024"
---
# <a name="canceling-blocking-operations"></a>Annullamento di operazioni di blocco

Un thread può, in qualsiasi momento, chiamare [WSAIsBlocking](/windows/desktop/api/winsock2/nf-winsock2-wsaisblocking) per determinare se una chiamata di blocco è attualmente in corso. Questa funzione è implementata all'interno degli shim di compatibilità di Windows Sockets 1,1 e pertanto non ha alcuna controparte SPI. Ovviamente questo è possibile solo quando il provider di servizi utilizza un pseudo blocco, invece del blocco effettivo. Quando necessario, è possibile chiamare [**WSPCancelBlockingCall**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85)) in qualsiasi momento per annullare qualsiasi operazione di pseudo blocco corrente.

 

 
