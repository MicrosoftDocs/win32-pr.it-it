---
description: ReceiveConnection
ms.assetid: 90a6a09a-95e1-4adf-8e0b-269f971aaa67
title: ReceiveConnection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55a8a91cbf9870d6c53592ff823f710eb5875fa939592309425df0a0bca6f0e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072765"
---
# <a name="receiveconnection"></a>ReceiveConnection

Questo meccanismo consente a un pin di output di proporre una modifica del formato al peer downstream, quando il nuovo formato richiede un buffer più grande. Il pin di output esegue le operazioni seguenti:

1.  Chiama [**IPin::ReceiveConnection sul**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) pin di input downstream.
2.  Se `ReceiveConnection` ha esito positivo, chiama [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) sul pin di input.

Inoltre, il pin di output potrebbe dover chiamare [**IMemAllocator::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) e quindi eseguire il decommit e il ricommit dell'allocatore per modificare le dimensioni del buffer. Assicurarsi di distribuire tutti gli esempi in sospeso nel formato precedente prima di modificare le dimensioni del buffer.

Alcuni decodificatori MPEG-2 usano questo meccanismo per passare dall'output MPEG-1 a MPEG-2 o se le dimensioni del video cambiano.

 

 



