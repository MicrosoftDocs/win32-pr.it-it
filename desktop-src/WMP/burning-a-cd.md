---
title: Masterizzazione di un CD
description: Masterizzazione di un CD
ms.assetid: df55479e-d8a7-443d-bf2c-c988bfd0b1be
keywords:
- Windows Media Player, masterizzazione CD
- Modello a oggetti di Windows Media Player, masterizzazione CD
- modello a oggetti, masterizzazione CD
- Controllo ActiveX Windows Media Player, masterizzazione CD
- Controllo ActiveX, masterizzazione CD
- Controllo ActiveX Windows Media Player Mobile, masterizzazione CD
- Windows Media Player Mobile, masterizzazione CD
- Masterizzazione CD, informazioni
- masterizzazione di CDs, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 007b7808ff375ab0673592d0d016f8e713321d1a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104117383"
---
# <a name="burning-a-cd"></a>Masterizzazione di un CD

Questa sezione descrive come usare l'interfaccia [IWMPCdromBurn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) per masterizzare musica in un CD. L'interfaccia **IWMPCdromBurn** fornisce funzionalità per la masterizzazione di playlist in CDS come dati o tracce audio, nonché per cancellare CD-RW.

Utilizzo del codice

Gli esempi di codice in questa sezione usano le classi Active Template Library (ATL), ad esempio **CComPtr**.

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



Gli argomenti seguenti descrivono come usare l'API di masterizzazione CD.

-   [Recupero dell'interfaccia di masterizzazione CD](retrieving-the-cd-burning-interface.md)
-   [Avvio del processo di masterizzazione](starting-the-burn-process.md)
-   [Cancellazione di un CD riscrivibile](erasing-a-rewritable-cd.md)
-   [Recupero dello stato dell'unità e del disco](retrieving-the-drive-and-disc-status.md)
-   [Recupero dello stato di masterizzazione](retrieving-the-burn-status.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida al controllo del lettore**](player-control-guide.md)
</dt> </dl>

 

 




