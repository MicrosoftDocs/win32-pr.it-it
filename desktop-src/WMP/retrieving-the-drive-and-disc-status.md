---
title: Recupero dello stato dell'unità e del disco
description: Recupero dello stato dell'unità e del disco
ms.assetid: 5e3e6107-d2bc-450c-a86e-5d3ef7b3092a
keywords:
- Windows Media Player, masterizzazione CD
- Modello a oggetti di Windows Media Player, masterizzazione CD
- modello a oggetti, masterizzazione CD
- Controllo ActiveX Windows Media Player, masterizzazione CD
- Controllo ActiveX, masterizzazione CD
- Controllo ActiveX Windows Media Player Mobile, masterizzazione CD
- Windows Media Player Mobile, masterizzazione CD
- Masterizzazione CD, recupero dello stato di unità e dischi
- masterizzazione di CD, recupero dello stato di unità e dischi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eab66581c336f642fd53b22f81949847d0a1c89
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103858025"
---
# <a name="retrieving-the-drive-and-disc-status"></a>Recupero dello stato dell'unità e del disco

Prima di avviare un'operazione di masterizzazione CD, è necessario verificare che l'unità CD-ROM selezionata supporti l'operazione che si desidera eseguire. È ad esempio necessario verificare che un CD sia in grado di essere cancellato prima di chiamare [IWMPCdromBurn:: erase](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-erase). Il codice seguente illustra un esempio dell'uso di [IWMPCdromBurn:: disavailable](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-isavailable) per determinare se un'operazione è supportata:


```C++
VARIANT_BOOL vbResult;
    
// Check whether this drive can burn CDs.
CComBSTR bstrItem;
HRESULT hr = bstrItem.Append("Burn");
if (SUCCEEDED(hr))
{
    hr = m_spCdromBurn->isAvailable(bstrItem, &vbResult);
}
if (SUCCEEDED(hr))
{
    if (VARIANT_TRUE == vbResult)
    {
        // The current drive can burn CDs.
    }
}

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Masterizzazione di un CD**](burning-a-cd.md)
</dt> <dt>

[**Recupero dell'interfaccia di masterizzazione CD**](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[**Avvio del processo di masterizzazione**](starting-the-burn-process.md)
</dt> <dt>

[**Cancellazione di un CD riscrivibile**](erasing-a-rewritable-cd.md)
</dt> <dt>

[**Recupero dello stato di masterizzazione**](retrieving-the-burn-status.md)
</dt> </dl>

 

 




