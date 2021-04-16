---
description: Il tipo di supporto (o modalità) descrive il tipo di informazioni scambiate, ad esempio la voce interattiva. Una determinata sessione di comunicazione può coinvolgere diversi tipi di supporti.
ms.assetid: 2eb140f0-ca07-4e60-b9f3-be2f466f4fca
title: Tipo di supporto per una sessione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc8f5c7743a5d5a85003c99b2ac1abbf13f54168
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104530511"
---
# <a name="media-type-for-a-session"></a>Tipo di supporto per una sessione

Il tipo di supporto (o modalità) descrive il tipo di informazioni scambiate, ad esempio la voce interattiva. Una determinata sessione di comunicazione può coinvolgere diversi tipi di supporti.

I provider di servizi espongono a TAPI e alle applicazioni il tipo o i tipi di supporto supportati. Per informazioni sull'acquisizione di questi dati, vedere la panoramica del [tipo di supporto](media-type-ovr.md) per dispositivi.

**TAPI 2. x:** Vedere [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), [**lineSetMediaMode**](/windows/win32/api/tapi/nf-tapi-linesetmediamode), [**lineMonitorMedia**](/windows/win32/api/tapi/nf-tapi-linemonitormedia), [**riga \_ MONITORMEDIA**](./line-monitormedia.md) Message, [LINEMEDIAMODE \_ costanti](./linemediamode--constants.md).

**TAPI 3. x:** Vedere [**ITCallInfo:: Get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) with **CIL \_ MEDIATYPESAVAILABLE**, [**ITCallInfo::p UT \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong) with **CIL \_ MEDIATYPESAVAILABLE**, [**ITCallInfoChangeEvent:: Get \_ cause**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfochangeevent-get_cause) (restituisce [**CALLINFOCHANGE \_ cause**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfochange_cause) of **CIC \_ MEDIATYPE**), [TAPIMEDIATYPE \_ costanti](tapimediatype--constants.md).

 

 
