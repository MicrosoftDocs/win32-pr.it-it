---
title: Avvio del processo di masterizzazione
description: Avvio del processo di masterizzazione
ms.assetid: 91442bd2-1a68-465c-b865-63d309f33d55
keywords:
- Windows Media Player, masterizzazione CD
- Modello a oggetti di Windows Media Player, masterizzazione CD
- modello a oggetti, masterizzazione CD
- Controllo ActiveX Windows Media Player, masterizzazione CD
- Controllo ActiveX, masterizzazione CD
- Controllo ActiveX Windows Media Player Mobile, masterizzazione CD
- Windows Media Player Mobile, masterizzazione CD
- Masterizzazione CD, avvio del processo di masterizzazione
- masterizzazione di CDs, avvio del processo di masterizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4a35f473eebe35bffd48ac802dcfe79082689de
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103956202"
---
# <a name="starting-the-burn-process"></a>Avvio del processo di masterizzazione

Prima che la masterizzazione possa iniziare, è necessario assegnare una playlist da masterizzare. Usare [IWMPCdromBurn::p UT \_ burnPlaylist](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_burnplaylist) per specificare una playlist per la masterizzazione.


```C++
HRESULT CMainDlg::PutPlaylist (void)
{
    // Specify the burn playlist.   
    HRESULT hr = m_spCdromBurn->put_burnPlaylist(m_spPlaylist);

    // Update the status information.
    if (SUCCEEDED(hr))
    {
        hr = m_spCdromBurn->refreshStatus();
    }

    return hr;
}

```



Per informazioni sull'uso delle playlist, vedere [IWMPPlaylist](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist).

Per avviare l'operazione di masterizzazione, chiamare [IWMPCdromBurn:: startBurn](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-startburn).


```C++
// Start burning.
hr = m_spCdromBurn->startBurn();

```



È possibile arrestare l'operazione di masterizzazione chiamando [IWMPCdromBurn:: stopBurn](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-stopburn).


```C++
// Stop burning.
hr = m_spCdromBurn->stopBurn();

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Masterizzazione di un CD**](burning-a-cd.md)
</dt> <dt>

[**Recupero dell'interfaccia di masterizzazione CD**](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[**Cancellazione di un CD riscrivibile**](erasing-a-rewritable-cd.md)
</dt> <dt>

[**Recupero dello stato dell'unità e del disco**](retrieving-the-drive-and-disc-status.md)
</dt> <dt>

[**Recupero dello stato di masterizzazione**](retrieving-the-burn-status.md)
</dt> </dl>

 

 




