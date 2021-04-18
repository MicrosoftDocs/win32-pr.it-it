---
title: Rilevamento di Windows Media Player da un'applicazione
description: Rilevamento di Windows Media Player da un'applicazione
ms.assetid: 3cf8a619-3b7e-45af-af6b-4711a45c7e07
keywords:
- Windows Media Player, rilevamento da applicazioni
- rilevamento Media Player Windows dalle applicazioni
- Registro di sistema, rilevamento Media Player Windows dalle applicazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03ae0c7d30b71749a22ecef10806817cd4182224
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298801"
---
# <a name="detecting-windows-media-player-from-an-application"></a>Rilevamento di Windows Media Player da un'applicazione

È possibile determinare la versione di Windows Media Player installata controllando la seguente chiave del registro di sistema:

**\_Componenti di \_ installazione \\ di \\ Microsoft \\ Active Setup Software per \\ computer locale HKEY**

Per Windows Media Player 6,4, vedere la chiave **{22d6f312-b0f6-11d0-94ab-0080c74c7e95}**.

Per Windows Media Player 7 o versione successiva, vedere la chiave **{6BF52A52-394A-11D3-B153-00C04F79FAA6}**.

In una di queste chiavi, se è stato **installato**<dl> <dt>

Tipo di dati
</dt> <dd>DWORD</dd> </dl> DWORD value is set to 0x1, you can safely use the **Version**<dl> <dt>

Tipo di dati
</dt> <dd>string</dd> </dl> string value as the version of Windows Media Player that is installed.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Ridistribuzione del software Windows Media Player**](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




