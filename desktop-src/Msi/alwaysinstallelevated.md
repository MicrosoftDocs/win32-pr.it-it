---
description: Installare un pacchetto di Windows Installer con privilegi elevati (di sistema).
ms.assetid: 0bbec06a-0a2b-430a-a361-317a319da615
title: AlwaysInstallElevated
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c07e705e3e46a28049b6fb85eda96930d645a867
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528878"
---
# <a name="alwaysinstallelevated"></a>AlwaysInstallElevated

È possibile usare il criterio AlwaysInstallElevated per installare un pacchetto di Windows Installer con privilegi elevati (di sistema).

* * Avviso: * *

Questa opzione equivale alla concessione di diritti amministrativi completi che possono comportare un notevole rischio di sicurezza. Microsoft sconsiglia vivamente l'uso di questa impostazione.

Per installare un pacchetto con privilegi elevati (di sistema), impostare il valore AlwaysInstallElevated su "1" in entrambe le chiavi del registro di sistema seguenti:

**HKEY \_ Criteri \_ software utente correnti** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

**HKEY \_ Criteri software del \_ computer locale** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

Se il valore AlwaysInstallElevated non è impostato su "1" in entrambe le chiavi del registro di sistema precedenti, il programma di installazione utilizza privilegi elevati per installare le applicazioni gestite e utilizza il livello di privilegio dell'utente corrente per le applicazioni non gestite.

Poiché questo criterio consente agli utenti di installare applicazioni che richiedono l'accesso alle directory e alle chiavi del registro di sistema per le quali l'utente non dispone delle autorizzazioni per la visualizzazione o la modifica, è necessario valutare se fornisce agli utenti un livello di sicurezza appropriato. L'impostazione di questo criterio indica Windows Installer di utilizzare le autorizzazioni di sistema durante l'installazione dell'applicazione nel sistema. Se questo criterio non è impostato, le applicazioni non distribuite dall'amministratore vengono installate usando i privilegi dell'utente e solo le applicazioni gestite ottengono privilegi elevati.

Si noti che quando il criterio per computer per AlwaysInstallElevated è abilitato, qualsiasi utente può impostare l'impostazione per utente.

## <a name="remarks"></a>Commenti

Per informazioni sull'interazione di questi criteri con le origini di installazione, vedere [gestione delle origini di installazione](managing-installation-sources.md).

## <a name="data-type"></a>Tipo di dati

**REG \_ DWORD**

 

 



