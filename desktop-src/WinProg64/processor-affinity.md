---
title: Affinità processori in WOW64
description: Windows a 32 bit supporta un massimo di 32 processori. Pertanto, le funzioni come GetProcessAffinityMask simulano un computer con processori 32 quando vengono chiamate in WOW64.
ms.assetid: f50a03e8-1c23-4eb0-a1ff-471c28d6b611
keywords:
- Programmazione di Windows con affinità processori a 64 bit
- Programmazione Windows WOW64 a 64 bit, affinità processori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c60ad6cf5055737dc39abd735211c5b4ec4ab9d7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728410"
---
# <a name="processor-affinity-under-wow64"></a>Affinità processori in WOW64

Windows a 32 bit supporta un massimo di 32 processori. Pertanto, le funzioni come [**GetProcessAffinityMask**](/windows/desktop/api/winbase/nf-winbase-getprocessaffinitymask) simulano un computer con processori 32 quando vengono chiamate in WOW64.

La maschera di affinità viene ottenuta eseguendo un'operazione OR bit per bit dei primi 32 bit della maschera con i 32 bit inferiori. Se pertanto un thread presenta affinità per i processori 0, 1 e 32, WOW64 segnala l'affinità come 0 e 1, perché il processore 32 viene mappato al processore 0. Le funzioni che impostano l'affinità del processore, ad esempio [**SetThreadAffinityMask**](/windows/desktop/api/winbase/nf-winbase-setthreadaffinitymask), limitano i processori ai primi processori 32 in WOW64.

Per ulteriori informazioni sull'affinità processori, vedere la pagina relativa a [più processori](/windows/desktop/ProcThread/multiple-processors).

 

 