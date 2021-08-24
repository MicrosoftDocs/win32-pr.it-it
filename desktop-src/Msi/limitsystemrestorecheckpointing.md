---
description: Questo criterio di sistema per computer disattiva la creazione di checkpoint Windows programma di installazione.
ms.assetid: 706d6c85-3876-4205-b7da-b0fd709e65dd
title: LimitSystemRestoreCheckpointing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cbea03dcab5db690f6fc06725dbb38a376310e967b9e92a9fcb0c59daab0180
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763511"
---
# <a name="limitsystemrestorecheckpointing"></a>LimitSystemRestoreCheckpointing

Questo criterio di sistema [per computer](system-policy.md) disattiva la creazione di checkpoint Windows programma di installazione.

Impostato su 0 o assente, il programma di installazione esegue normali checkpoint per l'installazione o la disinstallazione. Se impostato su 1, il programma di installazione non crea checkpoint.

Questo criterio influisce solo sui checkpoint impostati da Windows programma di installazione. Nei Windows XP, gli amministratori possono decidere di disabilitare l'impostazione dei checkpoint dall'interno Windows programma di installazione per migliorare le prestazioni. [**Ripristino configurazione di sistema**](../sr/system-restore-portal.md) crea anche checkpoint aggiuntivi. Per altre informazioni, vedere Ripristino configurazione di sistema e il programma [di installazione Windows](system-restore-points-and-the-windows-installer.md) e Impostazione di un punto di ripristino da [un'azione personalizzata.](setting-a-restore-point-from-a-custom-action.md)

## <a name="registry-key"></a>Chiave del Registro di sistema

Impostare il valore denominato LimitSystemRestoreCheckpointing nella chiave del Registro di sistema seguente.

**HKEY \_ LOCAL MACHINE Software Policies Microsoft Windows \_ \\ \\ \\ \\ \\ Installer**

## <a name="data-type"></a>Tipo di dati

**REG \_ DWORD**

 

 
