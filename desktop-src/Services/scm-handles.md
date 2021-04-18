---
description: SCM supporta i tipi di handle per consentire l'accesso agli oggetti seguenti.
ms.assetid: 5ffdd1a9-1a66-4fc4-b35d-4f744bae4897
title: Handle SCM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c8a84fb09dbc95f3e1b5f5cee432de616f5ff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318221"
---
# <a name="scm-handles"></a>Handle SCM

SCM supporta i tipi di handle per consentire l'accesso agli oggetti seguenti.

-   Database dei servizi installati.
-   Un servizio.
-   Blocco del database.

Un oggetto SCManager rappresenta il database dei servizi installati. Si tratta di un oggetto contenitore che include oggetti servizio. La funzione [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) restituisce un handle a un oggetto SCManager in un computer specificato. Questo handle viene utilizzato per l'installazione, l'eliminazione, l'apertura e l'enumerazione dei servizi e per il blocco del database dei servizi.

Un oggetto servizio rappresenta un servizio installato. Le funzioni [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) e [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) restituiscono handle ai servizi installati.

Le funzioni [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera), [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)e [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) possono richiedere tipi diversi di accesso agli oggetti SCManager e Service. L'accesso richiesto viene concesso o negato a seconda del token di accesso del processo chiamante e del descrittore di sicurezza associato all'oggetto SCManager o al servizio.

La funzione [**CloseServiceHandle**](/windows/desktop/api/Winsvc/nf-winsvc-closeservicehandle) chiude gli handle agli oggetti SCManager e Service. Quando questi handle non sono più necessari, assicurarsi di chiuderli.

 

 



