---
description: Derivazione da CBasePin
ms.assetid: ef453bec-e5a9-4185-94e3-f934e748b11f
title: Derivazione da CBasePin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b07eb76fc2913152a69ec729f49826e8b35f1524a3841c5e0d3085ea0634f646
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079261"
---
# <a name="deriving-from-cbasepin"></a>Derivazione da CBasePin

Per implementare un pin [**usando CBasePin**](cbasepin.md), è necessario derivare una nuova classe dalla classe di base ed eseguire l'override di diversi dei relativi metodi. È necessario eseguire l'override dei metodi seguenti:

-   [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md)
-   [**CBasePin::GetMediaType**](cbasepin-getmediatype.md)

Sarà probabilmente necessario eseguire l'override di questi metodi aggiuntivi:

-   [**CBasePin::Active**](cbasepin-active.md)
-   [**CBasePin::BreakConnect**](cbasepin-breakconnect.md)
-   [**CBasePin::CheckConnect**](cbasepin-checkconnect.md)
-   [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md)
-   [**CBasePin::EndOfStream**](cbasepin-endofstream.md)
-   [**CBasePin::Inactive**](cbasepin-inactive.md)
-   [**CBasePin::Notify**](cbasepin-notify.md)
-   [**CBasePin::Run**](cbasepin-run.md)

Infine, è necessario implementare [**i metodi IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) [**e IPin::EndFlush.**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush)

Alcuni di questi metodi vengono implementati nelle classi di base che derivano da **CBasePin,** ad esempio [**CBaseInputPin**](cbaseinputpin.md) [**e CBaseOutputPin.**](cbaseoutputpin.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**CBasePin**](cbasepin.md)
</dt> </dl>

 

 



