---
title: Audio Low-Delay
description: Audio Low-Delay
ms.assetid: f93819eb-f38a-45a0-aa1b-4e677e33daf8
keywords:
- Windows Media Format SDK, audio a ritardo ridotto
- Windows Media Format SDK, supporto audio
- codec, audio a ritardo ridotto
- codec, supporto audio
- audio a ritardo ridotto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be8cedd3a6bb54942f5a517c7133e993cf5b11cb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298897"
---
# <a name="low-delay-audio"></a>Audio Low-Delay

L'audio a ritardo ridotto è una modalità di codifica che produce audio compresso con un'impostazione della finestra buffer più piccola rispetto ad altre modalità. Questa operazione è utile per i flussi che devono essere scambiati rapidamente durante la riproduzione. Lo scenario tipico per questa funzionalità è una presentazione con flusso che include la possibilità di cambiare arbitrariamente il contenuto, ad esempio la modifica del canale di una televisione.

Quando si usa un formato audio a ritardo ridotto, la latenza per il cambio di contenuto è notevolmente ridotta rispetto ad altri formati audio. La latenza viene ridotta anche per le trasmissioni live quando si usano formati a ritardo ridotto.

Questa funzionalità è supportata dai codec Windows Media Audio 9,1 e Windows Media Audio 9,1 Professional. I formati a ritardo ridotto sono disponibili solo per la codifica della velocità in bit costante (sia a un passaggio che a due passaggi).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità di codec**](codec-features.md)
</dt> </dl>

 

 




