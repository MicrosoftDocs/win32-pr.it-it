---
description: L'identificazione connessa identifica l'entità effettivamente connessa a. Questo può essere diverso dall'identificazione chiamata se la chiamata è stata deviata.
ms.assetid: 3f9ba728-8e78-4f1f-a0c1-76799fd62c9d
title: Identificazione connessa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59fdb2f11b27bf9281b381170aa0d5b5ab027088
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350566"
---
# <a name="connected-identification"></a>Identificazione connessa

L'identificazione connessa identifica l'entità effettivamente connessa a. Questo può essere diverso dall'identificazione chiamata se la chiamata è stata deviata.

Non tutti i provider di servizi supportano l'utilizzo di queste informazioni.

**TAPI 2. x:** Vedere [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwConnectedIDFlags**, **dwConnectedIDSize**, **DwConnectedIDOffset**, **dwConnectedIDNameSize** e **dwConnectedIDNameOffset** membri di *lpCallInfo*).

**TAPI 3. x:** Vedere [**ITCallInfo:: Get \_ CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring) (**CIL \_ CONNECTEDIDNAME** membro della [**\_ stringa CALLINFO**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)).

 

 
