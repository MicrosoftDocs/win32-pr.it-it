---
description: I monitoraggi possono esaminare i frame in modalità solo locale o promiscua.
ms.assetid: 4646f5bb-e3e3-4929-91b7-f68c5b70ccb3
title: Local-Only modalità promiscue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8155c968f82154712ec8926f114e63380cdb1099bf7908d5a4dde86d7646dc20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555891"
---
# <a name="local-only-and-promiscuous-modes"></a>Local-Only modalità promiscue

I monitoraggi possono esaminare i frame in modalità solo locale o promiscua.

In modalità solo locale, il provider di pacchetti di rete (NPP) restituisce i fotogrammi inviati a o dal computer in cui è in esecuzione il monitoraggio, inclusi broadcast e multicast indirizzati al computer locale. Anche se limitato ai frame indirizzati localmente, anche la modalità locale è molto meno intensiva del processore.

In modalità promiscua, il monitoraggio può anche controllare il traffico non indirizzato verso o dal computer locale. A meno che il monitoraggio non abbia specificato il flag MCS CREATE PMODE NOT REQUIRED, nella funzione \_ \_ \_ \_ [OnLoadingDLL](onloadingdll.md) il servizio di controllo di monitoraggio (MCSVC) presuppone che il monitoraggio richieda la modalità promiscua quando carica la DLL del monitoraggio.

 

 



