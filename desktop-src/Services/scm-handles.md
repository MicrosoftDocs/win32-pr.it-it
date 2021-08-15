---
description: Gestione controllo servizi supporta i tipi di handle per consentire l'accesso agli oggetti seguenti.
ms.assetid: 5ffdd1a9-1a66-4fc4-b35d-4f744bae4897
title: Handle SCM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6830063e57b2135c32bf01b4fdc0b4cf6207de32198d9f88d97667f4b403fe2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118889189"
---
# <a name="scm-handles"></a>Handle SCM

Gestione controllo servizi supporta i tipi di handle per consentire l'accesso agli oggetti seguenti.

-   Database dei servizi installati.
-   Un servizio.
-   Blocco del database.

Un oggetto SCManager rappresenta il database dei servizi installati. Si tratta di un oggetto contenitore che contiene oggetti servizio. La [**funzione OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) restituisce un handle a un oggetto SCManager in un computer specificato. Questo handle viene utilizzato durante l'installazione, l'eliminazione, l'apertura e l'enumerazione dei servizi e durante il blocco del database dei servizi.

Un oggetto servizio rappresenta un servizio installato. Le [**funzioni CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) [**e OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) restituiscono handle ai servizi installati.

Le [**funzioni OpenSCManager,**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)e [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) possono richiedere diversi tipi di accesso a SCManager e agli oggetti servizio. L'accesso richiesto viene concesso o negato a seconda del token di accesso del processo chiamante e del descrittore di sicurezza associato a SCManager o all'oggetto servizio.

La [**funzione CloseServiceHandle**](/windows/desktop/api/Winsvc/nf-winsvc-closeservicehandle) chiude gli handle a SCManager e agli oggetti servizio. Quando questi handle non sono più necessari, assicurarsi di chiuderli.

 

 



