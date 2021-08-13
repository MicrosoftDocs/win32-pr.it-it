---
description: Questo documento fornisce informazioni sulle considerazioni sulla sicurezza relative all'acquisizione di immagini Windows (WIA).
ms.assetid: 35455320-7d08-49de-938d-40dc0873917b
title: "Considerazioni sulla sicurezza: Windows'acquisizione di immagini"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bb8f78e0f45b5b63d5d8deb8ffdd35bc64ee5566ced65ded30ecc51366c0793
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118439687"
---
# <a name="security-considerations-windows-image-acquisition"></a>Considerazioni sulla sicurezza: Windows'acquisizione di immagini

Questo documento fornisce informazioni sulle considerazioni sulla sicurezza relative all'acquisizione di immagini Windows (WIA). Questo documento non fornisce tutte le informazioni necessarie sui problemi di sicurezza, ma è possibile usarlo come punto di partenza e riferimento per questa area tecnologica.

-   [Usare le virgolette per i nomi di percorso](#use-quotation-marks-around-path-names)
-   [Posizionare le applicazioni registrate in posizioni sicure](#place-registered-applications-in-secure-locations)
-   [Non usare le directory sottostanti o le chiavi del Registro di sistema](#do-not-use-underlying-directories-or-registry-keys)
-   [Argomenti correlati](#related-topics)

## <a name="use-quotation-marks-around-path-names"></a>Usare le virgolette per i nomi di percorso

Quando si [**usa IWiaDevMgr::RegisterEventCallbackProgram**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackprogram) per registrare un'applicazione per ricevere eventi del dispositivo, assicurarsi di racchiudere il percorso e il nome file dell'applicazione tra virgolette. In questo modo si evita la possibilità che il percorso sia interpretato erroneamente e che un'applicazione non autorizzata sia in esecuzione.

## <a name="place-registered-applications-in-secure-locations"></a>Posizionare le applicazioni registrate in posizioni sicure

Quando un'applicazione viene registrata per ricevere un evento del dispositivo, tale applicazione può essere eseguita da qualsiasi utente che abbia accesso a tale dispositivo. Ad esempio, se un'applicazione è registrata per un evento di analisi, premendo il pulsante "scan" in uno scanner l'applicazione verrà eseguita. Se l'applicazione viene eseguita con privilegi più elevati di quelli dell'utente, si verifica un potenziale problema di sicurezza.

## <a name="do-not-use-underlying-directories-or-registry-keys"></a>Non usare le directory sottostanti o le chiavi del Registro di sistema

WiA usa internamente diverse directory e chiavi del Registro di sistema per archiviare dati o informazioni. Non accedere direttamente a queste directory o chiavi del Registro di sistema. Usare invece i metodi dell'interfaccia esposti per specificare le directory per le immagini acquisite.

## <a name="related-topics"></a>Argomenti correlati

-   [Microsoft Security](https://www.microsoft.com/security/)
-   [Home page sulla sicurezza di MSDN Library](https://msdn.microsoft.com/security/default.aspx)
-   [Risorse relative alle modalità di sicurezza](https://www.microsoft.com/technet/solutionaccelerators/howto/sechow.mspx)
-   [Risorse di sicurezza TechNet](https://technet.microsoft.com/security/default.aspx)
-   [Considerazioni sulla sicurezza per gli sviluppatori Windows XP Embedded](/previous-versions/ms838345(v=msdn.10))
-   [Procedure consigliate per la sicurezza](../secbp/best-practices-for-the-security-apis.md)

 

 
