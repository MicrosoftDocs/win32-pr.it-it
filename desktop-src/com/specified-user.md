---
title: Utente specificato
description: Utente specificato
ms.assetid: ec7684fb-a9f1-4ef2-a7d4-07caf24b6023
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acce63aa502a8966cd0eb53c90dcca3c4454e80b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298000"
---
# <a name="specified-user"></a>Utente specificato

Specificare un utente specifico (e la password dell'utente) è l'identità preferita per i server COM. Il motivo per cui questa identità è preferibile è che nessuno deve essere registrato nel computer in cui è in esecuzione il server per l'esecuzione del server e ogni client comunica con la stessa istanza del server se il server ne registra la class factory come multiutilizzo. Se il server dispone di un'interfaccia utente grafica, non scegliere questa identità; in tal caso, l'utente non sarà in grado di visualizzare l'interfaccia utente.

Questo tipo di server ha un token primario e può accedere alle risorse remote in cui un server con l'identità dell'utente che ha avviato l'avvio potrebbe non riuscire. Per ulteriori informazioni sui token di accesso e di rappresentazione, vedere [livelli di rappresentazione](impersonation-levels.md) e [mascheramento](cloaking.md).

L'esecuzione come account utente fisso è più sicura dell'identità utente interattiva perché questa identità può essere assegnata all'applicazione solo da un utente che ha la password di un utente specifico.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Identità applicazione](application-identity.md)
</dt> <dt>

[Utente interattivo](interactive-user.md)
</dt> <dt>

[Avvio dell'utente](launching-user.md)
</dt> <dt>

[Identità del servizio](service-identity.md)
</dt> </dl>

 

 




