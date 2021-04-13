---
description: L'interfaccia IUpdateSearcher definisce le proprietà seguenti.
ms.assetid: 65a39383-f326-4735-b2af-6df7a77ffba6
title: Proprietà di IUpdateSearcher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c777c2489afe10f73c41badfb346053aefad7022
ms.sourcegitcommit: aab10824ee4883c70e1afba428b679a17915a5aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/11/2021
ms.locfileid: "104354016"
---
# <a name="iupdatesearcher-properties"></a>Proprietà di IUpdateSearcher

L'interfaccia [**IUpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) definisce le proprietà seguenti.



| Proprietà                                                                                           | Descrizione                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CanAutomaticallyUpgradeService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_canautomaticallyupgradeservice)            | Ottiene e imposta un valore booleano che indica se le chiamate future ai metodi [**BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch) e [**Search**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-search) generano un aggiornamento automatico a Windows Update Agent (WUA). |
| [**ClientApplicationID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_clientapplicationid)                                  | Identifica l'applicazione client corrente.                                                                                                                                                                                                   |
| [**IncludePotentiallySupersededUpdates**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_includepotentiallysupersededupdates) | Ottiene e imposta un valore booleano che indica se i risultati della ricerca includono gli aggiornamenti sostituiti da altri aggiornamenti nei risultati della ricerca.                                                                                          |
| [**Online**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_online)                                                            | Ottiene e imposta un valore booleano che indica se [**UpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) passa online per la ricerca degli aggiornamenti.                                                                                                        |
| [**ServiceID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_serviceid)                                                      | Ottiene e imposta un sito in cui eseguire la ricerca quando il sito in cui eseguire la ricerca non è un sito Windows Update.                                                                                                                                                         |
| [**ServerSelection**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_serverselection)                                          | Ottiene e imposta un valore [**ServerSelection**](/openspecs/windows_protocols/ms-uamg/07e2bfa4-6795-4189-b007-cc50b476181a) che indica il server in cui cercare gli aggiornamenti.                                                                                                                            |




 

 

 



