---
description: L'identificazione del chiamante fornisce informazioni sulla parte chiamante quando riceve una sessione in ingresso. In genere, un'applicazione utilizza questi dati come parte di un messaggio di stato per un utente.
ms.assetid: aaaa5eae-e917-44a7-b9c5-97ca2d9a4eec
title: Identificazione del chiamante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93513e3d94fac9c550b23651b3987bc794905beb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883237"
---
# <a name="caller-identification"></a>Identificazione del chiamante

L'identificazione del chiamante fornisce informazioni sulla parte chiamante quando riceve una sessione in ingresso. In genere, un'applicazione utilizza questi dati come parte di un messaggio di stato per un utente.

Queste informazioni non sono sempre disponibili immediatamente. Un'applicazione che vuole usare queste informazioni e ha verificato che il provider di servizi la supporti, deve verificare più volte prima di presumere che le informazioni non siano disponibili.

Non tutti i provider di servizi supportano l'utilizzo di queste informazioni.

**TAPI 2. x:** Vedere [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwCallerIDFlags**, **dwCallerIDSize**, **dwCallerIDOffset**, **dwCallerIDNameSize**, **dwCallerIDNameOffset** e **dwCallerIDAddressType** membri di *lpCallInfo*).

**TAPI 3. x:** Vedere [**ITCallInfo:: Get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**CIL \_ CALLERIDADDRESSTYPE** membro of [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)), [**ITCallInfo:: Get \_ CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring) (**CIS \_ CALLERIDNAME** e **CIS \_ CALLERIDNAME** members of [**CALLINFO \_ String**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)).

 

 
