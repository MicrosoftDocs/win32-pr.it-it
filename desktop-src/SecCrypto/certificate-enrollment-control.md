---
description: Il controllo della registrazione dei certificati può essere utilizzato da un'applicazione che deve richiedere l'emissione di un certificato a un oggetto denominato.
ms.assetid: ce6661b0-7ed2-452f-a54c-6705d14f3298
title: Controllo di registrazione certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e417a9db7984cbb58b7c2e3b51d828b6d61a97b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306542"
---
# <a name="certificate-enrollment-control"></a>Controllo di registrazione certificati

Il controllo della registrazione dei certificati può essere utilizzato da un'applicazione che deve richiedere l'emissione di un certificato a un oggetto denominato. È progettato per accettare i dati sotto forma di stringa binaria (BSTR). I dati possono provenire da una pagina Web o dall'interfaccia utente del sistema di sviluppo Visual Basic o Visual C++. L'output del controllo di registrazione certificati è una \# richiesta di certificato PKCS 10 che può essere inviata a un'autorità di [*certificazione*](../secgloss/c-gly.md) (CA).

![controllo di registrazione certificati](images/xen-arch.png)

Le informazioni necessarie sull'utente, il soggetto del certificato, vengono raccolte dall'interfaccia utente. Queste informazioni vengono fornite come input BSTR per il controllo di registrazione del certificato. Il controllo di registrazione certificati genera la chiave di firma appropriata, la chiave per lo scambio delle chiavi o entrambe le coppie di chiavi. Il controllo genera quindi e firma una \# richiesta di [*certificato*](../secgloss/c-gly.md) PKCS 10 utilizzando la [*chiave privata*](../secgloss/p-gly.md)generata. Il controllo registrazione certificati collega quindi la coppia di chiavi a un certificato fittizio temporaneo archiviato nell'archivio richieste fino a quando il certificato emesso non viene restituito da un'autorità di certificazione. Infine, l'applicazione invia la \# richiesta di certificato PKCS 10 a una CA.

Se la CA approva la richiesta di certificato, la CA crea un certificato contenente la chiave pubblica. La CA firma e restituisce anche il certificato.

Quando il certificato richiesto viene restituito dalla CA, l'applicazione passa \# di nuovo il messaggio PKCS 7 al controllo di registrazione del certificato in cui il certificato o la catena di certificati viene estratta dal \# messaggio PKCS 7. Il certificato e tutti gli altri certificati nella catena di certificati vengono archiviati in un [*archivio certificati*](../secgloss/c-gly.md). Il certificato restituito non viene modificato in alcun modo. Qualsiasi applicazione in grado di riconoscere i certificati è ora in grado di accedere al certificato dall'archivio.

Il controllo registrazione smart card viene usato da un amministratore per eseguire la registrazione per conto di utenti di smart card. Il processo di registrazione comporta l'emissione di un certificato archiviato nella smart card di un utente.

Il controllo di registrazione delle smart card è contenuto in Scrdenrl.dll ed è costituito da un oggetto, **SCrdEnr**. Nessun altro oggetto incluso in Scrdenrl.dll. Questo oggetto di registrazione di smart card può essere utilizzato con un linguaggio di script, ad esempio Visual Basic Scripting Edition (VBScript).

Nel computer in cui è in esecuzione il controllo registrazione smart card deve essere installato un [*lettore di smart card*](../secgloss/r-gly.md) .

Inoltre, l'emittente della smart card deve avere ottenuto un certificato di firma basato sul modello di certificato "EnrollmentAgent". Questo certificato di firma verrà usato per firmare la richiesta di certificato generata per conto del destinatario della smart card. Per impostazione predefinita, agli amministratori di dominio viene concessa l'autorizzazione a richiedere un certificato basato sul modello "agente di registrazione". È possibile concedere a un altro utente l'autorizzazione per la registrazione di un certificato "EnrollmentAgent" (tramite lo snap-in MMC siti e servizi Active Directory); Questa operazione, tuttavia, consente a questo utente di emettere autonomamente una smart card con privilegi di amministratore di dominio.

 

 
