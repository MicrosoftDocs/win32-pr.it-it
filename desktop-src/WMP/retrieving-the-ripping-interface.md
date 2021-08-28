---
title: Recupero dell'interfaccia di copia da CD
description: Recupero dell'interfaccia di copia da CD
ms.assetid: 760610eb-e356-4b50-b865-53557ba9b815
keywords:
- Windows Media Player,ripping CD
- Windows Media Player a oggetti, ripping CD
- modello a oggetti, ripping CD
- Windows Media Player ActiveX controllo, ripping CD
- ActiveX, ripping CD
- Windows Media Player Controllo ActiveX per dispositivi mobili, ripping CD
- Windows Media Player Mobile, ripping CD
- Ripping cd, interfaccia IWMPCdromRip
- ripping di CD, interfaccia IWMPCdromRip
- Interfaccia IWMPCdromRip
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2179e4f38eee121d7b8fefc028adf232eb724264362396c8cacedfcc55b162d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002551"
---
# <a name="retrieving-the-ripping-interface"></a>Recupero dell'interfaccia di copia da CD

Per enumerare le unità CD nel computer dell'utente, usare **l'interfaccia IWMPCdromCollection.** Recuperare un puntatore a questa interfaccia chiamando [IWMPCore::get \_ cdromCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection).

Usando i [metodi get \_ count](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromcollection-get_count) e [item,](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromcollection-item) è possibile scorrere la raccolta per recuperare un'interfaccia [IWMPCdrom](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom) per ogni unità CD nel computer dell'utente.

**L'interfaccia IWMPCdrom** rappresenta una singola unità CD. Prima di iniziare a eseguire il ripping di un CD, è necessario chiamare **QueryInterface** tramite un puntatore **IWMPCdrom** per recuperare l'interfaccia [IWMPCdromRip.](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip)

L'esempio di codice seguente illustra come recuperare un'interfaccia per il ripping di un CD da un'unità specifica:


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

[**Ripping di un CD**](ripping-a-cd.md)
</dt> <dt>

[**Avvio del processo di rip**](starting-the-rip-process.md)
</dt> <dt>

[**Recupero dello stato di rip**](retrieving-the-rip-status.md)
</dt> <dt>

[**Selezione degli elementi per il ripping**](selecting-items-for-ripping.md)
</dt> <dt>

[**Interfaccia IWMPCdromCollection**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)
</dt> </dl>

 

 




