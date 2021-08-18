---
description: La tabella CounterDetails descrive un contatore specifico in un computer specifico.
ms.assetid: e2a16a6e-8cd4-4fd3-adeb-461faed948e4
title: CounterDetails
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef429f7f90c38d53f085ed0243e1c799c1d1cfa808c7aa052d8a37ed3a1faf1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011359"
---
# <a name="counterdetails"></a>CounterDetails

La **tabella CounterDetails** descrive un contatore specifico in un computer specifico.

La **tabella CounterDetails** definisce i campi seguenti:

-   **CounterID:** Identificatore univoco nel database che esegue il mapping a una stringa di testo del nome del contatore specifica. Questo campo è la chiave primaria di questa tabella.
-   **MachineName:** Nome del computer che ha registrato il set di dati.
-   **ObjectName:** Nome dell'oggetto prestazioni.
-   **CounterName:** Nome del contatore.
-   **CounterType:** Tipo di contatore. Per un elenco dei tipi di contatori e delle relative formule, vedere la sezione Counter Types (Tipi di contatori) di [Windows Server 2003 Deployment Kit.](/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10))
-   **DefaultScale:** Ridimensionamento predefinito da applicare ai dati del contatore delle prestazioni non elaborati.
-   **InstanceName:** Nome dell'istanza del contatore.
-   **InstanceIndex:** Numero di indice dell'istanza del contatore.
-   **ParentName:** Alcuni contatori sono associati logicamente ad altri e sono definiti elementi padre. Ad esempio, l'elemento padre di un thread è un processo e l'elemento padre di un driver di disco logico è un'unità fisica. Questo campo contiene il nome dell'elemento padre. Il valore in questo campo o il **campo ParentObjectID** identifica un'istanza padre specifica. Se il valore in questo campo è **NULL,** è necessario controllare il valore nel campo **ParentObjectID** per identificare l'elemento padre. Se i valori in entrambi i campi **sono NULL,** il contatore non ha un elemento padre.
-   **ParentObjectID:** Identificatore univoco dell'elemento padre. Il valore in questo campo o nel campo **ParentName** identifica un'istanza padre specifica. Se il valore in questo campo è **NULL,** è necessario controllare il valore nel campo **ParentName** per identificare l'elemento padre.

 

 
