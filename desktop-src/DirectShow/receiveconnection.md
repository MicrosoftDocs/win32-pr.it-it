---
description: ReceiveConnection
ms.assetid: 90a6a09a-95e1-4adf-8e0b-269f971aaa67
title: ReceiveConnection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80fd9fe31f87a34dc3bfdfc4ecfb532255138b9c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124671"
---
# <a name="receiveconnection"></a>ReceiveConnection

Questo meccanismo consente a un pin di output di proporre una modifica di formato al peer downstream, quando il nuovo formato richiede un buffer più grande. Il pin di output esegue le operazioni seguenti:

1.  Chiama [**Ipin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) sul pin di input downstream.
2.  Se ha `ReceiveConnection` esito positivo, chiama [**IMemInputPin:: NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) sul pin di input.

Inoltre, per modificare le dimensioni del buffer, potrebbe essere necessario chiamare [**IMemAllocator:: seproperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) , quindi eseguire il commit e il commit dell'allocatore. Assicurarsi di recapitare tutti gli esempi in sospeso nel formato precedente prima di modificare le dimensioni del buffer.

Alcuni decodificatori MPEG-2 usano questo meccanismo per passare tra l'output MPEG-1 e MPEG-2 o se le dimensioni del video cambiano.

 

 



