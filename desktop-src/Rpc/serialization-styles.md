---
title: Stili di serializzazione
description: Esistono tre stili che è possibile usare per modificare gli handle di serializzazione.
ms.assetid: 40b609b2-abad-4967-a5d1-948ac26fd65c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bfaa7cd3198245441a27990d331bcd9f0bd0396b5075d9985b13da58012147d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925387"
---
# <a name="serialization-styles"></a>Stili di serializzazione

Esistono tre stili che è possibile usare per modificare gli handle di serializzazione. Si tratta di:

-   [Serializzazione del buffer fisso](fixed-buffer-serialization.md)
-   [Serializzazione dinamica del buffer](dynamic-buffer-serialization.md)
-   [Serializzazione incrementale](incremental-serialization.md)

Indipendentemente dal tipo utilizzato, è necessario creare un handle di serializzazione, serializzare i dati e quindi liberare l'handle. Lo stile viene impostato quando il programma crea l'handle e definisce il modo in cui viene modificato un buffer. L'handle mantiene il contesto appropriato associato a ognuno dei tre stili di serializzazione.

 

 




