---
title: PeakValue
description: L'attributo PeakValue contiene un valore di ampiezza a 16 bit che designa il livello di picco del volume del contenuto audio.
ms.assetid: 885f6d4c-661a-4681-96b6-c1a282c8bf18
keywords:
- PeakValue Windows Media Format
topic_type:
- apiref
api_name:
- PeakValue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37ef933ec1b10555aa4c88a24261313abb261163
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299135"
---
# <a name="peakvalue"></a>PeakValue

L'attributo **PeakValue** contiene un valore di ampiezza a 16 bit che designa il livello di picco del volume del contenuto audio. Con [**AverageLevel**](averagelevel.md), questo attributo viene usato per la normalizzazione. La normalizzazione è il processo di regolazione del livello di volume di riproduzione dei file audio, in modo che le parti più rumorose dei file vengano riavviate allo stesso livello e il volume medio per ognuno di essi sia lo stesso.

## <a name="global-constant"></a>Costante globale

g \_ wszPeakValue

## <a name="data-type"></a>Tipo di dati

**WMT \_ tipo \_ DWORD**

## <a name="remarks"></a>Commenti

Questo attributo viene impostato dall'oggetto writer in base alle informazioni del codec. Solo i flussi compressi con uno dei codec Windows Media Audio hanno un valore impostato automaticamente.

**PeakValue** non è di sola lettura. Tuttavia, se il file verrà riprodotto dalla Media Player di Windows, è consigliabile non modificare questo valore. Windows Media Player usa questa operazione per normalizzare i livelli di file in una playlist.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




