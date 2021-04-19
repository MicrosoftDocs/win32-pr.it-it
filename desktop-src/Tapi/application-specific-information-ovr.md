---
description: Le informazioni specifiche dell'applicazione consentono alle applicazioni di passare le altre informazioni relative a una sessione tramite TAPI. Queste informazioni non vengono interpretate da TAPI e l'utilizzo è interamente definito dalle applicazioni.
ms.assetid: e72e4164-3578-4e18-aea0-09d47d385b57
title: Informazioni specifiche dell'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bf4a10413f914eb0bb2da763022f1946811ce12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319885"
---
# <a name="application-specific-information"></a>Informazioni specifiche dell'applicazione

Le informazioni specifiche dell'applicazione consentono alle applicazioni di passare le altre informazioni relative a una sessione tramite TAPI. Queste informazioni non vengono interpretate da TAPI e l'utilizzo è interamente definito dalle applicazioni.

Quando le informazioni specifiche dell'applicazione vengono modificate da un'applicazione, TAPI invia tutte le altre applicazioni con privilegi di monitoraggio o di proprietario nella sessione, un evento che indica che si è verificata una modifica.

Non tutti i provider di servizi supportano l'utilizzo di queste informazioni.

**TAPI 2. x:** Vedere [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (membro *dwAppSpecific* di *lpCallInfo*), [**lineSetAppSpecific**](/windows/win32/api/tapi/nf-tapi-linesetappspecific), [**riga \_ CALLINFO**](./line-callinfo.md) Message (*dwParam1* impostato su LINECALLINFOSTATE \_ APPSPECIFIC).

**TAPI 3. x:** Vedere [**ITCallInfo:: Get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), [**ITCallInfo::p UT \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong) (**CIL \_ APPSPECIFIC** membro of [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).

 

 
