---
description: A partire Windows Server 2008 e Windows Vista, questo criterio non ha più alcun effetto.
ms.assetid: 27a4192e-0574-414d-993e-6c715577f0ba
title: EnableAdminTSRemote
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45a644e6f0cb9200fd8a130a2cdb293e7658e3354b817f7378571fae0ab3b4f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118637105"
---
# <a name="enableadmintsremote"></a>EnableAdminTSRemote

A partire Windows Server 2008 e Windows Vista, questo criterio non ha più alcun effetto. Un amministratore può eseguire un'installazione dalla sessione della console di un server terminal. Un amministratore può anche eseguire un'installazione da una sessione client del server terminal.

Per altre informazioni, vedere [Servizi terminal](/windows/desktop/TermServ/terminal-services-portal) in Microsoft Windows Software Development Kit (SDK).

**Sistemi operativi precedenti a Windows Server 2008 e Windows Vista: **

L'impostazione di questo criterio [di sistema](system-policy.md) per computer consente agli amministratori di eseguire installazioni da una sessione client del server terminal. Se questo criterio non è impostato, gli amministratori possono eseguire installazioni solo dalla sessione della console. Gli utenti non amministratori non possono mai eseguire installazioni da una sessione client. Il valore predefinito per questo criterio consente solo agli amministratori di eseguire installazioni dalla sessione della console. Gli amministratori possono sempre [eseguire installazioni amministrative](administrative-installation.md) da una sessione client del server terminal o dalla sessione della console, indipendentemente dall'impostazione di questo criterio.

## <a name="registry-key"></a>Chiave del Registro di sistema

**HKEY \_ Criteri \_ software del** \\ **computer** \\ **locale Programma** di installazione \\  \\ **Windows** \\ **Microsoft**

## <a name="data-type"></a>Tipo di dati

**REG \_ DWORD**

## <a name="remarks"></a>Commenti

Per altre informazioni, vedere anche Using [Windows Installer with a Terminal Server](using-windows-installer-with-a-terminal-server.md).

 

 
