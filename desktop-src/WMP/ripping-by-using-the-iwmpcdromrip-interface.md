---
title: Ripping mediante l'interfaccia IWMPCdromRip
description: Ripping mediante l'interfaccia IWMPCdromRip
ms.assetid: 7622072e-82e1-4e31-ad80-ddc3473b5841
keywords:
- Windows Media Player, copia di CD
- Modello a oggetti di Windows Media Player, copia di CD
- modello a oggetti, copia di CD
- Controllo ActiveX di Windows Media Player, copia di CD
- Controllo ActiveX, copia di CD
- Controllo ActiveX Windows Media Player Mobile, copia di CD
- Windows Media Player Mobile, copia di CD
- Ripping del CD, interfaccia IWMPCdromRip
- ripping di CDs, interfaccia IWMPCdromRip
- Interfaccia IWMPCdromRip
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fcf2e959d10385365075bb20e1c04c2d796ad2e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103858022"
---
# <a name="ripping-by-using-the-iwmpcdromrip-interface"></a>Ripping mediante l'interfaccia IWMPCdromRip

Questa sezione descrive come usare l'interfaccia [IWMPCdromRip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip) per rippare musica da un CD.

La copia di un CD usando l'interfaccia **IWMPCdromRip** ha lo stesso effetto del ritaglio di musica usando l'interfaccia utente di Windows Media Player. Il contenuto Ripped viene aggiunto automaticamente alla libreria in base alle preferenze dell'utente. Per ulteriori informazioni su come rippare i CD, vedere l'argomento relativo all'estrazione di musica da CDs nella Guida di Windows Media Player.

Gli esempi di codice in questa sezione usano le classi Active Template Library (ATL), ad esempio **CComPtr**.

## <a name="included-headers"></a>Intestazioni incluse

Per usare il codice in questa sezione, includere le intestazioni seguenti:


```C++
#include <atlbase.h>
#include <atlcom.h>
#include <atlwin.h>
#include <commctrl.h>
#include "wmp.h"
#include "wmpids.h"

```



## <a name="interface-pointers"></a>Puntatori a interfaccia

Le interfacce per Windows Media Player sono archiviate nelle variabili membro seguenti.


```C++
// Player interface.
CComPtr<IWMPPlayer>             m_spPlayer;

// CDROM interfaces.
CComPtr<IWMPCdromCollection>    m_spCdromCollection;
CComPtr<IWMPCdrom>              m_spCdrom;
CComPtr<IWMPCdromRip>           m_spCdromRip;
CComPtr<IWMPPlaylist>           m_spPlaylist;

```



Le sezioni seguenti descrivono come usare l'interfaccia IWMPCdromRip

-   [Recupero dell'interfaccia di copia da CD](retrieving-the-ripping-interface.md)
-   [Avvio del processo RIP](starting-the-rip-process.md)
-   [Recupero dello stato di RIP](retrieving-the-rip-status.md)
-   [Selezione di elementi per l'estrazione](selecting-items-for-ripping.md)

 

 




