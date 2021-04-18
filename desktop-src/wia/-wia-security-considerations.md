---
description: In questo documento vengono fornite informazioni sulle considerazioni relative alla sicurezza relative all'acquisizione di immagini Windows (WIA).
ms.assetid: 35455320-7d08-49de-938d-40dc0873917b
title: 'Considerazioni sulla sicurezza: acquisizione di immagini Windows'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9ab080582492a0c03eab7879624bfb49a370e6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307336"
---
# <a name="security-considerations-windows-image-acquisition"></a>Considerazioni sulla sicurezza: acquisizione di immagini Windows

In questo documento vengono fornite informazioni sulle considerazioni relative alla sicurezza relative all'acquisizione di immagini Windows (WIA). Questo documento non fornisce tutte le informazioni necessarie per i problemi di sicurezza, ma è possibile usarlo come punto di partenza e come riferimento per questa area tecnologica.

-   [Racchiudere tra virgolette i nomi di percorso](#use-quotation-marks-around-path-names)
-   [Inserire applicazioni registrate in posizioni sicure](#place-registered-applications-in-secure-locations)
-   [Non usare directory sottostanti o chiavi del registro di sistema](#do-not-use-underlying-directories-or-registry-keys)
-   [Argomenti correlati](#related-topics)

## <a name="use-quotation-marks-around-path-names"></a>Racchiudere tra virgolette i nomi di percorso

Quando si usa [**IWiaDevMgr:: RegisterEventCallbackProgram**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackprogram) per registrare un'applicazione per la ricezione di eventi del dispositivo, assicurarsi di racchiudere il percorso e il nome file dell'applicazione con virgolette. In questo modo si evita la possibilità che il percorso venga interpretato erroneamente e venga eseguita un'applicazione non autorizzata.

## <a name="place-registered-applications-in-secure-locations"></a>Inserire applicazioni registrate in posizioni sicure

Quando un'applicazione viene registrata per ricevere un evento del dispositivo, l'applicazione può essere eseguita da qualsiasi utente che abbia accesso a tale dispositivo. Se, ad esempio, un'applicazione è registrata per un evento di analisi, quando si preme il pulsante "analizza" su uno scanner verrà eseguita l'applicazione. Se l'applicazione viene eseguita con un privilegio più elevato rispetto a quello dell'utente, questo causa un potenziale problema di sicurezza.

## <a name="do-not-use-underlying-directories-or-registry-keys"></a>Non usare directory sottostanti o chiavi del registro di sistema

WIA utilizza internamente più directory e chiavi del registro di sistema per archiviare dati o informazioni. Non accedere direttamente a tali directory o chiavi del registro di sistema. Usare invece i metodi di interfaccia esposti per specificare le directory per le immagini acquisite.

## <a name="related-topics"></a>Argomenti correlati

-   [Microsoft Security](https://www.microsoft.com/security/)
-   [Home page di sicurezza MSDN Library](https://msdn.microsoft.com/security/default.aspx)
-   [Risorse sulle procedure di sicurezza](https://www.microsoft.com/technet/solutionaccelerators/howto/sechow.mspx)
-   [Risorse di sicurezza TechNet](https://technet.microsoft.com/security/default.aspx)
-   [Considerazioni sulla sicurezza per gli sviluppatori di Windows XP Embedded](/previous-versions/ms838345(v=msdn.10))
-   [Procedure di sicurezza consigliate](../secbp/best-practices-for-the-security-apis.md)

 

 
