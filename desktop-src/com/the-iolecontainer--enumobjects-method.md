---
title: Metodo IOleContainer EnumObjects
description: Metodo IOleContainer EnumObjects
ms.assetid: 29562d0e-dc8b-49cd-a58f-1f3125a438ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbd74e4916eec4d58240f702a09fd8376008fe0bb352113e1512bd2882d8dee9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462321"
---
# <a name="the-iolecontainerenumobjects-method"></a>Metodo IOleContainer::EnumObjects

Questo metodo viene utilizzato per enumerare tutti gli oggetti OLE contenuti in un documento o in un modulo, che restituisce un puntatore a interfaccia per ogni oggetto OLE. Il contenitore deve restituire puntatori a ogni oggetto OLE che condivide lo stesso contenitore. È necessario enumerare anche i form annidati o i controlli annidati.

Alcuni contenitori implementano controlli Extender, che esetendono i controlli non ActiveX e quindi restituiscono puntatori a questi controlli extender durante l'enumerazione di un form. Questo comportamento consente ActiveX controlli e ActiveX contenitori di controlli per integrarsi in modo corretto con i controlli non ActiveX ed è pertanto consigliato, ma non obbligatorio.

 

 




