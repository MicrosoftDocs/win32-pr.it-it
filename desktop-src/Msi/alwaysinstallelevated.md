---
description: Installare un pacchetto Windows Installer con privilegi elevati (di sistema).
ms.assetid: 0bbec06a-0a2b-430a-a361-317a319da615
title: AlwaysInstallElevated
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc015dad8096db16d8b70238a5fd7e07544b83f9a9e3d1a5045be9d12bbb30cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650241"
---
# <a name="alwaysinstallelevated"></a>AlwaysInstallElevated

È possibile usare il criterio AlwaysInstallElevated per installare un pacchetto Windows Installer con privilegi elevati (di sistema).

**Avviso: **

Questa opzione equivale a concedere diritti amministrativi completi, che possono costituire un rischio elevato per la sicurezza. Microsoft sconsiglia fortemente l'uso di questa impostazione.

Per installare un pacchetto con privilegi di sistema elevati, impostare il valore AlwaysInstallElevated su "1" in entrambe le chiavi del Registro di sistema seguenti:

**HKEY \_ CURRENT \_ USER** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **Windows** \\ **Installer**

**HKEY \_ Criteri \_ software del** \\ **computer** \\ **locale Programma** di installazione di \\ **Microsoft** \\ **Windows** \\ 

Se il valore AlwaysInstallElevated non è impostato su "1" in entrambe le chiavi del Registro di sistema precedenti, il programma di installazione usa privilegi elevati per installare le applicazioni gestite e usa il livello di privilegio dell'utente corrente per le applicazioni non gestite.

Poiché questo criterio consente agli utenti di installare applicazioni che richiedono l'accesso a directory e chiavi del Registro di sistema per le quali l'utente potrebbe non avere l'autorizzazione per la visualizzazione o la modifica, è necessario valutare se offre agli utenti un livello di sicurezza appropriato. L'impostazione di questo criterio Windows programma di installazione di per usare le autorizzazioni di sistema quando installa l'applicazione nel sistema. Se questo criterio non è impostato, le applicazioni non distribuite dall'amministratore vengono installate usando i privilegi dell'utente e solo le applicazioni gestite ottengono privilegi elevati.

Si noti che una volta abilitati i criteri per computer per AlwaysInstallElevated, qualsiasi utente può impostare l'impostazione per utente.

## <a name="remarks"></a>Commenti

Per informazioni sull'interazione di questo criterio con le origini di installazione, vedere [Gestione delle origini di installazione.](managing-installation-sources.md)

## <a name="data-type"></a>Tipo di dati

**REG \_ DWORD**

 

 



