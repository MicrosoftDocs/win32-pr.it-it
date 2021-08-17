---
description: Un amministratore può usare i metodi seguenti per consentire a un utente non amministratore di installare un'applicazione con privilegi di sistema elevati.
ms.assetid: 61b9297e-f45e-4f50-9001-9bae580e1bf4
title: Installazione di un pacchetto con privilegi elevati per utenti non amministratori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 603d2a39fd20a6ae2971a29e615887041e2a1fbf64989e93d5a1046f96102b5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946109"
---
# <a name="installing-a-package-with-elevated-privileges-for-a-non-admin"></a>Installazione di un pacchetto con privilegi elevati per utenti non amministratori

Un amministratore può usare i metodi seguenti per consentire a un utente non amministratore di installare un'applicazione con privilegi di sistema elevati.

-   In Windows Vista con il programma di installazione di Windows, un membro del gruppo Administrators può [](u-gly.md) fornire a un utente non amministratore l'autorizzazione per elevare i privilegi dell'installazione tramite Controllo dell'account utente, come descritto in Uso del programma di installazione di [Windows](using-windows-installer-with-uac.md)con Controllo dell'account utente.

    **Windows Vista:** Obbligatorio.

I metodi seguenti possono essere usati anche per installare un'applicazione con privilegi di sistema elevati.

-   Un amministratore può annunciare un'applicazione nel computer di un utente assegnando o pubblicando il pacchetto Windows Installer usando la distribuzione dell'applicazione [e Criteri di gruppo](/previous-versions/windows/desktop/Policy/group-policy-start-page). L'amministratore annuncia il pacchetto per l'installazione per computer. Se un utente non amministratore installa l'applicazione, l'installazione può essere eseguita con privilegi elevati. Gli utenti non amministratori non possono installare pacchetti non invertiti che richiedono privilegi di sistema elevati.
-   Un amministratore può accedere al computer dell'utente e [annunciare l'applicazione](advertisement.md) per l'installazione per computer. Poiché il programma di installazione di Windows ha sempre privilegi elevati durante le installazioni nel contesto di installazione per [computer,](installation-context.md)se un utente non amministratore installa l'applicazione annunciata, l'installazione può essere eseguita con privilegi elevati. Gli utenti non amministratori non possono comunque installare pacchetti non invertiti che richiedono privilegi elevati.
-   Un utente senza privilegi può installare un'applicazione annunciata che richiede privilegi elevati se un agente di sistema locale annuncia l'applicazione. L'applicazione può essere annunciata per un'installazione per utente o per computer. Un'applicazione installata con questo metodo viene considerata gestita. Per altre informazioni, vedere [Advertising a Per-User Application To Be Installed with Elevated Privileges](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md).
-   Un amministratore può impostare i [criteri AlwaysInstallElevated](alwaysinstallelevated.md) sia per le installazioni per utente che per computer. Questo metodo può aprire un computer a un rischio per la sicurezza, perché quando questo criterio è impostato, un utente non amministratore può eseguire installazioni con privilegi elevati e accedere a percorsi sicuri nel computer, ad esempio SystemFolder o la chiave del Registro di sistema **HKLM.**

    Se l'applicazione viene installata per computer mentre è impostato il criterio [AlwaysInstallElevated,](alwaysinstallelevated.md) il prodotto viene considerato gestito. In questo caso, l'applicazione può comunque eseguire un ripristino con privilegi elevati se i criteri vengono rimossi. Inoltre, se l'applicazione viene installata per utente mentre è impostato il criterio AlwaysInstallElevated, l'applicazione non è in grado di eseguire un ripristino se i criteri vengono rimossi.

-   Un amministratore può accedere al computer di un utente ed eseguire un'installazione per computer dell'applicazione. Poiché per eseguire questo tipo di installazione sono necessari privilegi, le installazioni per computer vengono sempre gestite.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Contesto di installazione](installation-context.md)
</dt> </dl>

 

 
