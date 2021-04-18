---
description: CSourcePosition è una classe astratta per l'implementazione dell'interfaccia IMediaPosition in un filtro di origine.
ms.assetid: 838d2efd-6870-4412-98e2-fb2628e14bf3
title: Classe CSourcePosition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourcePosition
api_type:
- COM
api_location: ''
ms.openlocfilehash: 0b88289381641edcef5922557862729acbb81f54
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303774"
---
# <a name="csourceposition-class"></a>Classe CSourcePosition

`CSourcePosition` è una classe astratta per l'implementazione dell'interfaccia [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) in un filtro di origine.

Questa classe è obsoleta. Se il filtro di origine è ricercabile, deve esporre l'interfaccia [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) anziché **IMediaPosition**. A questo scopo, è possibile usare la classe di base [**CSourceSeeking**](csourceseeking.md) .

 

 



