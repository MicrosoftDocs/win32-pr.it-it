---
description: Molte delle funzioni richiedono tipi di codifica dei messaggi o certificati.
ms.assetid: 97b25435-aec2-4fdb-a4c6-89ec2e26f51d
title: Tipi di codifica di messaggi e certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3193b321d27892f8df9535ef81b8a988bf558e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484693"
---
# <a name="certificate-and-message-encoding-types"></a>Tipi di codifica di messaggi e certificati

Molte delle funzioni richiedono [*tipi di codifica dei messaggi*](../secgloss/m-gly.md)o certificati. Questo tipo di codifica è un **valore DWORD**, che può contenere sia il certificato che i tipi di codifica dei messaggi. Il tipo di codifica del certificato viene archiviato nella parola di ordine inferiore. Il tipo di codifica dei messaggi viene archiviato nella parola più avanzata. Alcune funzioni o campi della struttura richiedono solo uno dei tipi di codifica, ma è sempre accettabile specificare entrambi i tipi di codifica. Per un esempio di specifica di entrambi i tipi di codifica, vedere [ \# include e \# definisce](-includes-and--defines.md).

La convenzione di denominazione dei parametri riportata di seguito viene usata per indicare i tipi di codifica richiesti.



| Nome                       | Commenti                                                                                                                                                                                                                                                                                                                |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *dwMsgAndCertEncodingType* | Sono necessari entrambi i tipi di codifica.                                                                                                                                                                                                                                                                                       |
| *dwMsgEncodingType*        | È necessario solo il tipo di codifica dei messaggi.                                                                                                                                                                                                                                                                             |
| *dwCertEncodingType*       | È necessario solo il tipo di codifica del certificato.                                                                                                                                                                                                                                                                         |
| *dwEncodingType*           | È necessario specificare un tipo di codifica del messaggio o del certificato. Se la parola più bassa che contiene il tipo di codifica del certificato è diversa da zero, viene utilizzata. In caso contrario, viene utilizzata la parola più ordinata contenente il tipo di codifica dei messaggi. Se vengono specificati entrambi, viene utilizzato il tipo di codifica del certificato nella parola di ordine inferiore. |



 

I tipi di codifica attualmente definiti sono riportati nella tabella seguente.



| Tipo di codifica          | Valore      |
|------------------------|------------|
| \_codifica ASN di Crypt \_   | 0x00000001 |
| \_Codifica ASN \_ X509    | 0x00000001 |
| \_ \_ Codifica ASN 7 \_ ASN | 0x00010000 |



 

 

 
