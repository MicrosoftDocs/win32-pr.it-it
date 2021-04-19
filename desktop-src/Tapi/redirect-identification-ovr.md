---
description: Quando un'applicazione reindirizza una sessione, TAPI mantiene le informazioni di identificazione sul percorso che ha reindirizzato la sessione e il percorso a cui è stato reindirizzato.
ms.assetid: 08484b38-7c97-4acc-921e-0f566b2d3415
title: Identificazione Reindirizzamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8316b7d1566a24ead21f7b1fdf2d16b1c48a2b15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319879"
---
# <a name="redirect-identification"></a>Identificazione Reindirizzamento

Quando un'applicazione [reindirizza](redirect-ovr.md) una sessione, TAPI mantiene le informazioni di identificazione sul percorso che ha reindirizzato la sessione e il percorso a cui è stato reindirizzato.

"Reindirizzamento" si riferisce al percorso che ha richiamato l'operazione di reindirizzamento. "Reindirizzamento" identifica la nuova destinazione per la sessione.

Non tutti i provider di servizi supportano l'utilizzo di queste informazioni.

* * TAPI 2. x: * *[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwRedirectionIDSize**, **dwRedirectionIDOffset**, **dwRedirectionIDNameSize**, **dwRedirectionIDNameOffset**, **dwRedirectingIDSize**, **dwRedirectingIDOffset**, **dwRedirectingIDNameSize** e **dwRedirectingIDNameOffset** membri di [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)

* * TAPI 3. x: * *[**ITCallInfo:: Get \_ CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring)called with **the CIS \_ REDIRECTIONIDNAME**, **CIS \_ REDIRECTIONIDNUMBER**, **CIS \_ REDIRECTINGIDNAME** o **CIS \_ REDIRECTINGIDNUMBER** member of [**CALLINFO \_ String**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)

 

 
