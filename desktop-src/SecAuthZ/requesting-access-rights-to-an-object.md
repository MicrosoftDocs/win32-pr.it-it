---
description: Quando si apre un handle per un oggetto, l'handle restituito dispone di una combinazione di diritti di accesso all'oggetto.
ms.assetid: 581de4ba-0f90-42d7-b7db-1324d42595e2
title: Richiesta di diritti di accesso a un oggetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eb2e13bd5f5e51ed194b60c6ab63d1eda8eddfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308144"
---
# <a name="requesting-access-rights-to-an-object"></a>Richiesta di diritti di accesso a un oggetto

Quando si apre un handle per un oggetto, l'handle restituito dispone di una combinazione di diritti di accesso all'oggetto. Alcune funzioni, ad esempio [**CreateSemaphore**](/windows/desktop/api/winbase/nf-winbase-createsemaphorea), non richiedono un set specifico di diritti di accesso richiesti. Queste funzioni tentano sempre di aprire l'handle per l'accesso completo. Altre funzioni, ad esempio [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) e [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess), consentono di specificare il set di diritti di accesso desiderato. È necessario richiedere solo i diritti di accesso necessari, anziché aprire un handle per l'accesso completo. In questo modo si impedisce l'utilizzo dell'handle in modo indesiderato e aumentano le probabilità che la richiesta di accesso abbia esito positivo se l'elenco DACL dell'oggetto consente l'accesso limitato.

Usare [i diritti di accesso generici](generic-access-rights.md) per specificare il tipo di accesso necessario quando si apre un handle a un oggetto. Questa operazione è in genere più semplice rispetto a specificare tutti i diritti standard e specifici corrispondenti. In alternativa, utilizzare la \_ costante massima consentita per richiedere che l'oggetto venga aperto con tutti i diritti di accesso validi per il chiamante.

> [!Note]  
> \_Impossibile utilizzare la costante massima consentita in una voce ACE.

 

Per ottenere o impostare l'elenco SACL nel [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly)di un oggetto, richiedere il [diritto di accesso alla \_ \_ sicurezza del sistema di accesso](sacl-access-right.md) quando si apre un handle per l'oggetto.

 

 
