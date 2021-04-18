---
description: Il monitoraggio delle cifre monitora la chiamata per le cifre.
ms.assetid: 6ba28fdf-87d5-4d39-9e12-8201585a86ee
title: Monitoraggio delle cifre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2454f6886bba4e859348df929c1a35f10c3d481
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306331"
---
# <a name="digit-monitoring"></a><span data-ttu-id="e6feb-103">Monitoraggio delle cifre</span><span class="sxs-lookup"><span data-stu-id="e6feb-103">Digit Monitoring</span></span>

<span data-ttu-id="e6feb-104">Il monitoraggio delle cifre monitora la chiamata per le cifre.</span><span class="sxs-lookup"><span data-stu-id="e6feb-104">Digit monitoring monitors the call for digits.</span></span> <span data-ttu-id="e6feb-105">TAPI consente la segnalazione di cifre in base a due metodi (modalità digit):</span><span class="sxs-lookup"><span data-stu-id="e6feb-105">TAPI allows digits to be signaled according to two methods (digit modes):</span></span>

-   <span data-ttu-id="e6feb-106">Le cifre a impulsi vengono segnalate come sequenze impulsi o rotanti.</span><span class="sxs-lookup"><span data-stu-id="e6feb-106">Pulse Digits are signaled as pulse or rotary sequences.</span></span> <span data-ttu-id="e6feb-107">Per il rilevamento, questi impulsi si manifestano come nient'altro che sequenze di clic acustici.</span><span class="sxs-lookup"><span data-stu-id="e6feb-107">For detection, these pulses manifest themselves as nothing more than sequences of audible clicks.</span></span> <span data-ttu-id="e6feb-108">Le cifre di impulso valide sono comprese tra' 0' è 9'.</span><span class="sxs-lookup"><span data-stu-id="e6feb-108">Valid pulse digits are '0' through '9'.</span></span>
-   <span data-ttu-id="e6feb-109">Le cifre DTMF vengono segnalate come toni DTMF (Dual Tone Multiple Frequency).</span><span class="sxs-lookup"><span data-stu-id="e6feb-109">DTMF Digits are signaled as DTMF (Dual Tone Multiple Frequency) tones.</span></span> <span data-ttu-id="e6feb-110">Le cifre DTMF valide sono comprese tra' 0' è 9',' A '.</span><span class="sxs-lookup"><span data-stu-id="e6feb-110">Valid DTMF digits are '0' through '9', 'A'.</span></span> <span data-ttu-id="e6feb-111">' B ',' c',' d',' \* ' è \# '.</span><span class="sxs-lookup"><span data-stu-id="e6feb-111">'B', 'C', 'D', '\*', and '\#'.</span></span> <span data-ttu-id="e6feb-112">È possibile monitorare sia l'inizio che il bordo inferiore delle cifre DTMF.</span><span class="sxs-lookup"><span data-stu-id="e6feb-112">Both the beginning and the down edge of DTMF digits can be monitored.</span></span>

<span data-ttu-id="e6feb-113">Un'applicazione può abilitare o disabilitare il monitoraggio delle cifre per una chiamata specificata con [**lineMonitorDigits**](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits).</span><span class="sxs-lookup"><span data-stu-id="e6feb-113">An application can enable or disable digit monitoring on a specified call with [**lineMonitorDigits**](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits).</span></span> <span data-ttu-id="e6feb-114">Quando il monitoraggio dei numeri è abilitato, le cifre rilevate fanno sì che l'applicazione riceva una notifica con il messaggio di [**riga \_ MONITORDIGITS**](line-monitordigits.md) .</span><span class="sxs-lookup"><span data-stu-id="e6feb-114">When digit monitoring is enabled, detected digits cause the application to be notified with the [**LINE\_MONITORDIGITS**](line-monitordigits.md) message.</span></span> <span data-ttu-id="e6feb-115">Questo messaggio fornisce l'handle di chiamata su cui è stata rilevata la cifra, nonché il valore della cifra e la modalità di cifra.</span><span class="sxs-lookup"><span data-stu-id="e6feb-115">This message provides the call handle on which the digit was detected as well as the digit value and the digit mode.</span></span> <span data-ttu-id="e6feb-116">L'ambito del monitoraggio delle cifre è associato alla durata della chiamata.</span><span class="sxs-lookup"><span data-stu-id="e6feb-116">The scope of digit monitoring is bound by the lifetime of the call.</span></span> <span data-ttu-id="e6feb-117">Il monitoraggio delle cifre su una chiamata termina non appena la chiamata si *disconnette* o diventa *inattiva*.</span><span class="sxs-lookup"><span data-stu-id="e6feb-117">Digit monitoring on a call ends as soon as the call *disconnects* or goes *idle*.</span></span>

 

 



