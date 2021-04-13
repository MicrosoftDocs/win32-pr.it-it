---
description: Poiché i socket non sono rappresentati dall'intero di tipo UNIX, piccolo e non negativo, l'implementazione della funzione Select è stata modificata in Windows Sockets.
ms.assetid: 97c7996c-c541-4673-b26f-d66f3fc0b62e
title: Macro Select, FD_SET e FD_XXX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b9bce15e921bf6566717a30114af73530406e5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528627"
---
# <a name="select-fd_set-and-fd_xxx-macros"></a>Macro Select, FD \_ set e FD \_ xxx

Poiché i socket non sono rappresentati dall'intero di tipo UNIX, piccolo e non negativo, l'implementazione della funzione [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) è stata modificata in Windows Sockets. Ogni set di socket è ancora rappresentato dalla struttura **del \_ set FD** , ma anziché essere archiviato come maschera di maschera, il set viene implementato come una matrice di socket. Per evitare potenziali problemi, le applicazioni devono essere conformi all'uso delle \_ macro fd xxx per impostare, inizializzare, cancellare e controllare le strutture del [**\_ set FD**](/windows/desktop/api/winsock/nf-winsock-fd_set) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Porting delle applicazioni socket in Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Considerazioni sulla programmazione Winsock](winsock-programming-considerations.md)
</dt> </dl>

 

 



