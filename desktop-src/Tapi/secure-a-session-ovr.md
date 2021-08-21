---
description: Se un'applicazione non vuole interferenze da eventi esterni per una sessione da TAPI o dal provider di servizi, deve proteggere la chiamata.
ms.assetid: 0a3be209-e3ff-4177-abb2-ad0facbdf569
title: Proteggere una sessione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64ee16dc0854c6502f1347a3aa676e709920555ad91a02190db001bd80b34824
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080461"
---
# <a name="secure-a-session"></a>Proteggere una sessione

Se un'applicazione non vuole interferenze da eventi esterni per una sessione da TAPI o dal provider di servizi, deve proteggere la chiamata. In un ambiente analogo, ad esempio, i toni di chiamata in attesa possono eliminare una sessione di fax o modem nella chiamata originale.

Un'applicazione può proteggere una chiamata al momento della chiamata o dopo che la chiamata esiste già.

Non tutti i provider di servizi supportano l'uso di questa operazione.

**TAPI 2.x:** Vedere [**lineSecureCall**](/windows/win32/api/tapi/nf-tapi-linesecurecall).

**TAPI 3.x:** Vedere [**ITAddress::Forward**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward).

 

 
