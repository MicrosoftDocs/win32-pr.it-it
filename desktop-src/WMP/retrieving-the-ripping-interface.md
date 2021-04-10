---
title: Recupero dell'interfaccia di copia da CD
description: Recupero dell'interfaccia di copia da CD
ms.assetid: 760610eb-e356-4b50-b865-53557ba9b815
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
ms.openlocfilehash: 903fa285404700e35363a94239c79706e7af0e34
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "103858077"
---
# <a name="retrieving-the-ripping-interface"></a>Recupero dell'interfaccia di copia da CD

Per enumerare le unità CD nel computer dell'utente, usare l'interfaccia **IWMPCdromCollection** . Recuperare un puntatore a questa interfaccia chiamando [IWMPCore:: Get \_ cdromcollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection).

Usando i metodi [get \_ count](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromcollection-get_count) e [Item](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromcollection-item) , è possibile eseguire l'iterazione della raccolta per recuperare un'interfaccia [IWMPCdrom](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom) per ogni unità CD nel computer dell'utente.

L'interfaccia **IWMPCdrom** rappresenta una singola unità CD. Prima di iniziare a rippare un CD, è prima necessario chiamare **QueryInterface** tramite un puntatore **IWMPCdrom** per recuperare l'interfaccia [IWMPCdromRip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip) .

Nell'esempio di codice seguente viene illustrato come recuperare un'interfaccia per estrarre un CD da un'unità specifica:


```C++
HRESULT CMainDlg::GetCdromDriveCount (long &lDriveCount)
{
    HRESULT hr = m_spPlayer->get_cdromCollection(&m_spCdromCollection);

    // Get the number of CDROM drives.
    if (SUCCEEDED(hr))
    {
        hr = m_spCdromCollection->get_count(&lDriveCount);
    }

    return hr;
}

// lIndex refers to the index of the current drive,
// which must be less than the value retrieved by
// GetCdromDriveCount above.
HRESULT CMainDlg::GetCdromRipInterface (long lIndex)
{
    // Get the IWMPCdrom interface.
    m_spCdrom.Release();
    HRESULT hr = m_spCdromCollection->item(lIndex, &m_spCdrom);
    if (SUCCEEDED(hr))
    {
        // Get the IWMPCdromRip interface.
        m_spCdromRip.Release();
        hr = m_spCdrom->QueryInterface(&m_spCdromRip);
    }

    return hr;
}

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Copia di un CD**](ripping-a-cd.md)
</dt> <dt>

[**Avvio del processo RIP**](starting-the-rip-process.md)
</dt> <dt>

[**Recupero dello stato di RIP**](retrieving-the-rip-status.md)
</dt> <dt>

[**Selezione di elementi per l'estrazione**](selecting-items-for-ripping.md)
</dt> <dt>

[**Interfaccia IWMPCdromCollection**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)
</dt> </dl>

 

 




