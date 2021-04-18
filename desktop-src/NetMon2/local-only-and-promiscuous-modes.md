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
# <a name="local-only-and-promiscuous-modes"></a><span data-ttu-id="1d7d4-103">Modalità di Local-Only e promiscuità</span><span class="sxs-lookup"><span data-stu-id="1d7d4-103">Local-Only and Promiscuous Modes</span></span>

<span data-ttu-id="1d7d4-104">I monitoraggi possono esaminare i frame in modalità solo locale o promiscua.</span><span class="sxs-lookup"><span data-stu-id="1d7d4-104">Monitors can examine frames in local-only mode or promiscuous mode.</span></span>

<span data-ttu-id="1d7d4-105">In modalità solo locale, il provider di pacchetti di rete (NPP) restituisce i frame che vengono inviati a o dal computer in cui è in esecuzione il monitoraggio, incluse le trasmissioni e i multicast indirizzati al computer locale.</span><span class="sxs-lookup"><span data-stu-id="1d7d4-105">In local-only mode, the network packet provider (NPP) returns frames that are sent to or from the computer on which the monitor is running, including broadcasts and multicasts directed to the local machine.</span></span> <span data-ttu-id="1d7d4-106">Anche se limitato ai frame diretti localmente, la modalità locale è molto meno complessa.</span><span class="sxs-lookup"><span data-stu-id="1d7d4-106">Although limited to locally directed frames, local-mode is also much less processor intensive.</span></span>

<span data-ttu-id="1d7d4-107">In modalità promiscua, il monitoraggio può anche controllare il traffico non indirizzato al o dal computer locale.</span><span class="sxs-lookup"><span data-stu-id="1d7d4-107">In promiscuous mode, the monitor can also watch for traffic that is not directed to or from the local computer.</span></span> <span data-ttu-id="1d7d4-108">A meno che il monitoraggio non abbia specificato il flag, MCS \_ Create \_ pmode \_ non è \_ necessario nella funzione [OnLoadingDLL](onloadingdll.md) , il servizio di controllo di monitoraggio (MCSVC) presuppone che il monitoraggio richieda la modalità promiscua quando carica la dll di monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="1d7d4-108">Unless the monitor has specified the flag, MCS\_CREATE\_PMODE\_NOT\_REQUIRED, in the [OnLoadingDLL](onloadingdll.md) function, the Monitor Control Service (MCSVC) assumes that the monitor requires promiscuous mode when it loads the monitor DLL.</span></span>

 

 



