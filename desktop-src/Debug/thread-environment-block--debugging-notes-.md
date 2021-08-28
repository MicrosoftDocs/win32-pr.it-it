---
description: Blocco dell'ambiente thread (note sul debug)
ms.assetid: 5040CB82-D32F-4C44-8C03-30238D5B897A
title: Blocco dell'ambiente thread (note sul debug)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17f5c40b2a64eb868a7fd3ffb2052a3692db90f19d33357d4ef4f3113803bf52
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119655271"
---
# <a name="thread-environment-block-debugging-notes"></a>Blocco dell'ambiente thread (note sul debug)

Il blocco di ambiente thread [**(struttura TEB)**](/windows/win32/api/winternl/ns-winternl-teb)contiene informazioni di contesto per un thread.

Nelle versioni seguenti di Windows, l'offset dell'indirizzo TEB a 32 bit all'interno del TEB a 64 bit è 0. Può essere usato per accedere direttamente al TEB a 32 bit di un thread WOW64. Questa modifica potrebbe cambiare nelle versioni successive di Windows



|  Piattaforma     | Versione                |
|---------------|------------------------|
| Windows Vista | Windows Server 2008    |
| Windows 7     | Windows Server 2008 R2 |
| Windows 8     | Windows Server 2012    |
| Windows 8.1   | R2 per Windows Server 2012 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Strutture di debug](debugging-structures.md)
</dt> <dt>

[**CONTESTO \_ WOW64**](/windows/desktop/api/WinNT/ns-winnt-wow64_context)
</dt> </dl>

 

 
