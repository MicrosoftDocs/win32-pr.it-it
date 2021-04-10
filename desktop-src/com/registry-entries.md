---
title: Voci del registro di sistema (COM)
ms.assetid: f4f8875c-6416-4919-b49b-bcd675efcbd2
description: 'Altre informazioni su: voci del registro di sistema (COM)'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 368e9eb5e4c2174c5b4b90df6586b58135085c5b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127570"
---
# <a name="registry-entries-com"></a>Voci del registro di sistema (COM)

I valori del registro di sistema nelle chiavi del registro di sistema seguenti controllano gli aspetti della funzionalità di COM:

-   [**\_ \_ Classi software del computer locale \\ HKEY \\**](hkey-local-machine-software-classes.md)
-   [**\_Software per \_ computer locale HKEY \\ \\ Microsoft \\ OLE**](hkey-local-machine-software-microsoft-ole.md)
-   [**HKEY \_ \_ computer locale \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion**](hkey-local-machine-software-microsoft-windows-nt-currentversion.md)

A partire da Windows Server 2003, COM usa solo il token di processo corrente per decidere quale hive del registro di sistema accedere, non il token del thread. Se COM non è in grado di accedere all'hive del registro di sistema del profilo utente, accederà a **HKEY \_ Local \_ Machine \\ System** hive.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registro](/windows/desktop/SysInfo/registry)
</dt> </dl>

 

 
