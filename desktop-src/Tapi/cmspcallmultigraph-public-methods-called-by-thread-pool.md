---
description: Nell'elenco seguente sono inclusi i metodi pubblici CMSPCallMultiGraph chiamati dal pool di thread.
ms.assetid: f0a5f621-99c4-40f0-8a0e-0e43792e00a1
title: Metodi pubblici CMSPCallMultiGraph, chiamati dal pool di thread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3878298024164a4c940b96dceb88e0ff005d59ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312721"
---
# <a name="cmspcallmultigraph-public-methods-called-by-thread-pool"></a>Metodi pubblici CMSPCallMultiGraph, chiamati dal pool di thread



| Metodi pubblici CMSPCallMultiGraph                                   | Descrizione                                                                                                                                                                                              |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DispatchGraphEvent**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-dispatchgraphevent) | Chiamato quando il grafico del filtro segnala un evento.                                                                                                                                                           |
| [**HandleGraphEvent**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-handlegraphevent)     | Chiamato dal metodo statico [**DispatchGraphEvent**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-dispatchgraphevent) . Code [**ProcessGraphEvent**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-processgraphevent) nel thread di lavoro msp principale. |
| [**ProcessGraphEvent**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-processgraphevent)   | Consente all'istanza dell'oggetto chiamata MSP di gestire l'evento Filter Graph.                                                                                                                                    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**CMSPCallMultiGraph**](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallmultigraph)
</dt> </dl>

 

 



