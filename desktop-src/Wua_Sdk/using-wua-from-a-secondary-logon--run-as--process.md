---
description: Gli aggiornamenti che richiedono l'interazione dell'utente non possono essere installati dalle applicazioni di Windows Update Agent (WUA) se le applicazioni WUA sono in esecuzione nel contesto del servizio di accesso secondario.
ms.assetid: 090cd730-cfcd-49fc-b748-f66e696edaf3
title: Uso di WUA da un processo di accesso secondario (RunAs)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f08626532b588f044ca866f78ebab836671f12d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307583"
---
# <a name="using-wua-from-a-secondary-logon-run-as-process"></a>Uso di WUA da un processo di accesso secondario (RunAs)

Gli aggiornamenti che richiedono l'interazione dell'utente non possono essere installati dalle applicazioni di Windows Update Agent (WUA) se le applicazioni WUA sono in esecuzione nel contesto del servizio di accesso secondario.

Se il processo che chiama WUA viene eseguito nel contesto del servizio RunAs o del servizio di accesso secondario, un tentativo di installare un aggiornamento che richiede l'interazione dell'utente ha esito negativo e restituisce l'errore di **Wu \_ e \_ nessun \_ \_ utente interattivo** .

In Microsoft Windows è possibile eseguire programmi come un utente diverso dall'utente attualmente connesso. A tale scopo, è necessario che il servizio di accesso secondario sia in esecuzione.

 

 



