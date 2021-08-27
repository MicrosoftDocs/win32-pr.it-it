---
title: PeakValue
description: L'attributo PeakValue contiene un valore di ampiezza a 16 bit che designa il livello di volume massimo del contenuto audio.
ms.assetid: 885f6d4c-661a-4681-96b6-c1a282c8bf18
keywords:
- PeakValue windows Media Format
topic_type:
- apiref
api_name:
- PeakValue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e3089ac6d4b789d740f256a5c44c1911eb3501bc654c3b94d0006d405616572
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110261"
---
# <a name="peakvalue"></a>PeakValue

**L'attributo PeakValue** contiene un valore di ampiezza a 16 bit che designa il livello di volume massimo del contenuto audio. Con [**AverageLevel,**](averagelevel.md)questo attributo viene usato per la normalizzazione. La normalizzazione è il processo di regolazione del livello di volume di riproduzione dei file audio in modo che le parti più rumorose dei file riprodusino allo stesso livello e il volume medio per ognuno di essi sia lo stesso.

## <a name="global-constant"></a>Costante globale

g \_ wszPeakValue

## <a name="data-type"></a>Tipo di dati

**DWORD \_ DI \_ TIPO WMT**

## <a name="remarks"></a>Commenti

Questo attributo viene impostato dall'oggetto writer in base alle informazioni del codec. Solo i flussi compressi con uno dei codec audio Windows hanno un valore impostato automaticamente.

**PeakValue** non è di sola lettura. Tuttavia, se il file verrà riprodotto dal Windows Media Player, non è consigliabile modificare questo valore. L Windows Media Player viene utilizzato per normalizzare i livelli di file in una playlist.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




