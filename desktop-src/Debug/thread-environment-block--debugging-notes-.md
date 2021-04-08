---
description: Blocco ambiente thread (note di debug)
ms.assetid: 5040CB82-D32F-4C44-8C03-30238D5B897A
title: Blocco ambiente thread (note di debug)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d66b04b522bed8bdf7f5a5571c300019e4537b5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877786"
---
# <a name="thread-environment-block-debugging-notes"></a>Blocco ambiente thread (note di debug)

Il blocco dell'ambiente del thread ([**struttura TEB**](/windows/win32/api/winternl/ns-winternl-teb)) include informazioni di contesto per un thread.

Nelle versioni seguenti di Windows, l'offset dell'indirizzo TEB a 32 bit entro il TEB a 64 bit è 0. Può essere usato per accedere direttamente al TEB a 32 bit di un thread WOW64. Questo potrebbe cambiare nelle versioni successive di Windows



|               |                        |
|---------------|------------------------|
| Windows Vista | Windows Server 2008    |
| Windows 7     | Windows Server 2008 R2 |
| Windows 8     | Windows Server 2012    |
| Windows 8.1   | Windows Server 2012 R2 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Strutture di debug](debugging-structures.md)
</dt> <dt>

[**\_Contesto WOW64**](/windows/desktop/api/WinNT/ns-winnt-wow64_context)
</dt> </dl>

 

 
