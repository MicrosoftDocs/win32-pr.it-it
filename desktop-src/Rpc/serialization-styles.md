---
title: Stili di serializzazione
description: Sono disponibili tre stili che è possibile usare per modificare gli handle di serializzazione.
ms.assetid: 40b609b2-abad-4967-a5d1-948ac26fd65c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc825c24b591cdfea96a603835f0836eda68b3ba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396398"
---
# <a name="serialization-styles"></a>Stili di serializzazione

Sono disponibili tre stili che è possibile usare per modificare gli handle di serializzazione. Si tratta di:

-   [Serializzazione del buffer fissa](fixed-buffer-serialization.md)
-   [Serializzazione dinamica del buffer](dynamic-buffer-serialization.md)
-   [Serializzazione incrementale](incremental-serialization.md)

Indipendentemente dallo stile usato, è necessario creare un handle di serializzazione, serializzare i dati e quindi liberare l'handle. Lo stile viene impostato quando il programma crea l'handle e definisce la modalità di manipolazione di un buffer. L'handle gestisce il contesto appropriato associato a ognuno dei tre stili di serializzazione.

 

 




