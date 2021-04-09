---
description: Se questo criterio di sistema è impostato su 1, il programma di installazione non archivia i file di rollback durante l'installazione e Disabilita il rollback dell'installazione.
ms.assetid: 01747de6-7478-4403-ba36-8ff1abc2b70f
title: DisableRollback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7f0ce15e618880f021e04adf7d2146a97f6ed65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966833"
---
# <a name="disablerollback"></a>DisableRollback

Se questo [criterio di sistema](system-policy.md) è impostato su 1, il programma di installazione non archivia i file di rollback durante l'installazione e Disabilita il rollback dell'installazione. Per impostazione predefinita, il rollback è abilitato. Si consiglia agli amministratori di non utilizzare questo criterio a meno che non sia assolutamente essenziale. Per ulteriori informazioni, vedere [rollback Installation](rollback-installation.md).

## <a name="registry-key"></a>Chiave del Registro di sistema

Per disabilitare il rollback per le installazioni per utente, impostare **DisableRollback** su 1 nella chiave del registro di sistema seguente:

**HKEY \_ Criteri \_ software utente correnti** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

Per disabilitare il rollback per le installazioni per computer, impostare **DisableRollback** su 1 nella seguente chiave del registro di sistema.

**HKEY \_ Criteri software del \_ computer locale** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo di dati

**REG \_ DWORD**

 

 



