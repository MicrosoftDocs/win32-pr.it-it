---
description: Gli aggiornamenti che richiedono l'interazione dell'utente non possono essere installati dalle applicazioni dell'agente di aggiornamento di Windows (WUA) se le applicazioni WUA sono in esecuzione nel contesto del servizio di accesso secondario.
ms.assetid: 090cd730-cfcd-49fc-b748-f66e696edaf3
title: Uso di WUA da un processo di accesso secondario (RunAs)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66a659b9c46429100393138751039fdc1ce529191970a35c76d36e45bb16eb0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049089"
---
# <a name="using-wua-from-a-secondary-logon-run-as-process"></a>Uso di WUA da un processo di accesso secondario (RunAs)

Gli aggiornamenti che richiedono l'interazione dell'utente non possono essere installati dalle applicazioni dell'agente di aggiornamento di Windows (WUA) se le applicazioni WUA sono in esecuzione nel contesto del servizio di accesso secondario.

Se il processo che chiama WUA è in esecuzione nel contesto del servizio RunAs o del servizio di accesso secondario, un tentativo di installare un aggiornamento che richiede l'interazione dell'utente ha esito negativo e restituisce l'errore **WU E NO INTERACTIVE \_ \_ \_ \_ USER.**

In Microsoft Windows è possibile eseguire programmi come utente diverso dall'utente attualmente connesso. A tale scopo, è necessario che il servizio di accesso secondario sia in esecuzione.

 

 



