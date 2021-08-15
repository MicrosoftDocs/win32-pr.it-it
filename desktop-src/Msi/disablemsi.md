---
description: Se il valore di questo criterio di sistema per computer è impostato su \# &0034;2&0034; il programma di installazione è sempre disabilitato per tutte le \# applicazioni. Se il valore di questo criterio è impostato su \# &0034;1&0034;, il programma di installazione è disabilitato per le applicazioni non gestite, ma è ancora abilitato per le applicazioni \# gestite.
ms.assetid: 7f941559-54c3-4802-b827-5954bd4669f8
title: DisableMSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 846b8fb8c2c1127e59c82cce138a0956756d3447d6628cb61ef170a91e6290b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118378559"
---
# <a name="disablemsi"></a>DisableMSI

Se il valore di questo criterio di [sistema](system-policy.md) per computer è impostato su "2", il programma di installazione è sempre disabilitato per tutte le applicazioni. Se il valore di questo criterio è impostato su "1", il programma di installazione viene disabilitato per le applicazioni non gestite, ma è ancora abilitato per le applicazioni gestite.

Nella tabella seguente sono elencate le possibili configurazioni.



| DisableMSI | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Default*  | In Windows Server 2003, Windows Server 2003 R2, Windows Server 2008 e Windows Server 2008 R2, se il valore dei criteri è Null, assente o qualsiasi numero diverso da 1 o 2, il programma di installazione di Windows è abilitato per le applicazioni gestite. Le installazioni di applicazioni non gestite vengono bloccate.<br/> In Windows XP, Windows Vista e Windows 7, il Windows installer è abilitato per tutte le applicazioni. Tutte le operazioni di installazione sono consentite.<br/> |
| 0          | Windows Il programma di installazione è abilitato per tutte le applicazioni. Tutte le operazioni di installazione sono consentite.                                                                                                                                                                                                                                                                                                                                                      |
| 1          | Il Windows installer è disabilitato per le applicazioni non gestite, ma è ancora abilitato per le applicazioni gestite. Le installazioni per utente non elevate vengono bloccate. Sono consentite installazioni per utente con privilegi elevati e per computer.                                                                                                                                                                                                                        |
| 2          | Windows Il programma di installazione è sempre disabilitato per tutte le applicazioni. Non sono consentite installazioni, tra cui riparazioni, reinstalli o installazioni su richiesta.                                                                                                                                                                                                                                                                                               |



 

## <a name="registry-key"></a>Chiave del Registro di sistema

**HKEY \_ Criteri \_ software di LOCAL MACHINE** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo di dati

**REG \_ DWORD**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Non supportato in Windows Installer 2.0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




