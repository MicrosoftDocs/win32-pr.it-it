---
description: La tabella CounterDetails descrive un contatore specifico in un determinato computer.
ms.assetid: e2a16a6e-8cd4-4fd3-adeb-461faed948e4
title: CounterDetails
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 751073cdc2f2646ad1f2351bff0bdc02c498d428
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967522"
---
# <a name="counterdetails"></a>CounterDetails

La tabella **CounterDetails** descrive un contatore specifico in un determinato computer.

La tabella **CounterDetails** definisce i campi seguenti:

-   **CounterID:** Identificatore univoco nel database di cui viene eseguito il mapping a una stringa di testo specifica del nome del contatore. Questo campo è la chiave primaria della tabella.
-   **Nomecomputer:** Nome del computer che ha registrato il set di dati.
-   **ObjectName:** Nome dell'oggetto prestazioni.
-   **CounterName:** Nome del contatore.
-   **CounterType:** Tipo di contatore. Per un elenco dei tipi di contatori e delle relative formule, vedere la sezione relativa ai tipi di contatore del [Kit di distribuzione di Windows Server 2003](/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10)).
-   **DefaultScale:** Ridimensionamento predefinito da applicare ai dati del contatore delle prestazioni non elaborati.
-   **Nomeistanza:** Nome dell'istanza del contatore.
-   **InstanceIndex:** Numero di indice dell'istanza del contatore.
-   **Padrename:** Alcuni contatori sono associati logicamente ad altri e vengono definiti elementi padre. Ad esempio, l'elemento padre di un thread è un processo e l'elemento padre di un driver del disco logico è un'unità fisica. Questo campo contiene il nome dell'elemento padre. Il valore in questo campo o nel campo **ID oggetto padre** identifica un'istanza padre specifica. Se il valore di questo campo è **null**, è necessario controllare il valore nel campo **ID oggetto padre** per identificare l'elemento padre. Se i valori in entrambi i campi sono **null**, il contatore non ha un elemento padre.
-   **ID oggetto padre:** Identificatore univoco dell'elemento padre. Il valore in questo campo o nel campo **ParentName** identifica un'istanza padre specifica. Se il valore di questo campo è **null**, è necessario controllare il valore nel campo **ParentName** per identificare l'elemento padre.

 

 
