---
title: Cancellazione di un CD risbilebile
description: Cancellazione di un CD risbilebile
ms.assetid: 272fdd2b-c174-4bde-b05e-839d547532a6
keywords:
- Windows Media Player,CD
- Windows Media Player a oggetti, CD
- modello a oggetti, CD
- Windows Media Player ActiveX controllo, CD
- ActiveX controllo, CD
- Windows Media Player Mobile ActiveX control,CD
- Windows Media Player Dispositivi mobili, CD-
- CD dispersi, cancellazione di CD risabilitabili
- CD risibili, cancellazione di CD risibili
- cancellazione di CD risabilitabili
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76fcce5d4782e847154c06dd17e5af3eb7c01b6a9941114f132b99cee9eb0ece
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118838169"
---
# <a name="erasing-a-rewritable-cd"></a>Cancellazione di un CD risbilebile

[L'interfaccia IWMPCdromMethod fornisce](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) un metodo per cancellare i dischi CD-RW. Prima di cancellare un CD, è necessario assicurarsi che l'operazione sia supportata. Per altre informazioni, vedere Recupero dello stato [dell'unità e del disco.](retrieving-the-drive-and-disc-status.md)

Per iniziare a cancellare il contenuto di un CD risincrizzabile, chiamare [IWMPCdromComb::erase](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-erase).


```C++

    HRESULT hr = m_spCdromBurn->erase();
    

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creare un cd**](burning-a-cd.md)
</dt> <dt>

[**Recupero dell'interfaccia di masterizzazione CD**](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[**Avvio del processo di masterizzazione**](starting-the-burn-process.md)
</dt> <dt>

[**Recupero dello stato dell'unità e del disco**](retrieving-the-drive-and-disc-status.md)
</dt> <dt>

[**Recupero dello stato della masterizzazione**](retrieving-the-burn-status.md)
</dt> </dl>

 

 




