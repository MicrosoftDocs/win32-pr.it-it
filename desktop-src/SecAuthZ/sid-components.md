---
description: Componenti SID
ms.assetid: 528412e7-c2b6-4ddd-86de-999252972421
title: Componenti SID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbd44d0534cc56c6ef998c150810f14b3eda289d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049587"
---
# <a name="sid-components"></a>Componenti SID

Un valore SID include componenti che forniscono informazioni sulla struttura e sui componenti di [**SID**](/windows/desktop/api/Winnt/ns-winnt-sid) che identificano in modo univoco un trustee. Un SID è costituito dai componenti seguenti:

-   Livello di revisione della struttura del [**SID**](/windows/desktop/api/Winnt/ns-winnt-sid)
-   Valore dell'autorità di identificazione a 48 bit che identifica l'autorità che ha emesso il SID
-   Numero variabile di valori di sottoautorizzazione o di [*ID relativo*](/windows/desktop/SecGloss/r-gly) (RID) che identificano in modo univoco il trustee relativo all'autorità che ha emesso il SID

La combinazione del valore dell'autorità di identificazione e dei valori di sottoautore garantisce che due SID non saranno uguali, anche se due diverse autorità emittenti di SID emettono la stessa combinazione di valori RID. Ogni autorità emittente SID rilascia un determinato RID una sola volta.

I SID vengono archiviati in formato binario in una struttura [**SID**](/windows/desktop/api/Winnt/ns-winnt-sid) . Per visualizzare un SID, è possibile chiamare la funzione [**ConvertSidToStringSid**](/windows/desktop/api/Sddl/nf-sddl-convertsidtostringsida) per convertire un SID binario in formato stringa. Per eseguire la conversione di una stringa SID in un SID funzionale valido, chiamare la funzione [**ConvertStringSidToSid**](/windows/desktop/api/Sddl/nf-sddl-convertstringsidtosida) .

Queste funzioni usano la notazione di stringa standardizzata seguente per SID, che semplifica la visualizzazione dei componenti:

s-*R* - *i* - ...

In questa notazione, il carattere letterale "S" identifica la serie di cifre come SID, *R* è il livello di revisione *, è* il valore dell'autorità di identificazione e *S*... è uno o più valori di sottoautorizzazione.

Nell'esempio seguente viene utilizzata questa notazione per visualizzare il noto SID relativo al dominio del gruppo Administrators locale:

S-1-5-32-544

In questo esempio, il SID include i componenti seguenti. Le costanti racchiuse tra parentesi sono l'autorità di identificazione nota e i valori [*RID*](/windows/desktop/SecGloss/r-gly) definiti in Winnt. h:

-   Livello di revisione 1
-   Valore dell'autorità di identificazione 5 ( \_ autorità NT di sicurezza \_ )
-   Primo valore di subauthority di 32 (SECURITY \_ Builtin \_ Domain \_ RID)
-   Un secondo valore di subauthority di 544 (DOMAIN \_ alias \_ RID \_ Admins)

 

 
