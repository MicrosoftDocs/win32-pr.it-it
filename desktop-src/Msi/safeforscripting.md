---
description: Se questo criterio di sistema per computer è impostato su &\# 0034;1&0034;, il programma di installazione non richiede agli utenti quando gli script all'interno di una pagina Web usano l'interfaccia di automazione del programma di \# installazione.
ms.assetid: 1365996d-30a2-43f9-8e1b-7704d46a11c9
title: SafeForScripting
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b9a78bded284a687994075fdda1276122df2ab68716c4aaf759b4f5750aeb15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117990151"
---
# <a name="safeforscripting"></a>SafeForScripting

Se questo criterio di [sistema](system-policy.md) per computer è impostato su "1", il programma di installazione non richiede agli utenti quando gli script all'interno di una pagina Web usano l'interfaccia di automazione del programma [di installazione.](automation-interface.md)

Prima di impostare questo criterio, è necessario valutare se la richiesta dell'utente fornisce un livello di sicurezza appropriato per gli utenti. Se questo criterio non è impostato, quando uno script ospitato da un browser Internet tenta di installare un'applicazione, il sistema avvisa l'utente e chiede di accettare o rifiutare l'installazione. L'impostazione di SafeForScripting elimina questo avviso e può consentire l'installazione di applicazioni nel sistema all'insaputa dell'utente. Questo criterio può essere utile per un'azienda che usa strumenti basati sul Web per distribuire programmi.

Per altre informazioni, vedere [Linee guida](guidelines-for-authoring-secure-installations.md) per la creazione di installazioni protette e firme digitali [e](digital-signatures-and-windows-installer.md) Windows programma di installazione e Download di un'installazione [da Internet.](downloading-an-installation-from-the-internet.md)

## <a name="registry-key"></a>Chiave del Registro di sistema

**HKEY \_ Criteri \_ software di LOCAL MACHINE** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo di dati

**REG \_ DWORD**

 

 



