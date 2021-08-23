---
description: L'attributo swapinputs specifica se scambiare gli input di transizione. Se il valore è TRUE, gli input vengono scambiati. Il valore predefinito è FALSE.
ms.assetid: 2b8d95ec-2c6c-4bd8-83e9-7f72770449b5
title: Attributo swapinputs
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b74d16d9b195f504188f4684cf234a5b0c7627274c6e74d57e6824df20a0c3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951710"
---
# <a name="swapinputs-attribute"></a>Attributo swapinputs

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

`swapinputs`L'attributo specifica se scambiare gli input di transizione. Se il valore è **TRUE,** gli input vengono scambiati. Il valore predefinito è **FALSE.**

## <a name="possible-values"></a>Valori possibili

I valori seguenti sono definiti come TRUE: y, Y, t, T, 1. I valori seguenti sono definiti come FALSE: n, N, f, F, 0 (zero).

## <a name="applies-to"></a>Si applica a

[**Transizione**](transition-element.md)

## <a name="remarks"></a>Commenti

Per impostazione predefinita, una transizione procede dal composito di tutti i livelli con priorità inferiore al livello in cui si trova la transizione. Se `swapinputs` l'attributo è 1, questa direzione viene inversa. Per altre informazioni sul modello a livelli usato da DES, vedere [Modello di sequenza temporale](the-timeline-model.md).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Attributi XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineTrans::SetSwapInputs**](iamtimelinetrans-setswapinputs.md)
</dt> </dl>

 

 



