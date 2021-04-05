---
description: La funzione SetupSetSourceList consente di aprire o creare un elenco di origine nel sistema utenti.
ms.assetid: cda632cf-6c92-48fb-aef1-25b320affd3e
title: Uso dell'elenco di origine MRU
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dbecb9e32a554d1818661b1fd7f6e782744c16e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967176"
---
# <a name="using-the-mru-source-list"></a>Uso dell'elenco di origine MRU

La funzione [**SetupSetSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetsourcelista) aprirà o creerà un elenco di origine nel sistema dell'utente. È possibile specificare per impostare l'elenco di utenti, l'elenco di sistema, una combinazione degli elenchi di utenti e di sistema o un elenco temporaneo come elenco di origine MRU. Se viene usato un elenco temporaneo, sarà l'unico elenco disponibile per l'applicazione di installazione fino a quando non viene chiamato [**SetupCancelTemporarySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupcanceltemporarysourcelist) oppure **SetupSetSourceList** viene chiamato una seconda volta.

Dopo aver impostato un elenco, è possibile eseguire una query sull'elenco di origine usando [**SetupQuerySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerysourcelista) per ottenere una matrice dei percorsi di origine. Quando la matrice dell'elenco di origine non è più necessaria, è necessario chiamare la funzione [**SetupFreeSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupfreesourcelista) per liberare le risorse allocate da [**SetupQuerySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerysourcelista).

Per aggiungere un percorso a un elenco di origine, ovvero uno che risiede nel sistema dell'utente o un elenco temporaneo, chiamare [**SetupAddToSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtosourcelista). Se l'elenco di origine specificato non è temporaneo, tale origine rimarrà nel sistema dell'utente e sarà accessibile alle installazioni successive.

Per rimuovere un percorso dal percorso di origine, chiamare la funzione [**SetupRemoveFromSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromsourcelista) .

 

 



