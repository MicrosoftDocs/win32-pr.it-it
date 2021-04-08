---
description: Se il valore di questo criterio del sistema per computer è impostato su &\# 0034; 2&\# 0034; il programma di installazione è sempre disabilitato per tutte le applicazioni. Se il valore di questo criterio è impostato su &\# 0034; 1&\# 0034;, il programma di installazione è disabilitato per le applicazioni non gestite, ma è ancora abilitato per le applicazioni gestite.
ms.assetid: 7f941559-54c3-4802-b827-5954bd4669f8
title: DisableMSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbf8a784f5e8090bf6ba2007091c22cf4bc070c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050151"
---
# <a name="disablemsi"></a>DisableMSI

Se il valore di questo [criterio di sistema](system-policy.md) per computer è impostato su "2", il programma di installazione è sempre disabilitato per tutte le applicazioni. Se il valore di questo criterio è impostato su "1", il programma di installazione viene disabilitato per le applicazioni non gestite, ma è ancora abilitato per le applicazioni gestite.

Nella tabella seguente sono elencate le configurazioni possibili.



| DisableMSI | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Default*  | In Windows Server 2003, Windows Server 2003 R2, Windows Server 2008 e Windows Server 2008 R2, se il valore dei criteri è null, assente o un numero diverso da 1 o 2, il Windows Installer è abilitato per le applicazioni gestite. Le installazioni di applicazioni non gestite sono bloccate.<br/> In Windows XP, Windows Vista e Windows 7, il Windows Installer è abilitato per tutte le applicazioni. Sono consentite tutte le operazioni di installazione.<br/> |
| 0          | Windows Installer è abilitato per tutte le applicazioni. Sono consentite tutte le operazioni di installazione.                                                                                                                                                                                                                                                                                                                                                      |
| 1          | Il Windows Installer è disabilitato per le applicazioni non gestite, ma è ancora abilitato per le applicazioni gestite. Le installazioni per utente non elevate sono bloccate. Sono consentite installazioni con privilegi elevati e computer per utente.                                                                                                                                                                                                                        |
| 2          | Windows Installer è sempre disabilitato per tutte le applicazioni. Non sono consentite installazioni, tra cui riparazioni, reinstallazioni o installazioni su richiesta.                                                                                                                                                                                                                                                                                               |



 

## <a name="registry-key"></a>Chiave del Registro di sistema

**HKEY \_ Criteri software del \_ computer locale** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo di dati

**REG \_ DWORD**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Non supportato in Windows Installer 2,0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




