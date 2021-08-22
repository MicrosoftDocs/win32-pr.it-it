---
description: Il trattamento si riferisce alla gestione di una sessione in ingresso a cui non è ancora stata data risposta o che è stata messa in attesa, ad esempio musica. Per un elenco dei tipi di trattamento definiti da TAPI, vedere Costanti \_ LINECALLTREATMENT.
ms.assetid: 0b8d1023-374a-4937-b39c-04043423eb47
title: Modalità di gestione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60f29f8848c76029daa7828f40061c828b625ec046dea7fac35159b390a4d106
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139744"
---
# <a name="treatment"></a>Modalità di gestione

Il trattamento si riferisce alla gestione di una sessione in ingresso a cui non è ancora stata data risposta o che è stata messa in attesa, ad esempio musica. Per un elenco dei tipi di trattamento definiti da TAPI, vedere Costanti [LINECALLTREATMENT. \_ ](./linecalltreatment--constants.md)

Non tutti i provider di servizi supportano l'uso di queste informazioni.

**TAPI 2.x: **[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (** dwCallTreatment** membro di *lpCallInfo*)

**TAPI 3.x: **[**ITCallInfo::get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (** membro CIL \_ CALLTREATMENT** di [**CALLINFO \_ LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long))

 

 
