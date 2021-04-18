---
title: Modalità tunnel
description: Lo scenario dei criteri IPsec in modalità tunnel viene usato per applicare la protezione in modalità tunnel IPsec per tutto il traffico corrispondente tra due endpoint del tunnel.
ms.assetid: 170046c5-28ec-4341-89e2-93494bf9c6b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a75fdecb7f959a2f95aae2649a6e3f8f94def9b3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331303"
---
# <a name="tunnel-mode"></a>Modalità tunnel

Lo scenario dei criteri IPsec in modalità tunnel viene usato per applicare la protezione in modalità tunnel IPsec per tutto il traffico corrispondente tra due endpoint del tunnel.

Questo scenario di criteri viene in genere usato per proteggere il traffico tra più subnet dell'ufficio, quando viene inviato tra i gateway corrispondenti in Internet. Può anche essere usato per proteggere la comunicazione end-to-end tra due computer host, detti anche tunnel da punto a punto.

Per implementare i criteri in modalità tunnel utilizzando Windows Filtering Platform (WFP), chiamare la funzione [**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) che crea un'istanza dei filtri in modalità tunnel appropriati ai livelli appropriati per conto del chiamante. Il chiamante deve specificare la modalità principale, i contesti del provider in modalità rapida e le condizioni di filtro che descrivono il traffico che deve essere protetto all'interno del tunnel.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codice di esempio: uso della modalità tunnel](using-tunnel-mode.md)
</dt> <dt>

[**Filtraggio degli identificatori del livello**](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

 




