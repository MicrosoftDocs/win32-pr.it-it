---
title: Esecuzione di query per informazioni dettagliate sui diritti
description: Esecuzione di query per informazioni dettagliate sui diritti
ms.assetid: d9d5c299-1f61-41df-ab2c-7f4d196e9290
keywords:
- Windows Media Format SDK, esecuzione di query per i diritti dettagliati
- Windows Media Format SDK, query sui diritti dettagliati
- Digital Rights Management (DRM), esecuzione di query per i diritti dettagliati
- DRM (Digital Rights Management), esecuzione di query per i diritti dettagliati
- Digital Rights Management (DRM), query sui diritti dettagliati
- DRM (Digital Rights Management), query sui diritti dettagliati
- API estese del client DRM, esecuzione di query per i diritti dettagliati
- API estese del client, esecuzione di query per i diritti dettagliati
- API estese del client DRM, query sui diritti dettagliati
- API estese client, query con diritti dettagliati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3a21fa974f0289c4e4e8983ee6d4fd1757de824
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221530"
---
# <a name="querying-for-detailed-rights-information"></a>Esecuzione di query per informazioni dettagliate sui diritti

Usando il metodo [**IWMDRMLicenseQuery:: QueryLicenseState**](iwmdrmlicensequery-querylicensestate.md) , è possibile ottenere informazioni dettagliate sui diritti concessi dalle licenze per un ID chiave. Le informazioni che si ottengono da questo metodo vengono aggregate da tutte le licenze nell'archivio licenze locale che si applicano all'ID chiave specificato.

**QueryLicenseState** usa la [**struttura \_ \_ \_ dei dati di stato delle licenze DRM**](drmdrm-license-state-data.md) per visualizzare informazioni aggregate su tutte le licenze per l'ID chiave specificato. Questo utilizzo è diverso rispetto ad altri oggetti in Windows Media Format SDK.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Recupero di informazioni dalle licenze nell'archivio licenze locale**](getting-information-from-licenses-in-the-local-license-store.md)
</dt> </dl>

 

 




