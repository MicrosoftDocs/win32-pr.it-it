---
description: Un amministratore può utilizzare i metodi seguenti per consentire a un utente non amministratore di installare un'applicazione con privilegi di sistema elevati.
ms.assetid: 61b9297e-f45e-4f50-9001-9bae580e1bf4
title: Installazione di un pacchetto con privilegi elevati per un amministratore non
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec81de333d6ca388017e03c96f739d7bd258a7c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884870"
---
# <a name="installing-a-package-with-elevated-privileges-for-a-non-admin"></a>Installazione di un pacchetto con privilegi elevati per un amministratore non

Un amministratore può utilizzare i metodi seguenti per consentire a un utente non amministratore di installare un'applicazione con privilegi di sistema elevati.

-   In Windows Vista con Windows Installer, un membro del gruppo Administrators può fornire l'autorizzazione a un utente non amministratore per elevare l'installazione tramite [*controllo dell'account utente*](u-gly.md) (UAC), come descritto in [uso di Windows Installer con UAC](using-windows-installer-with-uac.md).

    **Windows Vista:** Obbligatorio.

I metodi seguenti possono essere usati anche per installare un'applicazione con privilegi di sistema elevati.

-   Un amministratore può pubblicizzare un'applicazione nel computer di un utente assegnando o pubblicando il pacchetto di Windows Installer usando la distribuzione dell'applicazione e [criteri di gruppo](/previous-versions/windows/desktop/Policy/group-policy-start-page). L'amministratore annuncia il pacchetto per l'installazione per computer. Se l'applicazione viene installata da un utente non amministratore, l'installazione può essere eseguita con privilegi elevati. Gli utenti non amministratori non possono installare pacchetti non pubblicizzati che richiedono privilegi di sistema elevati.
-   Un amministratore può accedere al computer dell'utente e [annunciare](advertisement.md) l'applicazione per l'installazione per computer. Poiché il Windows Installer dispone sempre di privilegi elevati durante le installazioni nel [contesto di installazione](installation-context.md)per computer, se un utente non amministratore installa l'applicazione annunciata, l'installazione può essere eseguita con privilegi elevati. Gli utenti non amministratori non possono ancora installare pacchetti non pubblicizzati che richiedono privilegi elevati.
-   Un utente senza privilegi può installare un'applicazione annunciata che richiede privilegi elevati se un agente di sistema locale annuncia l'applicazione. L'applicazione può essere annunciata per un'installazione per utente o per computer. Un'applicazione installata mediante questo metodo viene considerata gestita. Per ulteriori informazioni, vedere [la pagina relativa all'annuncio di un'applicazione Per-User da installare con privilegi elevati](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md).
-   Un amministratore può impostare i criteri [AlwaysInstallElevated](alwaysinstallelevated.md) per le installazioni per utente e per computer. Questo metodo può aprire un computer a un rischio per la sicurezza, perché quando questo criterio è impostato, un utente non amministratore può eseguire installazioni con privilegi elevati e accedere a posizioni sicure nel computer, ad esempio SystemFolder o la chiave del registro di sistema **HKLM** .

    Se l'applicazione viene installata per computer mentre è impostato il criterio [AlwaysInstallElevated](alwaysinstallelevated.md) , il prodotto viene considerato gestito. In questo caso, l'applicazione può comunque eseguire una correzione con privilegi elevati se i criteri vengono rimossi. Se, inoltre, l'applicazione è installata per utente mentre è impostato il criterio AlwaysInstallElevated, l'applicazione non è in grado di eseguire un ripristino se il criterio è stato rimosso.

-   Un amministratore può accedere al computer di un utente ed eseguire un'installazione per computer dell'applicazione. Poiché i privilegi sono necessari per eseguire questo tipo di installazione, le installazioni per computer sono sempre gestite.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Contesto di installazione](installation-context.md)
</dt> </dl>

 

 
