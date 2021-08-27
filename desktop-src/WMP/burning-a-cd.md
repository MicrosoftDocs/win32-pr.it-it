---
title: Creare un cd
description: Creare un cd
ms.assetid: df55479e-d8a7-443d-bf2c-c988bfd0b1be
keywords:
- Windows Media Player, CD
- Windows Media Player a oggetti, CD
- modello a oggetti, CD
- Windows Media Player ActiveX controllo, CD
- ActiveX controllo, CD
- Windows Media Player Mobile ActiveX control,CD
- Windows Media Player Dispositivi mobili, CD-
- CD Evaso, informazioni
- CD divasi, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82c7cfee7468b2cd376b7b25d4cff4a04e0d057dcc7a792ac7471843de2b74a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118840770"
---
# <a name="burning-a-cd"></a>Creare un cd

Questa sezione descrive come usare [l'interfaccia IWMPCdromLim](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) per masterizzare musica in un CD. **L'interfaccia IWMPCdrom Playlist** fornisce funzionalità per la riproduzione di playlist ai CD come tracce di dati o audio, nonché per la cancellazione di CD-RW.

Utilizzo del codice

Gli esempi di codice in questa sezione usano Active Template Library (ATL), ad esempio **CComPtr.**

Intestazioni incluse

Per usare il codice in questa sezione, includere le intestazioni seguenti:


```C++
#include <atlbase.h>
#include <atlcom.h>
#include <atlwin.h>
#include <commctrl.h>
#include "wmp.h"
#include "wmpids.h"

```



Puntatori a interfaccia

Le interfacce per Windows Media Player sono archiviate nelle variabili membro seguenti:


```C++
// Player interface.
CComPtr<IWMPPlayer>             m_spPlayer;

// CDROM interfaces.
CComPtr<IWMPCdromCollection>    m_spCdromCollection;
CComPtr<IWMPCdrom>              m_spCdrom;
CComPtr<IWMPCdromBurn>          m_spCdromBurn;
CComPtr<IWMPPlaylist>           m_spPlaylist;

```



Gli argomenti seguenti descrivono come usare l'API CD.

-   [Recupero dell'interfaccia di masterizzazione CD](retrieving-the-cd-burning-interface.md)
-   [Avvio del processo di masterizzazione](starting-the-burn-process.md)
-   [Cancellazione di un CD risbilebile](erasing-a-rewritable-cd.md)
-   [Recupero dello stato dell'unità e del disco](retrieving-the-drive-and-disc-status.md)
-   [Recupero dello stato della masterizzazione](retrieving-the-burn-status.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida al controllo del lettore**](player-control-guide.md)
</dt> </dl>

 

 




