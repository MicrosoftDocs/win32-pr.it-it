---
description: Questo criterio di sistema per computer disattiva la creazione di checkpoint per Windows Installer.
ms.assetid: 706d6c85-3876-4205-b7da-b0fd709e65dd
title: LimitSystemRestoreCheckpointing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7606d266b4e9e42f6287669df9b3ab33a3ad9f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307249"
---
# <a name="limitsystemrestorecheckpointing"></a>LimitSystemRestoreCheckpointing

Questo [criterio di sistema](system-policy.md) per computer disattiva la creazione di checkpoint per Windows Installer.

Impostato su 0 o assente, il programma di installazione esegue normali checkpoint per l'installazione o la disinstallazione. Impostando su 1, il programma di installazione non crea alcun checkpoint.

Questo criterio ha effetto solo sui checkpoint impostati dal Windows Installer. Nei computer Windows XP, gli amministratori possono decidere di disabilitare il checkpoint dall'interno Windows Installer per migliorare le prestazioni. [**Ripristino configurazione di sistema**](../sr/system-restore-portal.md) crea anche ulteriori checkpoint. Per ulteriori informazioni, vedere [punti di ripristino del sistema e il Windows Installer](system-restore-points-and-the-windows-installer.md) e [impostazione di un punto di ripristino da un'azione personalizzata](setting-a-restore-point-from-a-custom-action.md).

## <a name="registry-key"></a>Chiave del Registro di sistema

Impostare il valore denominato LimitSystemRestoreCheckpointing nella seguente chiave del registro di sistema.

**HKEY \_ \_ criteri software del computer locale \\ \\ \\ Microsoft \\ Windows \\ Installer**

## <a name="data-type"></a>Tipo di dati

**REG \_ DWORD**

 

 
