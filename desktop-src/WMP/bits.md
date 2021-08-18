---
title: BITS
description: BITS
ms.assetid: 67159ad9-e11b-4fea-bff2-468d5a7447be
keywords:
- Windows Media Player online store,Servizio trasferimento intelligente in background (BITS)
- negozi online, Servizio trasferimento intelligente in background (BITS)
- Tipo 2 di negozi online, Servizio trasferimento intelligente in background (BITS)
- Servizio trasferimento intelligente in background (BITS)
- BITS (Servizio trasferimento intelligente in background)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6f1a9987ca50d659063e9689289334201b0121ccfe5257f71030536eee03a52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135974"
---
# <a name="bits"></a>BITS

Il [Servizio trasferimento intelligente in background](/windows/desktop/Bits/background-intelligent-transfer-service-portal) è una funzionalità del Windows operativo. BITS trasferisce i file (download o caricamenti) tra un client e un server e fornisce informazioni sullo stato relative ai trasferimenti. Se si vogliono trasferire file usando codice C++, BITS è la tecnologia corretta da usare. Se si vuole trasferire i file usando JScript codice nella pagina Web del negozio online, usare download manager.

Poiché Windows Media Player Download Manager usa BITS, è possibile eseguire le operazioni necessarie per configurare i processi di copia BITS in modo che Windows Media Player gestirli automaticamente. A tale scopo, è necessario seguire la convenzione descritta nella sezione [Windows Media Player BitS Job Convention](windows-media-player-bits-job-convention.md) quando si aggiungono i processi alla coda di trasferimento BITS. Questa sezione descrive anche un meccanismo per recuperare informazioni sui processi BITS dalla pagina Web dei negozi online.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso di Download Manager**](using-the-download-manager.md)
</dt> <dt>

[**Informazioni sui negozi online di tipo 2**](about-type-2-online-stores.md)
</dt> </dl>

 

 