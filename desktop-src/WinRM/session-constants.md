---
title: Costanti di sessione
description: Le costanti di sessione nell' \_ \_ enumerazione WSManSessionFlags specificano l'autenticazione e altre informazioni per le chiamate a WSMan. CreateSession o IWSMan CreateSession che si connettono a un computer remoto.
ms.assetid: 5df52696-ac2c-42b7-8b0f-99a27b58575b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8417289a218203dbdaee288ff03096d894f4bd4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297817"
---
# <a name="session-constants"></a>Costanti di sessione

Le costanti di sessione nell'enumerazione **\_ \_ WSManSessionFlags** specificano l'autenticazione e altre informazioni per le chiamate [**WSMan. CreateSession**](wsman-createsession.md) o [**IWSMan:: CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession) che si connettono a un computer remoto. Queste costanti sono anche strettamente correlate alle opzioni dello strumento da riga di comando **WinRM** .

## <a name="using-session-constants"></a>Utilizzo delle costanti di sessione

È possibile impostare i flag di sessione per la chiamata a [**WSMan. CreateSession**](wsman-createsession.md) in due modi diversi. Uno è più breve e più semplice. Il modo più lungo, come illustrato nell'esempio seguente, consiste nell'individuare il valore del flag che si vuole usare e creare una costante nello script con tale valore. La costante viene quindi utilizzata per impostare il valore del parametro *iFlags* .

``` syntax
Const SessionFlagUseNegotiate = 131072
Const SessionFlagCredUserNamePassword = 4096
iFlags = SessionFlagUseNegotiate Or SessionFlagCredUserNamePassword
```

La modalità consigliata, come illustrato nell'esempio seguente, consiste nell'usare il metodo dell'oggetto [**WSMan**](wsman.md) associato al flag.

``` syntax
iFlags = Wsman.SessionFlagUseNegotiate Or Wsman.SessionFlagCredUserNamePassword
```

<dl> <dt>

<span id="Authentication_Constants"></span><span id="authentication_constants"></span><span id="AUTHENTICATION_CONSTANTS"></span>[**Costanti di autenticazione**](authentication-constants.md)
</dt> <dd>

Specificare il metodo di autenticazione e la modalità di gestione dei server di certificati.

</dd> <dt>

<span id="Other_Session_Constants"></span><span id="other_session_constants"></span><span id="OTHER_SESSION_CONSTANTS"></span>[**Altre costanti di sessione**](other-session-constants.md)
</dt> <dd>

Specificare la porta di codifica, crittografia e nome dell'entità servizio.

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti ed enumerazioni WinRM](winrm-constants-and-enumerations.md)
</dt> <dt>

[**WSMan. CreateSession**](wsman-createsession.md)
</dt> <dt>

[Autenticazione per le connessioni remote](authentication-for-remote-connections.md)
</dt> </dl>

 

 




