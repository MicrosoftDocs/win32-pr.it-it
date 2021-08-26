---
description: I flag di parametro forniscono informazioni su diversi flag di stato relativi a una sessione di comunicazione, ad esempio se l'identificazione del chiamante deve essere bloccata. Per un elenco dei flag definiti da TAPI, vedere Costanti LINECALLPARAMFLAGS. \_
ms.assetid: 30511328-a310-42b7-a81e-3ef2abf586ed
title: Flag di parametro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf663ea4ff6121f3e130f9c2a2e4c3c1f86f8611be8cc3fef3762adc535e84bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959861"
---
# <a name="parameter-flags"></a>Flag di parametro

I flag di parametro forniscono informazioni su diversi flag di stato relativi a una sessione di comunicazione, ad esempio se l'identificazione del chiamante deve essere bloccata. Per un elenco di flag definiti da TAPI, vedere Costanti [LINECALLPARAMFLAGS. \_ ](./linecallparamflags--constants.md)

Non tutti i provider di servizi supportano l'uso di queste informazioni.

**TAPI 2.x:** Vedere [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwCallParamFlags** membro di *lpCallInfo*).

**TAPI 3.x:** Vedere [**ITCallInfo::get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**membro CIL \_ CALLPARAMSFLAGS** di [**CALLINFO \_ LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).

 

 
