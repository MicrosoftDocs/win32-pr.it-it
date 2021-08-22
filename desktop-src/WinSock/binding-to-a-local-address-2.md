---
description: Prima di poter usare un socket per configurare una connessione o ricevere una richiesta di connessione, è necessario che sia associato a un indirizzo locale.
ms.assetid: 8767a209-e293-47cd-b503-ff4cffbf6fb4
title: Binding a un indirizzo locale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dd4691e6581cbe1a3a2dee21d7dc4e0a0672812121028c515ad192b30279f61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132754"
---
# <a name="binding-to-a-local-address"></a>Binding a un indirizzo locale

Prima di poter usare un socket per configurare una connessione o ricevere una richiesta di connessione, è necessario che sia associato a un indirizzo locale. Questa operazione può essere eseguita in modo esplicito chiamando [**WSPBind**](/previous-versions/windows/hardware/network/ff566268(v=vs.85))o in modo implicito da [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) se il socket non è associato quando viene chiamata questa funzione.

 

 
