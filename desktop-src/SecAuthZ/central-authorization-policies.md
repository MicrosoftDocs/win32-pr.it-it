---
description: Un criterio di autorizzazione centrale (CAP) raccoglie le regole di autorizzazione specifiche (CAP) in un singolo criterio.
ms.assetid: E3E43D9F-6826-468A-86E9-AC8F9A381FD4
title: Criteri di autorizzazione centrali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0617f6bddb606d3c3fb3e5ccb6692c79c62a60f90de591b6ec3e04988db46f63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783225"
---
# <a name="central-authorization-policies"></a>Criteri di autorizzazione centrali

Un criterio di autorizzazione centrale (CAP) raccoglie le regole di autorizzazione specifiche (CAP) in un singolo criterio. Per consentire la combinazione delle regole di autorizzazione specifiche (CAPR) nei criteri di autorizzazione olistici dell'organizzazione, è possibile fare riferimento ai capr e applicarlo a un set di risorse. Questa operazione viene eseguita raccogliendo più (per riferimento) in un cap. Una volta definito, un CAP può essere distribuito dai responsabili delle risorse per applicare i criteri di autorizzazione delle organizzazioni alle risorse.

Un cap ha gli attributi seguenti:

-   Raccolta di CAPR: elenco di riferimenti a oggetti CAPR esistenti
-   Identificatore (Sid)
-   Descrizione
-   Nome

Un CAP viene valutato durante la valutazione dell'accesso per i file e le cartelle in cui è abilitata da un amministratore. Durante una [**chiamata AccessCheck,**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) il controllo CAP viene combinato logicamente con il controllo ACL discrezionale. Ciò significa che per ottenere l'accesso a un file a cui si applica il cap, un utente deve avere accesso sia in base al CAP (capr associati) che all'ACL discrezionale sul file.

Cap di esempio:

``` syntax
CORPORATE-FINANCE-CAP]
CAPID=S-1-5-3-4-56-45-67-123
Policies=HBI-CAPE;RETENTION-CAPR
```

## <a name="cap-definition"></a>Definizione CAP

Un cap viene creato e modificato in Active Directory usando una nuova esperienza utente in ADAC (o PowerShell) che consente all'amministratore di creare un CAP e specificare un set di capr che costituiscono il CAP.

 

 
