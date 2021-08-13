---
description: Un motore di riconoscimento della grafia, o riconoscimento, è un software che elabora l'input penna e lo converte in testo.
ms.assetid: b64f6856-453c-4080-84e0-0a9e69e79de7
title: Uso del contesto per migliorare l'accuratezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7564c18ace39c17e8877c3e5edee6464caea0c36d148cffbfcfb3b5ac09f666
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118715275"
---
# <a name="using-context-to-improve-accuracy"></a>Uso del contesto per migliorare l'accuratezza

Un motore di riconoscimento della grafia, o riconoscimento, è un software che elabora l'input penna e lo converte in testo. Un contesto è pertinente, informazioni specifiche dell'applicazione fornite a un sistema di riconoscimento per migliorare l'accuratezza del riconoscimento. In altre parole, il contesto è qualsiasi informazione sull'input che consente al riconoscimento di elaborare accuratamente l'input penna in un campo.

Questa sezione descrive i diversi modi in cui è possibile sfruttare il contesto nell'applicazione Tablet PC, ponendo particolare attenzione alla tecnica programmatica preferita per le applicazioni che non sono abilitate per l'input penna.

> [!Note]  
> Nelle sezioni Relative alla tecnologia Tablet PC di Windows Vista Software Development Kit (SDK) viene usato il termine "contesto" per quanto riguarda l'oggetto [**RecognizerContext**](inkrecognizercontext-class.md) e le relative proprietà [**PrefixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_prefixtext) e [**SuffixText.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_suffixtext) Non confondere questi altri utilizzi di "contesto" con la definizione in questa sezione.

 

 

 



