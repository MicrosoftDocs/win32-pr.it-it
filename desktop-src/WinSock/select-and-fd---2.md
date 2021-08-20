---
description: Poiché i socket non sono rappresentati da un numero intero piccolo e non negativo di tipo UNIX, l'implementazione della funzione select è stata modificata in Windows Socket.
ms.assetid: 97c7996c-c541-4673-b26f-d66f3fc0b62e
title: Selezionare, FD_SET e FD_XXX macro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4468e889d8eae0339513519c7e6ae62df9c6f06013a7a81866eda9c6a914360
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118111602"
---
# <a name="select-fd_set-and-fd_xxx-macros"></a>Macro Select, FD SET e \_ FD \_ XXX

Poiché i socket non sono rappresentati da un numero intero piccolo e non negativo di tipo UNIX, l'implementazione della funzione [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) è stata modificata in Windows Socket. Ogni set di socket è ancora rappresentato dalla struttura **\_ FD SET,** ma invece di essere archiviato come maschera di bit, il set viene implementato come matrice di socket. Per evitare potenziali problemi, le applicazioni devono rispettare l'uso delle macro FD XXX per impostare, inizializzare, cancellare e controllare \_ le [**strutture \_ FD SET.**](/windows/desktop/api/winsock/nf-winsock-fd_set)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Porting di applicazioni socket in Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Considerazioni sulla programmazione winsock](winsock-programming-considerations.md)
</dt> </dl>

 

 



