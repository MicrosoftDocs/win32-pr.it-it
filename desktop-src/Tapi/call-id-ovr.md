---
description: L'ID di chiamata differisce dall'identificatore di sessione in due modi principali a cui il provider di servizi lo assegna ed è lo stesso per tutte le applicazioni che gestiscono la sessione.
ms.assetid: c9d0d43b-3053-4e3e-b442-57942f3448df
title: ID chiamata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef571b55f653cb9c7bc1d61cdc8a3f71e91ba8f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312732"
---
# <a name="call-id"></a>ID chiamata

L'ID di chiamata differisce dall' [identificatore di sessione](session-identifier-ovr.md) in due modi principali: il provider di servizi lo assegna ed è lo stesso per tutte le applicazioni che gestiscono la sessione. Non può essere usato per la comunicazione ordinaria con TAPI per le operazioni di sessione perché non corrisponde a una particolare applicazione.

L'ID chiamata viene usato nelle operazioni, ad esempio determinare se un gruppo di ID di sessione fa effettivamente riferimento a una chiamata, come nel caso di una conferenza o per le comunicazioni con un'altra applicazione.

Non tutti i provider di servizi supportano l'utilizzo di queste informazioni.

**TAPI 2. x:** Vedere [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (membro **dwCallID** di [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)).

**TAPI 3. x:** Vedere [**ITCallInfo:: Get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**CIL \_ CALLID** member of [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).

 

 
