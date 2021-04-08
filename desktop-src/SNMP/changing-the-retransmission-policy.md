---
title: Modifica dei criteri di ritrasmissione
description: L'implementazione di Microsoft WinSNMP fornisce supporto per i criteri di ritrasmissione archiviando un valore di timeout e un numero di tentativi per l'applicazione WinSNMP in un database.
ms.assetid: 9ab45adc-12b7-40b1-8fec-40bf04302f64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9f21fc479517b8844e9c1db75834b5b1c02edc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856189"
---
# <a name="changing-the-retransmission-policy"></a><span data-ttu-id="488e6-103">Modifica dei criteri di ritrasmissione</span><span class="sxs-lookup"><span data-stu-id="488e6-103">Changing the Retransmission Policy</span></span>

<span data-ttu-id="488e6-104">L'implementazione di Microsoft WinSNMP fornisce supporto per i criteri di ritrasmissione archiviando un valore di timeout e un numero di tentativi per l'applicazione WinSNMP in un database.</span><span class="sxs-lookup"><span data-stu-id="488e6-104">The Microsoft WinSNMP implementation provides retransmission policy support by storing a time-out value and a retry count for the WinSNMP application in a database.</span></span> <span data-ttu-id="488e6-105">L'implementazione archivia i valori per le singole entità di destinazione.</span><span class="sxs-lookup"><span data-stu-id="488e6-105">The implementation stores values for individual destination entities.</span></span> <span data-ttu-id="488e6-106">L'implementazione fornisce inizialmente i valori predefiniti per questi elementi, ma un'applicazione può aggiungere o modificare i valori per le singole entità.</span><span class="sxs-lookup"><span data-stu-id="488e6-106">The implementation initially supplies default values for these elements, but an application can add or modify values for individual entities.</span></span>

<span data-ttu-id="488e6-107">Una chiamata alle funzioni [**SnmpGetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettimeout) e [**SnmpGetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretry) restituisce i valori di timeout e di ripetizione dei tentativi per un'entità di destinazione specifica.</span><span class="sxs-lookup"><span data-stu-id="488e6-107">A call to the [**SnmpGetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettimeout) and [**SnmpGetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretry) functions returns the time-out and retry count values for a specific destination entity.</span></span> <span data-ttu-id="488e6-108">Per modificare il valore di timeout, un'applicazione WinSNMP deve chiamare la funzione [**SnmpSetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettimeout) .</span><span class="sxs-lookup"><span data-stu-id="488e6-108">To change the time-out value, a WinSNMP application must call the [**SnmpSetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettimeout) function.</span></span> <span data-ttu-id="488e6-109">Per modificare il valore del numero di tentativi, l'applicazione deve chiamare la funzione [**SnmpSetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretry) .</span><span class="sxs-lookup"><span data-stu-id="488e6-109">To change the retry count value the application must call the [**SnmpSetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretry) function.</span></span> <span data-ttu-id="488e6-110">Le impostazioni aggiornate influiscono sulle nuove richieste di messaggi SNMP all'entità di destinazione.</span><span class="sxs-lookup"><span data-stu-id="488e6-110">The updated settings affect new SNMP message requests to the destination entity.</span></span>

 

 




