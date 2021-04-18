---
description: La frequenza o la larghezza di banda di una chiamata specifica la velocità di trasmissione dei dati. I tre punti dati identificano la frequenza attuale della velocità massima per una modalità di porta specificata e la velocità minima per la modalità di porta.
ms.assetid: bc373ac5-a986-483f-a136-60cdc2e2c6b0
title: Tariffa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40747c26a98d8eb69e8161fb04302c5187121dff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316032"
---
# <a name="rate"></a><span data-ttu-id="1d311-104">Tariffa</span><span class="sxs-lookup"><span data-stu-id="1d311-104">Rate</span></span>

<span data-ttu-id="1d311-105">La velocità (o larghezza di banda) di una chiamata specifica la velocità di trasmissione dei dati.</span><span class="sxs-lookup"><span data-stu-id="1d311-105">The rate (or bandwidth) of a call specifies the speed of data transmission.</span></span> <span data-ttu-id="1d311-106">Frequenza di identificazione dei tre punti dati: la frequenza corrente, la velocità massima per una modalità di porta specificata e la velocità minima per la modalità di porta.</span><span class="sxs-lookup"><span data-stu-id="1d311-106">Three data points identify rate: the current rate, the maximum rate for a specified bearer mode, and the minimum rate for the bearer mode.</span></span>

<span data-ttu-id="1d311-107">Non tutti i provider di servizi supportano l'utilizzo di queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="1d311-107">Not all service providers support use of this information.</span></span>

<span data-ttu-id="1d311-108">\* \* TAPI 2. x: \* \*[**lineSetCallParams**](/windows/win32/api/tapi/nf-tapi-linesetcallparams), [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **DwMinRate** o **dwMaxRate** membro di [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)</span><span class="sxs-lookup"><span data-stu-id="1d311-108">\*\*TAPI 2.x:  \*\*[**lineSetCallParams**](/windows/win32/api/tapi/nf-tapi-linesetcallparams), [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwMinRate** or **dwMaxRate** member of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)</span></span>

<span data-ttu-id="1d311-109">\* \* TAPI 3. x: \* \*[**ITCallInfo:: Get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), [**ITCallInfo::p UT \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong), **CIL \_ MAXRATE**, **CIL \_ MINRATE** o **CIL \_ rate** member of [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)</span><span class="sxs-lookup"><span data-stu-id="1d311-109">\*\*TAPI 3.x:  \*\*[**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), [**ITCallInfo::put\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong), **CIL\_MAXRATE**, **CIL\_MINRATE**, or **CIL\_RATE** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)</span></span>

<span data-ttu-id="1d311-110">\* \* TSPI: \* \*[**riga \_ CALLINFO**](/previous-versions/windows/desktop/legacy/ms725218(v=vs.85)) messaggio con *dwParam1* impostato su LINECALLINFOSTATE \_ frequenza</span><span class="sxs-lookup"><span data-stu-id="1d311-110">\*\*TSPI:  \*\*[**LINE\_CALLINFO**](/previous-versions/windows/desktop/legacy/ms725218(v=vs.85)) message, with *dwParam1* set to LINECALLINFOSTATE\_RATE</span></span>

 

 
