---
title: Avvio del processo RIP
description: Avvio del processo RIP
ms.assetid: 82ffc114-ddad-41be-af80-6c1bd29cb0d4
keywords:
- Windows Media Player, copia di CD
- Modello a oggetti di Windows Media Player, copia di CD
- modello a oggetti, copia di CD
- Controllo ActiveX di Windows Media Player, copia di CD
- Controllo ActiveX, copia di CD
- Controllo ActiveX Windows Media Player Mobile, copia di CD
- Windows Media Player Mobile, copia di CD
- Ripping del CD, avvio del processo RIP
- copia di CDs, avvio del processo RIP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2107b053abf8747d7add8fcedc26a2386ae5fd84
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299393"
---
# <a name="starting-the-rip-process"></a>Avvio del processo RIP

Dopo aver recuperato l'interfaccia di strappo come illustrato nella sezione precedente, avviare il processo di ripping chiamando [IWMPCdromRip:: startRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-startrip).


```C++
// Start ripping.
HRESULT hr = m_spCdromRip->startRip();

```



È possibile arrestare l'operazione di strappo chiamando [IWMPCdromRip:: stopRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-stoprip).


```C++
// Stop ripping.
HRESULT hr = m_spCdromRip->stopRip();

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Copia di un CD**](ripping-a-cd.md)
</dt> <dt>

[**Recupero dell'interfaccia di copia da CD**](retrieving-the-ripping-interface.md)
</dt> <dt>

[**Recupero dello stato di RIP**](retrieving-the-rip-status.md)
</dt> <dt>

[**Selezione di elementi per l'estrazione**](selecting-items-for-ripping.md)
</dt> </dl>

 

 




