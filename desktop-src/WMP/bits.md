---
title: BITS
description: BITS
ms.assetid: 67159ad9-e11b-4fea-bff2-468d5a7447be
keywords:
- Windows Media Player Online Stores, Servizio trasferimento intelligente in background (BITS)
- archivi online, Servizio trasferimento intelligente in background (BITS)
- digitare 2 archivi online, Servizio trasferimento intelligente in background (BITS)
- Servizio trasferimento intelligente in background (BITS)
- BITS (Servizio trasferimento intelligente in background)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527edf56e7505c64657d167e0210190e00d697d2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337926"
---
# <a name="bits"></a>BITS

Il [servizio trasferimento intelligente in background](/windows/desktop/Bits/background-intelligent-transfer-service-portal) è una funzionalità del sistema operativo Windows. BITS trasferisce i file (download o caricamenti) tra un client e un server e fornisce informazioni sullo stato di avanzamento correlate ai trasferimenti. Se si desidera trasferire file usando il codice C++, BITS è la tecnologia corretta da usare. Se si desidera trasferire i file utilizzando il codice JScript nella pagina Web del negozio online, utilizzare invece gestione download.

Poiché Windows Media Player Download Manager USA BITS, è possibile eseguire le operazioni necessarie per configurare i processi di copia BITS in modo che Windows Media Player gestisca i processi. A tale scopo, è necessario seguire la convenzione descritta nella sezione relativa alla [convenzione dei processi BITS di Windows Media Player](windows-media-player-bits-job-convention.md) durante l'aggiunta dei processi alla coda di trasferimento BITS. Questa sezione descrive anche un meccanismo per il recupero di informazioni sui processi BITS dalla pagina Web dei negozi online.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso di Download Manager**](using-the-download-manager.md)
</dt> <dt>

[**Informazioni sui negozi online di tipo 2**](about-type-2-online-stores.md)
</dt> </dl>

 

 