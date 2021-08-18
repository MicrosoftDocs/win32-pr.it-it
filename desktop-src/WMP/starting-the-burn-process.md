---
title: Avvio del processo di masterizzazione
description: Avvio del processo di masterizzazione
ms.assetid: 91442bd2-1a68-465c-b865-63d309f33d55
keywords:
- Windows Media Player, CD
- Windows Media Player a oggetti, CD
- modello a oggetti, CD
- Windows Media Player ActiveX controllo, CD
- ActiveX controllo, CD
- Windows Media Player Controllo di ActiveX per dispositivi mobili, CD
- Windows Media Player Dispositivi mobili, CD-
- CD disasato, avvio del processo di masterizzazione
- CD di masterizzazione, avvio del processo di masterizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50f5620ba8fa6ab911cf0fd594fd27f139b5061d1383575f861dadfec45dabbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995081"
---
# <a name="starting-the-burn-process"></a>Avvio del processo di masterizzazione

Prima di iniziare il processo di riproduzione, è necessario assegnare una playlist per la riproduzione. Usare [IWMPCdrom Playlist::p ut \_ burnPlaylist](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_burnplaylist) per specificare una playlist per la riproduzione.


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



Per informazioni sull'uso delle playlist, vedere [IWMPPlaylist.](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist)

Per avviare l'operazione di esezione, [chiamare IWMPCdromComb::start Rieti](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-startburn).


```C++
// Start burning.
hr = m_spCdromBurn->startBurn();

```



È possibile arrestare l'operazione di [esercite chiamando IWMPCdromComb::stop 1.](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-stopburn)


```C++
// Stop burning.
hr = m_spCdromBurn->stopBurn();

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creare un cd**](burning-a-cd.md)
</dt> <dt>

[**Recupero dell'interfaccia di masterizzazione CD**](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[**Cancellazione di un CD risbilebile**](erasing-a-rewritable-cd.md)
</dt> <dt>

[**Recupero dello stato dell'unità e del disco**](retrieving-the-drive-and-disc-status.md)
</dt> <dt>

[**Recupero dello stato della masterizzazione**](retrieving-the-burn-status.md)
</dt> </dl>

 

 




