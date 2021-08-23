---
description: La velocità o la larghezza di banda di una chiamata specifica la velocità di trasmissione dei dati. Tre punti dati identificano la frequenza corrente della velocità massima per una modalità di connessione specificata e la velocità minima per la modalità di connessione.
ms.assetid: bc373ac5-a986-483f-a136-60cdc2e2c6b0
title: Tariffa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce0af0b2dd6dfe34759753f52773bafe0bdf2bf8f4472ed863dcc6c8b0f10a0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060559"
---
# <a name="rate"></a>Tariffa

La velocità (o la larghezza di banda) di una chiamata specifica la velocità di trasmissione dei dati. Tre punti dati identificano la frequenza: la frequenza corrente, la velocità massima per una modalità di connessione specificata e la velocità minima per la modalità di connessione.

Non tutti i provider di servizi supportano l'uso di queste informazioni.

**TAPI 2.x: **[**lineSetCallParams,**](/windows/win32/api/tapi/nf-tapi-linesetcallparams) [**lineGetCallInfo,**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) **dwMinRate** o **dwMaxRate** membro di [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)

**TAPI 3.x: **[**ITCallInfo::get \_ CallInfoLong,**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) [**ITCallInfo::p ut \_ CallInfoLong,**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong) **CIL \_ MAXRATE,** **CIL \_ MINRATE** o **CIL \_ RATE** membro di [**CALLINFO \_ LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)

**TSPI: **[**MESSAGGIO LINE \_ CALLINFO,**](/previous-versions/windows/desktop/legacy/ms725218(v=vs.85)) con *dwParam1* impostato su LINECALLINFOSTATE \_ RATE

 

 
