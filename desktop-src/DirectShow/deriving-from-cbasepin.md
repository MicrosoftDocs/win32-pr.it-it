---
description: Derivazione da CBasePin
ms.assetid: ef453bec-e5a9-4185-94e3-f934e748b11f
title: Derivazione da CBasePin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82ab56da3ae326be175c9519b5248e53fa02b82f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304401"
---
# <a name="deriving-from-cbasepin"></a>Derivazione da CBasePin

Per implementare un PIN usando [**CBasePin**](cbasepin.md), è necessario derivare una nuova classe dalla classe di base ed eseguire l'override di diversi metodi. È necessario eseguire l'override dei metodi seguenti:

-   [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md)
-   [**CBasePin::GetMediaType**](cbasepin-getmediatype.md)

Probabilmente sarà necessario eseguire l'override di questi metodi aggiuntivi:

-   [**CBasePin:: Active**](cbasepin-active.md)
-   [**CBasePin::BreakConnect**](cbasepin-breakconnect.md)
-   [**CBasePin:: CheckConnect**](cbasepin-checkconnect.md)
-   [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md)
-   [**CBasePin:: EndOfStream**](cbasepin-endofstream.md)
-   [**CBasePin:: inactive**](cbasepin-inactive.md)
-   [**CBasePin:: Notify**](cbasepin-notify.md)
-   [**CBasePin:: Run**](cbasepin-run.md)

Infine, è necessario implementare i metodi [**Ipin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) e [**Ipin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) .

Alcuni di questi metodi sono implementati nelle classi di base che derivano da **CBasePin**, ad esempio [**CBaseInputPin**](cbaseinputpin.md) e [**CBaseOutputPin**](cbaseoutputpin.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**CBasePin**](cbasepin.md)
</dt> </dl>

 

 



