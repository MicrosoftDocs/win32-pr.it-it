---
description: Quando si apre un handle a un oggetto, l'handle restituito dispone di una combinazione di diritti di accesso all'oggetto.
ms.assetid: 581de4ba-0f90-42d7-b7db-1324d42595e2
title: Richiesta di diritti di accesso a un oggetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a168a5c9aa97d95acb13cb1cfeb3e776ea1e7ae6e2e090df5c8395a4b61fabea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907541"
---
# <a name="requesting-access-rights-to-an-object"></a>Richiesta di diritti di accesso a un oggetto

Quando si apre un handle a un oggetto, l'handle restituito dispone di una combinazione di diritti di accesso all'oggetto. Alcune funzioni, ad esempio [**CreateSemaphore,**](/windows/desktop/api/winbase/nf-winbase-createsemaphorea)non richiedono un set specifico di diritti di accesso richiesti. Queste funzioni tentano sempre di aprire l'handle per l'accesso completo. Altre funzioni, ad esempio [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) e [**OpenProcess,**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess)consentono di specificare il set di diritti di accesso desiderati. È consigliabile richiedere solo i diritti di accesso necessari, anziché aprire un handle per l'accesso completo. Ciò impedisce di usare l'handle in modo imprevisto e aumenta le probabilità che la richiesta di accesso riesca se l'elenco DACL dell'oggetto consente solo l'accesso limitato.

Usare [i diritti di accesso generici](generic-access-rights.md) per specificare il tipo di accesso necessario quando si apre un handle a un oggetto. Questa operazione è in genere più semplice rispetto alla specifica di tutti i diritti standard e specifici corrispondenti. In alternativa, usare la costante MAXIMUM ALLOWED per richiedere che l'oggetto sia aperto con tutti i diritti di \_ accesso validi per il chiamante.

> [!Note]  
> La costante MAXIMUM \_ ALLOWED non può essere utilizzata in una ACE.

 

Per ottenere o impostare l'elenco SACL nel descrittore di sicurezza di un oggetto [*,*](/windows/desktop/SecGloss/s-gly)richiedere il diritto di accesso ACCESS [SYSTEM \_ \_ SECURITY](sacl-access-right.md) all'apertura di un handle per l'oggetto.

 

 
