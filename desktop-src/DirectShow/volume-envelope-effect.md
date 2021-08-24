---
description: Effetto volume envelope
ms.assetid: 17b6d842-e79c-49b0-baa4-1535b4a2c6ae
title: Effetto volume envelope
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4ecb66914063596849522a0e4bb340fc84f7d80e5ea1113bfdae2d32e855d3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746951"
---
# <a name="volume-envelope-effect"></a>Effetto volume envelope

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

L'effetto Volume Envelope imposta il volume su un flusso audio.

ID classe (CLSID): {036A9790-C153-11D2-9EF7-006008039E37}

Nome variabile CLSID: CLSID \_ AudMixer

Proprietà



| Proprietà | Type   | Predefinito | Descrizione                                                                                                           |
|----------|--------|---------|-----------------------------------------------------------------------------------------------------------------------|
| Vol.      | double | 1.0     | Volume, come percentuale del volume creato. È possibile produrre dissolvenze audio variando il valore di questa proprietà nel tempo. |



 

## <a name="remarks"></a>Commenti

Ogni oggetto in una sequenza temporale può avere al massimo un effetto di busta del volume. In una composizione o in un gruppo, l'inviluppo del volume viene applicato per primo, prima di qualsiasi altro effetto audio, indipendentemente dalla priorità. In un'origine o in una traccia, l'effetto volume viene applicato in base alla priorità.

 

 



