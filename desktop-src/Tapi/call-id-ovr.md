---
description: L'ID chiamata è diverso dall'identificatore di sessione in due modi principali assegnati dal provider di servizi ed è lo stesso per ogni applicazione che gestisce la sessione.
ms.assetid: c9d0d43b-3053-4e3e-b442-57942f3448df
title: ID chiamata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb32a8cd00e3c8f77bcabb14de79170a259fba0e40ddb354afeab022528369c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118870150"
---
# <a name="call-id"></a>ID chiamata

L'ID chiamata differisce dall'identificatore di sessione [in](session-identifier-ovr.md) due modi principali: il provider di servizi lo assegna ed è lo stesso per ogni applicazione che gestisce la sessione. Non può essere usato per la comunicazione normale con TAPI relativamente alle operazioni di sessione perché non corrisponde a una particolare applicazione.

L'ID chiamata viene usato in operazioni come determinare se un gruppo di ID di sessione si riferisce effettivamente a una chiamata, come nel caso di una conferenza o per le comunicazioni con un'altra applicazione.

Non tutti i provider di servizi supportano l'uso di queste informazioni.

**TAPI 2.x:** Vedere [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwCallID** member of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)).

**TAPI 3.x:** Vedere [**ITCallInfo::get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**MEMBRO \_ CALLID CIL** di [**CALLINFO \_ LONG).**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)

 

 
