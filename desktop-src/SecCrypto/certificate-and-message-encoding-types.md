---
description: Molte delle funzioni richiedono tipi di codifica dei certificati o dei messaggi.
ms.assetid: 97b25435-aec2-4fdb-a4c6-89ec2e26f51d
title: Tipi di codifica dei certificati e dei messaggi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 185be8d3cc781786c93ac809c042c86d3601a45d86eaa39452f0bcbf44203a1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771977"
---
# <a name="certificate-and-message-encoding-types"></a>Tipi di codifica dei certificati e dei messaggi

Molte delle funzioni richiedono tipi di codifica dei certificati [*o dei messaggi*](../secgloss/m-gly.md). Questo tipo di codifica è **un valore DWORD,** possibilmente contenente sia il certificato che i tipi di codifica dei messaggi. Il tipo di codifica del certificato viene archiviato nella parola di ordine basso. Il tipo di codifica dei messaggi viene archiviato nella parola di ordine alto. Alcune funzioni o campi di struttura richiedono solo uno dei tipi di codifica, ma è sempre accettabile specificare entrambi i tipi di codifica. Per un esempio che specifica entrambi i tipi di codifica, vedere [ \# include e \# definisce](-includes-and--defines.md).

La convenzione di denominazione dei parametri seguente viene usata per indicare i tipi di codifica necessari.



| Nome                       | Commenti                                                                                                                                                                                                                                                                                                                |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *dwMsgAndCertEncodingType* | Entrambi i tipi di codifica sono obbligatori.                                                                                                                                                                                                                                                                                       |
| *dwMsgEncodingType*        | È necessario solo il tipo di codifica dei messaggi.                                                                                                                                                                                                                                                                             |
| *dwCertEncodingType*       | È necessario solo il tipo di codifica del certificato.                                                                                                                                                                                                                                                                         |
| *dwEncodingType*           | È necessario un messaggio o un tipo di codifica del certificato. Se la parola di ordine basso contenente il tipo di codifica del certificato è diversa da zero, viene usata. In caso contrario, viene usata la parola di ordine alto contenente il tipo di codifica dei messaggi. Se vengono specificati entrambi, viene usato il tipo di codifica del certificato nella parola di ordine basso. |



 

I tipi di codifica attualmente definiti sono illustrati nella tabella seguente.



| Tipo di codifica          | Valore      |
|------------------------|------------|
| CODIFICA \_ ASN CRYPT \_   | 0x00000001 |
| CODIFICA ASN X509 \_ \_    | 0x00000001 |
| CODIFICA ASN PKCS \_ 7 \_ \_ | 0x00010000 |



 

 

 
