---
description: Se un'applicazione non desidera alcuna interferenza da parte degli eventi esterni per una sessione da TAPI o dal provider di servizi, deve proteggere la chiamata.
ms.assetid: 0a3be209-e3ff-4177-abb2-ad0facbdf569
title: Proteggere una sessione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00b1567303efb61f28f9c6b3e92c24287d23d4af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319861"
---
# <a name="secure-a-session"></a>Proteggere una sessione

Se un'applicazione non desidera alcuna interferenza da parte degli eventi esterni per una sessione da TAPI o dal provider di servizi, deve proteggere la chiamata. Ad esempio, in un ambiente analogo i toni di attesa delle chiamate possono eliminare una sessione fax o modem sulla chiamata originale.

Un'applicazione può proteggere una chiamata nel momento in cui viene effettuata la chiamata o dopo che la chiamata esiste già.

Non tutti i provider di servizi supportano l'utilizzo di questa operazione.

**TAPI 2. x:** Vedere [**lineSecureCall**](/windows/win32/api/tapi/nf-tapi-linesecurecall).

**TAPI 3. x:** Vedere [**ITAddress:: inoltr**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward).

 

 
