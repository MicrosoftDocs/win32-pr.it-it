---
description: I flag di parametro forniscono informazioni su diversi flag di stato relativi a una sessione di comunicazione, ad esempio se l'identificazione del chiamante deve essere bloccata. \_Per un elenco di flag definiti da TAPI, vedere costanti LINECALLPARAMFLAGS.
ms.assetid: 30511328-a310-42b7-a81e-3ef2abf586ed
title: Flag di parametro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3adcb8b430045dc41afea4e7f55e5fa4458530b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311886"
---
# <a name="parameter-flags"></a>Flag di parametro

I flag di parametro forniscono informazioni su diversi flag di stato relativi a una sessione di comunicazione, ad esempio se l'identificazione del chiamante deve essere bloccata. Per un elenco di flag definiti da TAPI, vedere [ \_ costanti LINECALLPARAMFLAGS](./linecallparamflags--constants.md) .

Non tutti i provider di servizi supportano l'utilizzo di queste informazioni.

**TAPI 2. x:** Vedere [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (membro **dwCallParamFlags** di *lpCallInfo*).

**TAPI 3. x:** Vedere [**ITCallInfo:: Get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**CIL \_ CALLPARAMSFLAGS** member of [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).

 

 
