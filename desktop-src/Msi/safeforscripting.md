---
description: Se il criterio di sistema per computer è impostato su &\# 0034; 1&\# 0034;, il programma di installazione non richiede agli utenti quando gli script all'interno di una pagina Web utilizzano l'interfaccia di automazione del programma di installazione.
ms.assetid: 1365996d-30a2-43f9-8e1b-7704d46a11c9
title: SafeForScripting
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2907c4b021101ff936bdddf98a5cc1e32a01b991
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309448"
---
# <a name="safeforscripting"></a>SafeForScripting

Se il [criterio di sistema](system-policy.md) per computer è impostato su "1", il programma di installazione non richiede agli utenti quando gli script all'interno di una pagina Web utilizzano l' [interfaccia di automazione](automation-interface.md)del programma di installazione.

Prima di impostare questo criterio, è necessario valutare se la richiesta di conferma da parte dell'utente fornisca un livello di sicurezza appropriato per gli utenti. Se questo criterio non è impostato, quando uno script ospitato da un browser Internet tenta di installare un'applicazione, il sistema avvisa l'utente e chiede di accettare o rifiutare l'installazione. L'impostazione di SafeForScripting evita questo avviso e può consentire l'installazione di applicazioni nel sistema senza la conoscenza dell'utente. Questo criterio può essere utile per un'azienda che usa strumenti basati sul Web per distribuire i programmi.

Per ulteriori informazioni, vedere [linee guida per la creazione di installazioni protette](guidelines-for-authoring-secure-installations.md) e [firme digitali e Windows Installer](digital-signatures-and-windows-installer.md) e [il download di un'installazione da Internet](downloading-an-installation-from-the-internet.md).

## <a name="registry-key"></a>Chiave del Registro di sistema

**HKEY \_ Criteri software del \_ computer locale** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo di dati

**REG \_ DWORD**

 

 



