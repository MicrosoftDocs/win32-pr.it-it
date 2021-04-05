---
title: Linee guida sulla sicurezza
description: È importante informare l'utente sui possibili problemi di sicurezza.
ms.assetid: f0c041fd-3cc5-491e-b088-6c93fcd61def
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b3d4214ba4582394ed555bafd58551e8b047493
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118219"
---
# <a name="security-guideline"></a>Linee guida sulla sicurezza

È importante informare l'utente sui possibili problemi di sicurezza.

## <a name="notify-the-user-of-security-related-events"></a>Invia notifica all'utente di eventi Security-Related

Informare sempre l'utente di eventuali modifiche apportate alla sicurezza, sia che si tratti di un errore correlato alla sicurezza, ad esempio un errore di certificato, o di una modifica della sicurezza del protocollo sottostante, ad esempio il passaggio da un sito HTTPS a un sito HTTP.

## <a name="notify-the-user-of-security-related-errors"></a>Notifica all'utente Security-Related errori

Quando l'applicazione riceve un messaggio di errore che può indicare un problema di sicurezza, la funzione **InternetErrorDlg** fornisce un'interfaccia standard e familiare per inviare una notifica all'utente nella maggior parte dei casi.

Tra gli errori che rientrano in questa categoria:

**ERRORE \_ \_ da http \_ a HTTPS da Internet a \_ \_ \_ redir**

**ERRORE \_ Internet \_ CA non valida \_**

**ERRORE \_ Internet \_ Post \_ \_ non \_ sicuro**

**\_errori del certificato di Internet \_ sec errore \_ \_**

**ERRORE per il \_ \_ certificato CN di Internet sec \_ \_ \_ non valido**

**ERRORE in \_ Internet \_ sec \_ CERT \_ data \_ non valida**

Un errore di notifica all'utente di errori come questi possono esporre l'utente a vari tipi di violazioni della sicurezza, inclusi gli attacchi di spoofing o la divulgazione di informazioni non volontarie.

## <a name="notify-the-user-when-connection-security-changes"></a>Notifica all'utente quando viene modificata la sicurezza della connessione

Inviare sempre notifiche all'utente quando viene modificata la sicurezza della connessione, ad esempio da HTTPS a HTTP. In caso contrario, a meno che l'utente non abbia scelto in modo esplicito di non ricevere notifiche di tali modifiche, si nascondono i rischi derivanti dalla divulgazione involontaria di informazioni.

Tra le funzioni che segnalano una modifica di questo tipo nella sicurezza delle connessioni si trovano la funzione di callback **InternetStatusCallback** e la funzione **InternetConfirmZoneCrossing** .

> [!Note]  
> WinINet non supporta le implementazioni del server. Inoltre, non deve essere utilizzato da un servizio. Per le implementazioni o i servizi del server, usare i [Servizi http di Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 