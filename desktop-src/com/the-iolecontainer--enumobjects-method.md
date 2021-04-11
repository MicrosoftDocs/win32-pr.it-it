---
title: Metodo EnumObjects di IOleContainer
description: Metodo EnumObjects di IOleContainer
ms.assetid: 29562d0e-dc8b-49cd-a58f-1f3125a438ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a2dff2331374299abbc13cdd595aa709ec1aa74
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221016"
---
# <a name="the-iolecontainerenumobjects-method"></a>Il metodo IOleContainer:: EnumObjects

Questo metodo viene utilizzato per enumerare tutti gli oggetti OLE contenuti in un documento o un form, restituendo un puntatore a interfaccia per ogni oggetto OLE. Il contenitore deve restituire puntatori a ogni oggetto OLE che condivide lo stesso contenitore. È necessario enumerare anche i form nidificati o i controlli annidati.

Alcuni contenitori implementano i controlli Extender, che consentono di eseguire il wrapping dei controlli non ActiveX, quindi restituiscono i puntatori a questi controlli Extender come un form enumerato. Questo comportamento consente ai controlli ActiveX e ai contenitori di controlli ActiveX di integrarsi correttamente con i controlli non ActiveX ed è quindi consigliabile, ma non obbligatorio.

 

 




