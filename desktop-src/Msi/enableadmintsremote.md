---
description: A partire da Windows Server 2008 e Windows Vista, questo criterio non ha più alcun effetto.
ms.assetid: 27a4192e-0574-414d-993e-6c715577f0ba
title: EnableAdminTSRemote
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 383339ab5c2a592f3d6ab2cd81b4d6a446780411
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226622"
---
# <a name="enableadmintsremote"></a>EnableAdminTSRemote

A partire da Windows Server 2008 e Windows Vista, questo criterio non ha più alcun effetto. Un amministratore può eseguire un'installazione dalla sessione della console di un server terminal. Un amministratore può inoltre eseguire un'installazione da una sessione client di Terminal Server.

Per ulteriori informazioni, vedere [Servizi terminal](/windows/desktop/TermServ/terminal-services-portal) in Microsoft Windows Software Development Kit (SDK).

* * Sistemi operativi precedenti a Windows Server 2008 e Windows Vista: * *

L'impostazione di questo [criterio di sistema](system-policy.md) per computer consente agli amministratori di eseguire installazioni da una sessione client di Terminal Server. Se questo criterio non è impostato, gli amministratori possono eseguire le installazioni solo dalla sessione della console. Gli utenti non amministratori non possono mai eseguire installazioni da una sessione client. Il valore predefinito per questo criterio consente solo agli amministratori di eseguire installazioni dalla sessione della console. Gli amministratori possono sempre eseguire [installazioni amministrative](administrative-installation.md) da una sessione client di Terminal Server o dalla sessione della console, indipendentemente dal fatto che questi criteri siano impostati.

## <a name="registry-key"></a>Chiave del Registro di sistema

**HKEY \_ Criteri software del \_ computer locale** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo di dati

**REG \_ DWORD**

## <a name="remarks"></a>Commenti

Per ulteriori informazioni, vedere anche [utilizzo di Windows Installer con una Terminal Server](using-windows-installer-with-a-terminal-server.md).

 

 
