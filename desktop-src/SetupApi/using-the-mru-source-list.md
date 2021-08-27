---
description: La funzione SetupSetSourceList aprirà o creerà un elenco di origine nel sistema degli utenti.
ms.assetid: cda632cf-6c92-48fb-aef1-25b320affd3e
title: Uso dell'elenco di origini MRU
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ada1fa55a1c0defea2f344200eb331b8031dedfa66336510fb55b6fb77213a24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100631"
---
# <a name="using-the-mru-source-list"></a>Uso dell'elenco di origini MRU

La [**funzione SetupSetSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetsourcelista) aprirà o creerà un elenco di origine nel sistema dell'utente. È possibile specificare di impostare l'elenco utenti, l'elenco di sistema, una combinazione di elenchi di utenti e di sistema o un elenco temporaneo come elenco di origine MRU. Se viene usato un elenco temporaneo, sarà l'unico elenco disponibile per l'applicazione di installazione fino a quando non viene chiamato [**SetupCancelTemporarySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupcanceltemporarysourcelist) o non viene chiamato **SetupSetSourceList** una seconda volta.

Dopo aver impostato un elenco, è possibile eseguire una query sull'elenco di origine usando [**SetupQuerySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerysourcelista) per ottenere una matrice dei percorsi di origine. Quando la matrice dell'elenco di origine non è più necessaria, è necessario chiamare la funzione [**SetupFreeSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupfreesourcelista) per liberare le risorse allocate da [**SetupQuerySourceList.**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerysourcelista)

Per aggiungere un percorso a un elenco di origine, uno che risiede nel sistema dell'utente o un elenco temporaneo, chiamare [**SetupAddToSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtosourcelista). Se l'elenco di origine specificato non è temporaneo, tale origine rimarrà nel sistema dell'utente ed è accessibile alle installazioni successive.

Per rimuovere un percorso dal percorso di origine, chiamare la [**funzione SetupRemoveFromSourceList.**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromsourcelista)

 

 



