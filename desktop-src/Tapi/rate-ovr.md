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
# <a name="rate"></a>Tariffa

La velocità (o larghezza di banda) di una chiamata specifica la velocità di trasmissione dei dati. Frequenza di identificazione dei tre punti dati: la frequenza corrente, la velocità massima per una modalità di porta specificata e la velocità minima per la modalità di porta.

Non tutti i provider di servizi supportano l'utilizzo di queste informazioni.

* * TAPI 2. x: * *[**lineSetCallParams**](/windows/win32/api/tapi/nf-tapi-linesetcallparams), [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **DwMinRate** o **dwMaxRate** membro di [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)

* * TAPI 3. x: * *[**ITCallInfo:: Get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), [**ITCallInfo::p UT \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong), **CIL \_ MAXRATE**, **CIL \_ MINRATE** o **CIL \_ rate** member of [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)

* * TSPI: * *[**riga \_ CALLINFO**](/previous-versions/windows/desktop/legacy/ms725218(v=vs.85)) messaggio con *dwParam1* impostato su LINECALLINFOSTATE \_ frequenza

 

 
