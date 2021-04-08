---
description: Chiusura di una connessione Schannel
ms.assetid: 7081ba1f-df3c-41b4-96da-24d44e74d714
title: Chiusura di una connessione Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc61b67083ceee65da714069c2b30ba1bfd5c89b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749602"
---
# <a name="shutting-down-an-schannel-connection"></a>Chiusura di una connessione Schannel

Al termine della connessione, un client o un server deve arrestarlo. L'altra parte, a sua volta, deve riconoscere l'arresto ed eliminare la connessione.

**Per arrestare una connessione Schannel**

1.  Chiamare la funzione [**ApplyControlToken**](/windows/desktop/api/Sspi/nf-sspi-applycontroltoken) , specificando il \_ token di controllo di arresto di Schannel.
2.  Dopo \_ la ricezione di un \_ valore restituito sec E OK da [**ApplyControlToken**](/windows/desktop/api/Sspi/nf-sspi-applycontroltoken), chiamare la funzione [**InitializeSecurityContext (Schannel)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) (clients) o [**AcceptSecurityContext (Schannel)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) (Servers), passando i buffer vuoti.
3.  Continuare come se l'applicazione creasse una nuova connessione fino a quando la funzione restituisce il \_ contesto di secondo i non \_ \_ scaduto o sec \_ E \_ OK per indicare che la connessione è stata arrestata.
4.  Inviare le informazioni di output finale, se presenti, alla parte remota.
5.  Chiamare [**DeleteSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) per liberare risorse detenute dalla connessione.

## <a name="recognizing-a-shutdown"></a>Riconoscimento di un arresto

La funzione [**DecryptMessage (Schannel)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) restituisce il \_ contesto di sec i \_ \_ scaduto quando il mittente del messaggio chiude la connessione. Dopo la ricezione del valore restituito, attenersi alla procedura per arrestare una connessione Schannel, più indietro in questo argomento.

 

 
