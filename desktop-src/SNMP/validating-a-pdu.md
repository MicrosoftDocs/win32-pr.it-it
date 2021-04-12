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
# <a name="validating-a-pdu"></a><span data-ttu-id="e0068-103">Convalida di una PDU</span><span class="sxs-lookup"><span data-stu-id="e0068-103">Validating a PDU</span></span>

<span data-ttu-id="e0068-104">Quando l'applicazione WinSNMP chiama la funzione [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) o la funzione [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) , l'implementazione di Microsoft WinSNMP verifica la validità della PDU e degli altri parametri della funzione.</span><span class="sxs-lookup"><span data-stu-id="e0068-104">When the WinSNMP application calls the [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) function or the [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) function, the Microsoft WinSNMP implementation verifies the validity of the PDU and the other function parameters.</span></span>

<span data-ttu-id="e0068-105">Il valore di un componente dati PDU (o campo) può essere valido singolarmente, ma potrebbe non essere valido in combinazione con i valori per gli altri campi.</span><span class="sxs-lookup"><span data-stu-id="e0068-105">The value of one PDU data component (or field) can be valid individually, but it may be invalid in combination with values for other fields.</span></span> <span data-ttu-id="e0068-106">Ad esempio, a meno che il campo **\_ tipo PDU** della PDU non sia una \_ risposta SNMP PDU \_ GetBulk o SNMP \_ PDU \_ , i campi **\_ stato errore** e **\_ Indice errori** devono essere uguali a zero.</span><span class="sxs-lookup"><span data-stu-id="e0068-106">For example, unless the **PDU\_type** field of the PDU is SNMP\_PDU\_GETBULK or SNMP\_PDU\_RESPONSE, both the **error\_status** and **error\_index** fields must be equal to zero.</span></span> <span data-ttu-id="e0068-107">Qualsiasi altra combinazione di valori costituisce una PDU non valida.</span><span class="sxs-lookup"><span data-stu-id="e0068-107">Any other value combination constitutes an invalid PDU.</span></span>

<span data-ttu-id="e0068-108">L'implementazione rifiuta PDU non validi e restituisce lo stato di errore SNMPAPI errore \_ .</span><span class="sxs-lookup"><span data-stu-id="e0068-108">The implementation rejects invalid PDUs and returns the error status SNMPAPI\_FAILURE.</span></span> <span data-ttu-id="e0068-109">Imposta un codice di errore esteso uguale a SNMPAPI \_ PDU \_ non valido.</span><span class="sxs-lookup"><span data-stu-id="e0068-109">It sets an extended error code equal to SNMPAPI\_PDU\_INVALID.</span></span>

 

 




