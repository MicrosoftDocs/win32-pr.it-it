---
title: Recupero dell'interfaccia di masterizzazione CD
description: Recupero dell'interfaccia di masterizzazione CD
ms.assetid: d52f7b27-a327-4656-8dc2-0b075264d295
keywords:
- Windows Media Player,CD
- Windows Media Player a oggetti, CD
- modello a oggetti, CD
- Windows Media Player ActiveX controllo, CD
- ActiveX controllo, CD
- Windows Media Player Mobile ActiveX control,CD
- Windows Media Player Dispositivi mobili, CD-
- CD e recupero dell'interfaccia IWMPCdromCollection
- CD di windows, recupero dell'interfaccia IWMPCdromCollection
- Interfaccia IWMPCdromCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84013d5df4244fc30c9cb52e3447d15f60e559befe1223f0964934dd8ca1e1cf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123201"
---
# <a name="retrieving-the-cd-burning-interface"></a>Recupero dell'interfaccia di masterizzazione CD

Per enumerare le unità CD nel computer dell'utente, usare **l'interfaccia IWMPCdromCollection.** Per recuperare un puntatore a questa interfaccia, chiamare [IWMPCore::get \_ cdromCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection).

Usando i **metodi get \_ count** e **item,** è possibile eseguire l'iterazione della raccolta per recuperare un puntatore all'interfaccia [IWMPCdrom](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom) per ogni unità CD nel computer dell'utente.

**L'interfaccia IWMPCdrom** rappresenta una singola unità CD. Prima di iniziare a creare un CD, è necessario chiamare **QueryInterface** tramite un puntatore **IWMPCdrom** per recuperare un puntatore all'interfaccia [IWMPCdromInterface.](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn)

L'esempio di codice seguente illustra come recuperare un'interfaccia per copiare un CD in un'unità specifica:


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

[**Creare un cd**](burning-a-cd.md)
</dt> <dt>

[**Avvio del processo di masterizzazione**](starting-the-burn-process.md)
</dt> <dt>

[**Cancellazione di un CD risbilebile**](erasing-a-rewritable-cd.md)
</dt> <dt>

[**Recupero dello stato dell'unità e del disco**](retrieving-the-drive-and-disc-status.md)
</dt> <dt>

[**Recupero dello stato della masterizzazione**](retrieving-the-burn-status.md)
</dt> <dt>

[**Interfaccia IWMPCdromCollection**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)
</dt> </dl>

 

 




