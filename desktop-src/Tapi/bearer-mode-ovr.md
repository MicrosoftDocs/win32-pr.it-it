---
description: La modalità di chiamata corrisponde alla qualità della trasmissione richiesta dalla rete per stabilire una chiamata.
ms.assetid: 5276e1e7-7a91-4b74-b8c2-c0c7cebb203f
title: Modalità di porta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1780bee44254e6da754584f838785452ee728f18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226851"
---
# <a name="bearer-mode"></a>Modalità di porta

La [**modalità**](./linebearermode--constants.md) di chiamata corrisponde alla qualità della trasmissione richiesta dalla rete per stabilire una chiamata. È importante mantenere il concetto di modalità di portabilità separata da quello del [**tipo di supporto**](tapimediatype--constants.md). Ad esempio, la rete telefonica analoga (PSTN) fornisce solo una modalità di connessione di tipo Voice a 3,1 kHz, ma chiama che lo usa può supportare i tipi di supporto, ad esempio Voice, fax o data modem.

La modalità di chiamata di una chiamata viene specificata al momento dell'impostazione della chiamata o viene fornita quando viene offerta la chiamata. Con i dispositivi linea in grado di rappresentare i pool di canali, un provider di servizi può consentire la creazione di chiamate con una larghezza di banda più ampia.

Non tutti i provider di servizi supportano l'utilizzo di queste informazioni.

**TAPI 2. x:** Vedere [**lineSetCallParams**](/windows/win32/api/tapi/nf-tapi-linesetcallparams), [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwBearerMode** member of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo).

**TAPI 3. x:** Vedere [**ITCallInfo:: Get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), [**ITCallInfo::p UT \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong), **CIL \_ BEARERMODE** membro of [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long).

**TSPI:** Vedere il messaggio di [**riga \_ CALLINFO**](/previous-versions/windows/desktop/legacy/ms725218(v=vs.85)) con *dwParam1* impostato su LINECALLINFOSTATE \_ BEARERMODE.

 

 
