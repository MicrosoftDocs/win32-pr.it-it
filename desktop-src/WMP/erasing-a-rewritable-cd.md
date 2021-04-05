---
title: Cancellazione di un CD riscrivibile
description: Cancellazione di un CD riscrivibile
ms.assetid: 272fdd2b-c174-4bde-b05e-839d547532a6
keywords:
- Windows Media Player, masterizzazione CD
- Modello a oggetti di Windows Media Player, masterizzazione CD
- modello a oggetti, masterizzazione CD
- Controllo ActiveX Windows Media Player, masterizzazione CD
- Controllo ActiveX, masterizzazione CD
- Controllo ActiveX Windows Media Player Mobile, masterizzazione CD
- Windows Media Player Mobile, masterizzazione CD
- Masterizzazione CD, cancellazione di CDs riscrivibili
- masterizzazione di CDs, cancellazione di CDs riscrivibili
- cancellazione di CDs riscrivibili
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7025b7cd70c86c0b832aa792e50a8a2c64e7f45
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046308"
---
# <a name="erasing-a-rewritable-cd"></a>Cancellazione di un CD riscrivibile

L'interfaccia [IWMPCdromBurn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) fornisce un metodo per cancellare i dischi CD-RW. Prima di cancellare un CD, è prima necessario assicurarsi che l'operazione sia supportata. Per ulteriori informazioni, vedere [recupero dello stato dell'unità e del disco](retrieving-the-drive-and-disc-status.md).

Per iniziare a cancellare il contenuto di un CD riscrivibile, chiamare [IWMPCdromBurn:: erase](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-erase).


```C++

    HRESULT hr = m_spCdromBurn->erase();
    

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Masterizzazione di un CD**](burning-a-cd.md)
</dt> <dt>

[**Recupero dell'interfaccia di masterizzazione CD**](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[**Avvio del processo di masterizzazione**](starting-the-burn-process.md)
</dt> <dt>

[**Recupero dello stato dell'unità e del disco**](retrieving-the-drive-and-disc-status.md)
</dt> <dt>

[**Recupero dello stato di masterizzazione**](retrieving-the-burn-status.md)
</dt> </dl>

 

 




