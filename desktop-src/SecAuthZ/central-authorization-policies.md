---
description: Un criterio di autorizzazione centrale (CAP) raccoglie le specifiche regole di autorizzazione (CAPRs) in un singolo criterio.
ms.assetid: E3E43D9F-6826-468A-86E9-AC8F9A381FD4
title: Criteri di autorizzazione centrale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b890236b0dae0f8f8d51254def4e1607cc35894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308878"
---
# <a name="central-authorization-policies"></a>Criteri di autorizzazione centrale

Un criterio di autorizzazione centrale (CAP) raccoglie le specifiche regole di autorizzazione (CAPRs) in un singolo criterio. Per consentire la combinazione di regole di autorizzazione specifiche (CAPRs) nel criterio di autorizzazione olistica dell'organizzazione, è possibile fare riferimento a CAPRs insieme a un set di risorse. Questa operazione viene eseguita raccogliendo più (per riferimento) in un limite. Una volta definito un limite, è possibile distribuirlo utilizzato dai responsabili delle risorse per applicare i criteri di autorizzazione delle organizzazioni alle risorse.

Un limite ha gli attributi seguenti:

-   Raccolta di CAPRs: un elenco di riferimenti agli oggetti CAPR esistenti
-   Identificatore (SID)
-   Descrizione
-   Nome

Un limite viene valutato durante la valutazione dell'accesso per i file e le cartelle in cui è abilitato da un amministratore. Durante una chiamata [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) , il controllo della copertura viene combinato logicamente con il controllo ACL discrezionale; Ciò significa che per ottenere l'accesso a un file a cui si applica il limite, un utente deve avere accesso sia in base all'estremità (il CAPRs associato) che all'ACL discrezionale del file.

LIMITE di esempio:

``` syntax
CORPORATE-FINANCE-CAP]
CAPID=S-1-5-3-4-56-45-67-123
Policies=HBI-CAPE;RETENTION-CAPR
```

## <a name="cap-definition"></a>Definizione CAP

Un limite viene creato e modificato in Active Directory usando una nuova esperienza utente in centro di amministrazione di sistema (o PowerShell) che consente all'amministratore di creare un limite e specificare un set di CAPRs che costituiscono il limite.

 

 
