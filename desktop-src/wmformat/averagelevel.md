---
title: AverageLevel
description: L'attributo AverageLevel contiene un valore di ampiezza a 16 bit che indica il livello medio di volume del contenuto audio.
ms.assetid: e6270ac8-5de3-4dee-824c-ba25fdd272c8
keywords:
- AverageLevel windows Media Format
topic_type:
- apiref
api_name:
- AverageLevel
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fd8745c5983eca67a02506b6cdeeabaca0a61a4c3f8b2a6993a73359d87adba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028159"
---
# <a name="averagelevel"></a>AverageLevel

**L'attributo AverageLevel** contiene un valore di ampiezza a 16 bit che indica il livello medio di volume del contenuto audio. Con [**PeakValue**](peakvalue.md)questo attributo viene usato per la normalizzazione. La normalizzazione è il processo di regolazione del livello di volume di riproduzione dei file audio in modo che le parti più rumorose della riproduzione dei file allo stesso livello e il volume medio per ognuno di essi sia lo stesso.

## <a name="global-constant"></a>Costante globale

g \_ wszAverageLevel

## <a name="data-type"></a>Tipo di dati

**DWORD \_ DI TIPO \_ WMT**

## <a name="remarks"></a>Commenti

Questo attributo viene impostato dall'oggetto writer in base alle informazioni del codec. Solo i flussi compressi con uno dei Windows media audio hanno un valore impostato automaticamente.

**AverageLevel** non è di sola lettura. Tuttavia, se il file verrà riprodotto dal Windows Media Player, non modificare questo valore. Il Windows Media Player usa questo valore per normalizzare i livelli di file in una playlist.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




