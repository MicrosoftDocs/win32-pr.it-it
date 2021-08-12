---
title: Rilevamento di Windows Media Player da un'applicazione
description: Rilevamento di Windows Media Player da un'applicazione
ms.assetid: 3cf8a619-3b7e-45af-af6b-4711a45c7e07
keywords:
- Windows Media Player,rilevamento dalle applicazioni
- rilevamento di Windows Media Player dalle applicazioni
- Registro di sistema, rilevamento Windows Media Player dalle applicazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5267dc6c3202d9ecf894377899dfb34cf02ad42dfee05f8d42896c39ae48fc24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118579487"
---
# <a name="detecting-windows-media-player-from-an-application"></a>Rilevamento di Windows Media Player da un'applicazione

È possibile determinare la versione di Windows Media Player installata controllando la chiave del Registro di sistema seguente:

**HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Active Setup \\ Installed Components**

Per Windows Media Player 6.4, esaminare la chiave **{22d6f312-b0f6-11d0-94ab-0080c74c7e95}**.

Per Windows Media Player 7 o versione successiva, esaminare la chiave **{6BF52A52-394A-11d3-B153-00C04F79FAA6}**.

In una di queste chiavi, se **isInstalled**<dl> <dt>

Tipo di dati
</dt> <dd>DWORD</dd> </dl> DWORD value is set to 0x1, you can safely use the **Version**<dl> <dt>

Tipo di dati
</dt> <dd>string</dd> </dl> string value as the version of Windows Media Player that is installed.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Ridistribuzione Windows Media Player Software**](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




