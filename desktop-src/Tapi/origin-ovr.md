---
description: Origin è una descrizione generale del punto in cui la sessione è stata avviata, ad esempio se è esterna o interna a una rete aziendale. \_Per un elenco delle origini supportate da TAPI, vedere costanti LINECALLORIGIN.
ms.assetid: d9779438-fd08-495a-ae3d-ffad9b543090
title: Origine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71105caff17850c76c1e2c388911086a4cf9ea8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131642"
---
# <a name="origin"></a>Origine

Origin è una descrizione generale del punto in cui la sessione è stata avviata, ad esempio se è esterna o interna a una rete aziendale. Per un elenco delle origini supportate da TAPI, vedere [ \_ costanti LINECALLORIGIN](./linecallorigin--constants.md) .

Non tutti i provider di servizi supportano l'utilizzo di queste informazioni.

**TAPI 2. x:** Vedere [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (membro **dwOrigin** di *lpCallInfo*).

**TAPI 3. x:** Vedere [**ITCallInfo:: Get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (membro di **\_ origine CIL** di [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).

 

 
