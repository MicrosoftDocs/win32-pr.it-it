---
title: Ridimensionamento della finestra di dialogo acquisizione licenza
description: Ridimensionamento della finestra di dialogo acquisizione licenza
ms.assetid: e091d981-1574-4ffc-bdc4-b92f74396cb7
keywords:
- Finestra di dialogo Media Player di Windows, ridimensionamento dell'acquisizione delle licenze
- Windows Media Player, finestra di dialogo acquisizione licenza
- Media Player di Windows, attributo DRM_LicenseAcqURL
- finestra di dialogo di ridimensionamento dell'acquisizione delle licenze
- Finestra di dialogo acquisizione licenza
- DRM_LicenseAcqURL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 440683ce65417653251bbed58d59c4d9a34dbc57
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396383"
---
# <a name="resizing-the-license-acquisition-dialog-box"></a>Ridimensionamento della finestra di dialogo acquisizione licenza

È possibile aggiungere i parametri della stringa di query all'URL specificato per l'attributo **\_ LicenseAcqURL di DRM** per specificare una dimensione per la finestra di dialogo di acquisizione della licenza di Windows Media Player 10 o versione successiva. Nella tabella seguente sono elencati i parametri.



| Parametro | Descrizione                                        |
|-----------|----------------------------------------------------|
| *DlgX*    | Specifica la larghezza, in pixel, della finestra di dialogo.  |
| *DlgY*    | Specifica l'altezza, in pixel, della finestra di dialogo. |



 

Ad esempio, l'URL di acquisizione della licenza seguente determina l'apertura della finestra di dialogo acquisizione licenza con una dimensione di 800 per 600 pixel:


```C++
https://www.proseware.com/license/lic_acq.htm?DlgX=800&DlgY=600

```



Le dimensioni massime per la finestra di dialogo non supereranno mai le dimensioni correnti dello schermo meno 20 pixel. La dimensione minima è 333 x 210 pixel (dimensione predefinita).

Questa funzionalità richiede Windows Media Player 10 o versione successiva.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Windows Media Player**](windows-media-player.md)
</dt> </dl>

 

 




