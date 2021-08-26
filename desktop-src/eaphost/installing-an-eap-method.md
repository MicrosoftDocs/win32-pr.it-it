---
title: Installazione di un metodo EAP
description: Seguire le istruzioni seguenti per installare un metodo EAP implementato dall'utente in un computer client che esegue EAPHost.
ms.assetid: c353550f-73a7-4195-81ea-544f74abc880
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e047c5a8f0bc4cedcc207016d6f66530b392869839dda128635cd31ac459011a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021581"
---
# <a name="installing-an-eap-method"></a>Installazione di un metodo EAP

Seguire le istruzioni seguenti per installare un metodo EAP implementato dall'utente in un computer client che esegue EAPHost.

-   Implementare [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) e [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) per la DLL del metodo EAP. Queste funzioni aggiungono e rimuovono le chiavi del Registro di sistema appropriate per il metodo EAP durante il processo di installazione e disinstallazione.

    Per informazioni sulle chiavi del Registro di sistema specifiche associate all'installazione di un metodo EAP, vedere l'argomento Configurazione del Registro di sistema [per i metodi EAP.](registry-keys-for-eap-methods.md)

-   Installare la DLL che contiene l'implementazione del metodo EAP con il comando della console seguente.

    **regsvr32.exe** *&lt; dll &gt;*

    Per disinstallare la DLL, usare il comando della console seguente:

    **regsvr32.exe** **dll /u** *&lt; &gt;*

-   Riavviare il servizio EAPHost.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di EAPHost](using-eap-host.md)
</dt> </dl>

 

 