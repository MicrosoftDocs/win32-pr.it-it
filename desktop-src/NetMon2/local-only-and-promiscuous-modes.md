---
description: I monitoraggi possono esaminare i frame in modalità solo locale o promiscua.
ms.assetid: 4646f5bb-e3e3-4929-91b7-f68c5b70ccb3
title: Modalità di Local-Only e promiscuità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd1188760d8de31836de3fbd437854a5df138402
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307718"
---
# <a name="local-only-and-promiscuous-modes"></a>Modalità di Local-Only e promiscuità

I monitoraggi possono esaminare i frame in modalità solo locale o promiscua.

In modalità solo locale, il provider di pacchetti di rete (NPP) restituisce i frame che vengono inviati a o dal computer in cui è in esecuzione il monitoraggio, incluse le trasmissioni e i multicast indirizzati al computer locale. Anche se limitato ai frame diretti localmente, la modalità locale è molto meno complessa.

In modalità promiscua, il monitoraggio può anche controllare il traffico non indirizzato al o dal computer locale. A meno che il monitoraggio non abbia specificato il flag, MCS \_ Create \_ pmode \_ non è \_ necessario nella funzione [OnLoadingDLL](onloadingdll.md) , il servizio di controllo di monitoraggio (MCSVC) presuppone che il monitoraggio richieda la modalità promiscua quando carica la dll di monitoraggio.

 

 



