---
title: Convalida di una PDU
description: Quando l'applicazione WinSNMP chiama la funzione SnmpSendMsg o la funzione SnmpEncodeMsg, l'implementazione di Microsoft WinSNMP verifica la validità della PDU e degli altri parametri della funzione.
ms.assetid: 0f5754ff-3688-465b-a1ad-bf7d89d7dbd8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9d3fe0f9831f285b51b3060517d2037a8ec05f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396539"
---
# <a name="validating-a-pdu"></a>Convalida di una PDU

Quando l'applicazione WinSNMP chiama la funzione [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) o la funzione [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) , l'implementazione di Microsoft WinSNMP verifica la validità della PDU e degli altri parametri della funzione.

Il valore di un componente dati PDU (o campo) può essere valido singolarmente, ma potrebbe non essere valido in combinazione con i valori per gli altri campi. Ad esempio, a meno che il campo **\_ tipo PDU** della PDU non sia una \_ risposta SNMP PDU \_ GetBulk o SNMP \_ PDU \_ , i campi **\_ stato errore** e **\_ Indice errori** devono essere uguali a zero. Qualsiasi altra combinazione di valori costituisce una PDU non valida.

L'implementazione rifiuta PDU non validi e restituisce lo stato di errore SNMPAPI errore \_ . Imposta un codice di errore esteso uguale a SNMPAPI \_ PDU \_ non valido.

 

 




