---
description: Il tipo di supporto (o modalità) descrive il tipo di informazioni scambiate, ad esempio la voce interattiva. Una determinata sessione di comunicazione può coinvolgere diversi tipi di supporti.
ms.assetid: 2eb140f0-ca07-4e60-b9f3-be2f466f4fca
title: Tipo di supporto per una sessione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 974935baf17652c0376386eea63028ba04eeb886d1f48eba1aaf7f8469a9c374
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002879"
---
# <a name="media-type-for-a-session"></a>Tipo di supporto per una sessione

Il tipo di supporto (o modalità) descrive il tipo di informazioni scambiate, ad esempio la voce interattiva. Una determinata sessione di comunicazione può coinvolgere diversi tipi di supporti.

I provider di servizi espongono a TAPI e alle applicazioni il tipo o i tipi di supporti supportati. Per informazioni [sull'acquisizione di questi dati,](media-type-ovr.md) vedere panoramica del tipo di supporto del dispositivo.

**TAPI 2.x:** Vedere [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), [**lineSetMediaMode**](/windows/win32/api/tapi/nf-tapi-linesetmediamode), [**lineMonitorMedia**](/windows/win32/api/tapi/nf-tapi-linemonitormedia), [**LINE \_ MONITORMEDIA**](./line-monitormedia.md) message, [LINEMEDIAMODE \_ Constants](./linemediamode--constants.md).

**TAPI 3.x:** Vedere [**ITCallInfo::get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) con **CIL \_ MEDIATYPESAVAILABLE**, [**ITCallInfo::p ut \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong) con **CIL \_ MEDIATYPESAVAILABLE**, [**ITCallInfoChangeEvent::get \_ Cause**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfochangeevent-get_cause) (restituisce [**CALLINFOCHANGE \_ CAUSE**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfochange_cause) di **CIC \_ MEDIATYPE),** [Costanti TAPIMEDIATYPE \_](tapimediatype--constants.md).

 

 
