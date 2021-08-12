---
title: Ripping tramite l'interfaccia IWMPCdromRip
description: Ripping tramite l'interfaccia IWMPCdromRip
ms.assetid: 7622072e-82e1-4e31-ad80-ddc3473b5841
keywords:
- Windows Media Player,ripping CD
- Windows Media Player a oggetti, ripping CD
- modello a oggetti, ripping CD
- Windows Media Player ActiveX, ripping CD
- ActiveX controllo, ripping CD
- Windows Media Player Controllo ActiveX per dispositivi mobili, ripping CD
- Windows Media Player Mobile, ripping CD
- Ripping cd, interfaccia IWMPCdromRip
- ripping di CD, interfaccia IWMPCdromRip
- Interfaccia IWMPCdromRip
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50651629f5a11f13bb27a11927c1f08c33de7162130fd7f10f33fe4c74386692
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118569797"
---
# <a name="ripping-by-using-the-iwmpcdromrip-interface"></a>Ripping tramite l'interfaccia IWMPCdromRip

Questa sezione descrive come usare [l'interfaccia IWMPCdromRip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip) per copiare musica da un CD.

Il ripping di un CD tramite **l'interfaccia IWMPCdromRip** ha lo stesso effetto di ripping di musica usando l'Windows Media Player utente. Il contenuto decompresso viene aggiunto automaticamente alla libreria in base alle preferenze dell'utente. Per altre informazioni sullo ripping di CD, vedere "Ripping di musica da CD" nella Guida di Windows Media Player.

Gli esempi di codice in questa sezione usano Active Template Library (ATL), ad esempio **CComPtr**.

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
-   [Avvio del processo di rip](starting-the-rip-process.md)
-   [Recupero dello stato di rip](retrieving-the-rip-status.md)
-   [Selezione degli elementi per il ripping](selecting-items-for-ripping.md)

 

 




