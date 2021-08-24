---
title: Tunnel Modalità
description: Lo scenario Tunnel criteri IPsec in modalità rete viene usato per applicare la protezione in modalità tunnel IPsec per tutto il traffico corrispondente tra due endpoint del tunnel.
ms.assetid: 170046c5-28ec-4341-89e2-93494bf9c6b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbac16de0dc01bc37e0e4f4b997d00d19339de021ffce66a0d3cf6957addbe90
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119639071"
---
# <a name="tunnel-mode"></a>Tunnel Modalità

Lo scenario Tunnel criteri IPsec in modalità rete viene usato per applicare la protezione in modalità tunnel IPsec per tutto il traffico corrispondente tra due endpoint del tunnel.

Questo scenario di criteri viene in genere usato per proteggere il traffico tra più subnet della succursale, quando viene inoltrato tra i gateway corrispondenti su Internet. Può anche essere usato per proteggere la comunicazione end-to-end tra due computer host, definiti anche tunnel da punto a punto.

Per implementare criteri in modalità Tunnel usando Windows Filtering Platform (WFP), chiamare la funzione [**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) che crea un'istanza dei filtri della modalità tunnel appropriati ai livelli appropriati per conto del chiamante. Il chiamante deve specificare la modalità principale, i contesti del provider in modalità rapida e le condizioni di filtro che descrivono il traffico che deve essere protetto all'interno del tunnel.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codice di esempio: uso della Tunnel predefinita](using-tunnel-mode.md)
</dt> <dt>

[**Filtro degli identificatori dei livelli**](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

 




