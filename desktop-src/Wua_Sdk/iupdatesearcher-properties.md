---
description: L'interfaccia IUpdateSearcher definisce le proprietà seguenti.
ms.assetid: 65a39383-f326-4735-b2af-6df7a77ffba6
title: Proprietà di IUpdateSearcher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5dc3af2635fff4260a44261333b23cbfcf1661793ad613f08bb288db452b93d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130433"
---
# <a name="iupdatesearcher-properties"></a>Proprietà di IUpdateSearcher

[**L'interfaccia IUpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) definisce le proprietà seguenti.



| Proprietà                                                                                           | Descrizione                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CanAutomaticallyUpgradeService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_canautomaticallyupgradeservice)            | Ottiene e imposta un valore booleano che indica se le future chiamate ai metodi [**BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch) e [**Search**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-search) comportano un aggiornamento automatico a Windows Update Agent (WUA). |
| [**ClientApplicationID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_clientapplicationid)                                  | Identifica l'applicazione client corrente.                                                                                                                                                                                                   |
| [**IncludePotentiallySupersedEdUpdates**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_includepotentiallysupersededupdates) | Ottiene e imposta un valore booleano che indica se i risultati della ricerca includono aggiornamenti sostituiti da altri aggiornamenti nei risultati della ricerca.                                                                                          |
| [**Online**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_online)                                                            | Ottiene e imposta un valore booleano che indica se [**UpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) passa alla modalità online per cercare gli aggiornamenti.                                                                                                        |
| [**ID servizio**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_serviceid)                                                      | Ottiene e imposta un sito in cui eseguire la ricerca quando il sito in cui eseguire la ricerca non è Windows sito di aggiornamento.                                                                                                                                                         |
| [**Selezione server**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_serverselection)                                          | Ottiene e imposta un [**valore ServerSelection**](/openspecs/windows_protocols/ms-uamg/07e2bfa4-6795-4189-b007-cc50b476181a) che indica il server in cui cercare gli aggiornamenti.                                                                                                                            |




 

 

 



