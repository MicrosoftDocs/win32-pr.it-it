---
description: L'attributo swapinputs specifica se scambiare gli input di transizione. Se il valore è TRUE, gli input vengono scambiati. Il valore predefinito è FALSE.
ms.assetid: 2b8d95ec-2c6c-4bd8-83e9-7f72770449b5
title: Attributo swapinputs
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27e2f02c642283e90b994bcd1bfa9e05076a7bae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349066"
---
# <a name="swapinputs-attribute"></a>Attributo swapinputs

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

L' `swapinputs` attributo specifica se scambiare gli input di transizione. Se il valore è **true**, gli input vengono scambiati. Il valore predefinito è **false**.

## <a name="possible-values"></a>Valori possibili

I valori seguenti sono definiti come TRUE: y, Y, t, T, 1. I valori seguenti sono definiti come FALSE: n, N, f, F, 0 (zero).

## <a name="applies-to"></a>Si applica a

[**transizione**](transition-element.md)

## <a name="remarks"></a>Commenti

Per impostazione predefinita, una transizione procede dalla composizione di tutti i livelli di priorità inferiore al livello su cui risiede la transizione. Se l' `swapinputs` attributo è 1, questa direzione è invertita. Per ulteriori informazioni sul modello di sovrapposizione utilizzato da DES, vedere [il modello di sequenza temporale](the-timeline-model.md).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Attributi XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineTrans::SetSwapInputs**](iamtimelinetrans-setswapinputs.md)
</dt> </dl>

 

 



