---
title: Aggiornamento di una PDU
description: Un'applicazione WinSNMP può recuperare e aggiornare i campi PDU selezionati usando le funzioni SnmpGetPduData e SnmpSetPduData.
ms.assetid: 001f5252-aa54-490b-8ff0-39a7780baff8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 678f980882b350669321cf676f9bc69af4369de8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713336"
---
# <a name="updating-a-pdu"></a><span data-ttu-id="3b9a9-103">Aggiornamento di una PDU</span><span class="sxs-lookup"><span data-stu-id="3b9a9-103">Updating a PDU</span></span>

<span data-ttu-id="3b9a9-104">Un'applicazione WinSNMP può recuperare e aggiornare i campi PDU selezionati usando le funzioni [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) e [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) .</span><span class="sxs-lookup"><span data-stu-id="3b9a9-104">A WinSNMP application can retrieve and update selected PDU fields by using the [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) and the [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) functions.</span></span>

<span data-ttu-id="3b9a9-105">L'applicazione può recuperare i campi tipo PDU, identificatore richiesta, stato errore e indice errore da una PDU specifica.</span><span class="sxs-lookup"><span data-stu-id="3b9a9-105">The application can retrieve the PDU type, request identifier, error status, and error index fields from a specific PDU.</span></span> <span data-ttu-id="3b9a9-106">Può anche recuperare l'handle per l'elenco di associazioni variabili.</span><span class="sxs-lookup"><span data-stu-id="3b9a9-106">It can also retrieve the handle to the variable binding list.</span></span> <span data-ttu-id="3b9a9-107">L'applicazione può aggiornare i **campi \_ tipo PDU** e **\_ ID richiesta** .</span><span class="sxs-lookup"><span data-stu-id="3b9a9-107">The application can update the **PDU\_type** and **request\_id** fields.</span></span>

<span data-ttu-id="3b9a9-108">Se il tipo PDU è uguale a SNMP \_ PDU \_ GetBulk, l'applicazione può anche aggiornare i **non \_ ripetitori** e i campi **numero massimo \_** di ripetizioni della PDU.</span><span class="sxs-lookup"><span data-stu-id="3b9a9-108">If the PDU type is equal to SNMP\_PDU\_GETBULK, the application can also update the **non\_repeaters** and the **max\_repetitions** fields of the PDU.</span></span>

 

 




