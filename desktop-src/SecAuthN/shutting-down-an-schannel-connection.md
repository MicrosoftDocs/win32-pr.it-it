---
description: Arresto di una connessione Schannel
ms.assetid: 7081ba1f-df3c-41b4-96da-24d44e74d714
title: Arresto di una connessione Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb700c8ac896d0e64b82b25371ea67cc343d8297c95445ca4126c5718d8024a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118918060"
---
# <a name="shutting-down-an-schannel-connection"></a>Arresto di una connessione Schannel

Quando un client o un server termina con una connessione, deve arrestarlo. L'altra parte, a sua volta, deve riconoscere l'arresto ed eliminare la connessione.

**Per arrestare una connessione Schannel**

1.  Chiamare la [**funzione ApplyControlToken,**](/windows/desktop/api/Sspi/nf-sspi-applycontroltoken) specificando il token di controllo SHUTDOWN SCHANNEL. \_
2.  Dopo aver ricevuto un valore restituito SEC E OK da ApplyControlToken, chiamare la funzione \_ \_ [**InitializeSecurityContext (Schannel) (client)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) o [**AcceptSecurityContext (Schannel) (servers),**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) passando buffer vuoti. [](/windows/desktop/api/Sspi/nf-sspi-applycontroltoken)
3.  Procedere come se l'applicazione crea una nuova connessione fino a quando la funzione non restituisce SEC I CONTEXT EXPIRED o SEC E OK per indicare che la \_ \_ connessione è stata \_ \_ \_ arrestata.
4.  Inviare le eventuali informazioni di output finali all'entità remota.
5.  Chiamare [**DeleteSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) per liberare le risorse utilizzate dalla connessione.

## <a name="recognizing-a-shutdown"></a>Riconoscimento di un arresto

La [**funzione DecryptMessage (Schannel)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) restituisce SEC \_ I CONTEXT EXPIRED quando il \_ \_ mittente del messaggio ha arrestato la connessione. Dopo aver ricevuto questo valore restituito, seguire la procedura Per arrestare una connessione Schannel, più indietro in questo argomento.

 

 
