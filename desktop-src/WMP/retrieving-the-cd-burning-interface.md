---
title: Recupero dell'interfaccia di masterizzazione CD
description: Recupero dell'interfaccia di masterizzazione CD
ms.assetid: d52f7b27-a327-4656-8dc2-0b075264d295
keywords:
- Windows Media Player, masterizzazione CD
- Modello a oggetti di Windows Media Player, masterizzazione CD
- modello a oggetti, masterizzazione CD
- Controllo ActiveX Windows Media Player, masterizzazione CD
- Controllo ActiveX, masterizzazione CD
- Controllo ActiveX Windows Media Player Mobile, masterizzazione CD
- Windows Media Player Mobile, masterizzazione CD
- Masterizzazione CD, recupero dell'interfaccia IWMPCdromCollection
- masterizzazione di CDs, recupero dell'interfaccia IWMPCdromCollection
- Interfaccia IWMPCdromCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b63763f9dd99bbaf88ae099edb53ba072cd1a25e
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104046425"
---
# <a name="retrieving-the-cd-burning-interface"></a>Recupero dell'interfaccia di masterizzazione CD

Per enumerare le unità CD nel computer dell'utente, usare l'interfaccia **IWMPCdromCollection** . Per recuperare un puntatore a questa interfaccia, chiamare [IWMPCore:: Get \_ cdromcollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection).

Usando i metodi **get \_ count** e **Item** , è possibile eseguire l'iterazione della raccolta per recuperare un puntatore di interfaccia [IWMPCdrom](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom) per ogni unità CD nel computer dell'utente.

L'interfaccia **IWMPCdrom** rappresenta una singola unità CD. Prima di iniziare a masterizzare un CD, è prima necessario chiamare **QueryInterface** tramite un puntatore **IWMPCdrom** per recuperare un puntatore all'interfaccia [IWMPCdromBurn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) .

Nell'esempio di codice seguente viene illustrato come recuperare un'interfaccia per la masterizzazione di un CD in un'unità specifica:


```C++
HRESULT CMainDlg::GetCdromDriveCount (long &lDriveCount)
{
    hr = m_spPlayer->get_cdromCollection(&m_spCdromCollection);

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
HRESULT CMainDlg::GetCdromBurnInterface (long lIndex)
{
    // Get the IWMPCdrom interface.
    m_spCdrom.Release();
    HRESULT hr = m_spCdromCollection->item(lIndex, &m_spCdrom);
    if (SUCCEEDED(hr))
    {
        // Get the IWMPCdromBurn interface.
        m_spCdromBurn.Release();
        hr = m_spCdrom->QueryInterface(&m_spCdromBurn);
    }

    return hr;
}

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Masterizzazione di un CD**](burning-a-cd.md)
</dt> <dt>

[**Avvio del processo di masterizzazione**](starting-the-burn-process.md)
</dt> <dt>

[**Cancellazione di un CD riscrivibile**](erasing-a-rewritable-cd.md)
</dt> <dt>

[**Recupero dello stato dell'unità e del disco**](retrieving-the-drive-and-disc-status.md)
</dt> <dt>

[**Recupero dello stato di masterizzazione**](retrieving-the-burn-status.md)
</dt> <dt>

[**Interfaccia IWMPCdromCollection**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)
</dt> </dl>

 

 




