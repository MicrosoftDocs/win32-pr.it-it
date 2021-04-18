---
description: Effetto busta volume
ms.assetid: 17b6d842-e79c-49b0-baa4-1535b4a2c6ae
title: Effetto busta volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9364b88b1928e533a031f0700cb8a2c44bc9822d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314368"
---
# <a name="volume-envelope-effect"></a>Effetto busta volume

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

L'effetto busta volume imposta il volume in un flusso audio.

ID classe (CLSID): {036A9790-C153-11D2-9EF7-006008039E37}

Nome variabile CLSID: CLSID \_ AudMixer

Proprietà



| Proprietà | Type   | Predefinito | Descrizione                                                                                                           |
|----------|--------|---------|-----------------------------------------------------------------------------------------------------------------------|
| Vol.      | double | 1.0     | Volume, come percentuale del volume creato. È possibile produrre dissolvenze audio variando il valore di questa proprietà nel tempo. |



 

## <a name="remarks"></a>Commenti

Ogni oggetto in una sequenza temporale può avere al massimo un effetto envelope del volume. In una composizione o un gruppo, la busta del volume viene applicata per prima, prima di qualsiasi altro effetto audio, indipendentemente dalla relativa priorità. In un'origine o in una traccia l'effetto del volume viene applicato in base alla priorità.

 

 



