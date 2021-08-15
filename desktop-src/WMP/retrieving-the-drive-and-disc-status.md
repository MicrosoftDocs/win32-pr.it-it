---
title: Recupero dello stato dell'unità e del disco
description: Recupero dello stato dell'unità e del disco
ms.assetid: 5e3e6107-d2bc-450c-a86e-5d3ef7b3092a
keywords:
- Windows Media Player,masterizzazione CD
- Windows Media Player a oggetti, masterizzazione CD
- modello a oggetti, masterizzazione CD
- Windows Media Player ActiveX controllo, masterizzazione CD
- ActiveX controllo, masterizzazione CD
- Windows Media Player Controllo ActiveX per dispositivi mobili, masterizzazione CD
- Windows Media Player Mobile, masterizzazione CD
- Masterizzazione CD, recupero dell'unità e dello stato del disco
- masterizzazione di CD, recupero dell'unità e dello stato del disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 664315972158b4cf68e7f766f98be095a27d7fa8496f983305cc6baaafe784d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117746273"
---
# <a name="retrieving-the-drive-and-disc-status"></a>Recupero dello stato dell'unità e del disco

Prima di avviare un'operazione di masterizzazione cd, è necessario assicurarsi che l'unità CD-ROM selezionata supporti l'operazione che si vuole eseguire. Ad esempio, è necessario verificare che un CD sia in grado di essere cancellato prima di chiamare [IWMPCdromBurn::erase](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-erase). Il codice seguente illustra un esempio di uso [di IWMPCdromBurn::isAvailable](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-isavailable) per determinare se è supportata un'operazione:


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

[**Cancellazione di un CD risibile**](erasing-a-rewritable-cd.md)
</dt> <dt>

[**Recupero dello stato di masterizzazione**](retrieving-the-burn-status.md)
</dt> </dl>

 

 




