---
description: Quando un'applicazione reindirizza una sessione, TAPI mantiene le informazioni di identificazione sulla posizione che ha reindirizzato la sessione e la posizione a cui è stata reindirizzata.
ms.assetid: 08484b38-7c97-4acc-921e-0f566b2d3415
title: Identificazione del reindirizzamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa7648167e6f60dc2e8593a576053df9a0ff54eb0fadc9a446a66127b435e5c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060449"
---
# <a name="redirect-identification"></a>Identificazione del reindirizzamento

Quando [un'applicazione reindirizza](redirect-ovr.md) una sessione, TAPI mantiene le informazioni di identificazione sulla posizione che ha reindirizzato la sessione e la posizione a cui è stata reindirizzata.

"Reindirizzamento" si riferisce alla posizione che ha richiamato l'operazione di reindirizzamento. "Reindirizzamento" identifica la nuova destinazione per la sessione.

Non tutti i provider di servizi supportano l'uso di queste informazioni.

**TAPI 2.x: **[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwRedirectionIDSize**, **dwRedirectionIDOffset**, **dwRedirectionIDNameSize**, **dwRedirectionIDNameOffset**, **dwRedirectingIDSize**, **dwRedirectingIDOffset**, **dwRedirectingIDNameSize** e **dwRedirectingIDNameOffset** membri di [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)

**TAPI 3.x: **[**ITCallInfo::get \_ CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring)chiamato con il membro **CIS \_ REDIRECTIONIDNAME,** **CIS \_ REDIRECTIONIDNUMBER,** **CIS \_ REDIRECTINGIDNAME** o **CIS \_ REDIRECTINGIDNUMBER** di [**CALLINFO \_ STRING**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)

 

 
