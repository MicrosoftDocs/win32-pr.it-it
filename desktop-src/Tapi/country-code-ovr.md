---
description: Il codice paese o regione è pertinente solo quando il tipo di indirizzo è LINEADDRESSTYPE \_ PhoneNumber. Identifica un'area del mondo.
ms.assetid: d838c2ac-4ee3-4314-8573-deed6c7430e3
title: Codice paese o area geografica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5557e4d67b701fda2aa05ad81686ae474b172063
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879746"
---
# <a name="country-or-region-code"></a>Codice paese o area geografica

Il codice paese o regione è pertinente solo quando il tipo di indirizzo è LINEADDRESSTYPE \_ PhoneNumber. Identifica un'area del mondo.

Tutti i provider di servizi che supportano l'utilizzo di numeri di telefono devono supportare l'utilizzo di queste informazioni.

**TAPI 2. x:** Vedere [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (membro **dwCountryCode** di *lpCallInfo*).

**TAPI 3. x:** Vedere [**ITCallInfo:: Get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**CIL \_ COUNTRYCODE** member of [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).

 

 
