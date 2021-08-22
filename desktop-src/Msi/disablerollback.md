---
description: Se questo criterio di sistema è impostato su 1, il programma di installazione non archivia i file di rollback durante l'installazione e disabilita il rollback dell'installazione.
ms.assetid: 01747de6-7478-4403-ba36-8ff1abc2b70f
title: DisableRollback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5da8380ce5dc7ea0b711d5766a554d6dce970bc81587a75164e61f3694c6a5ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947315"
---
# <a name="disablerollback"></a>DisableRollback

Se questo criterio [di sistema è](system-policy.md) impostato su 1, il programma di installazione non archivia i file di rollback durante l'installazione e disabilita il rollback dell'installazione. Per impostazione predefinita, il rollback è abilitato. È consigliabile che gli amministratori non usino questi criteri a meno che non siano assolutamente essenziali. Per altre informazioni, vedere [Rollback Installation](rollback-installation.md).

## <a name="registry-key"></a>Chiave del Registro di sistema

Per disabilitare il rollback per le installazioni per utente, **impostare DisableRollback** su 1 nella chiave del Registro di sistema seguente:

**HKEY \_ CURRENT \_ USER** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **Windows** \\ **Installer**

Per disabilitare il rollback per le installazioni per computer, **impostare DisableRollback** su 1 nella chiave del Registro di sistema seguente.

**HKEY \_ Criteri \_ software del** \\ **computer** \\ **locale Programma** di installazione di \\ **Microsoft** \\ **Windows** \\ 

## <a name="data-type"></a>Tipo di dati

**REG \_ DWORD**

 

 



