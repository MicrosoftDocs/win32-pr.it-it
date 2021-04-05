---
title: Installazione di un metodo EAP
description: Seguire le istruzioni riportate di seguito per installare un metodo EAP implementato dall'utente in un computer client che esegue EAPHost.
ms.assetid: c353550f-73a7-4195-81ea-544f74abc880
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e93e7796c216b5f60b7a46768ed9db9ca913482d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726287"
---
# <a name="installing-an-eap-method"></a>Installazione di un metodo EAP

Seguire le istruzioni riportate di seguito per installare un metodo EAP implementato dall'utente in un computer client che esegue EAPHost.

-   Implementare [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) e [**DLLUNREGISTERSERVER**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) per la dll del metodo EAP. Queste funzioni aggiungono e rimuovono le chiavi del registro di sistema appropriate per il metodo EAP durante il processo di installazione e (disinstallazione).

    Per informazioni sulle chiavi del registro di sistema specifiche associate all'installazione di un metodo EAP, vedere l'argomento configurazione del registro di sistema [per i metodi EAP](registry-keys-for-eap-methods.md) .

-   Installare la DLL che contiene l'implementazione del metodo EAP con il comando della console seguente.

     *&lt; Nome &gt; della dll* regsvr32.exe

    Per disinstallare la DLL, usare il comando console seguente:

    **regsvr32.exe** **/u** *&lt; nome &gt; dll*

-   Riavviare il servizio EAPHost.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di EAPHost](using-eap-host.md)
</dt> </dl>

 

 