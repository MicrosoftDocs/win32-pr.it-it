---
description: Un motore di riconoscimento della grafia, o un riconoscimento, è un software che elabora input penna e converte tale input penna in testo.
ms.assetid: b64f6856-453c-4080-84e0-0a9e69e79de7
title: Uso del contesto per migliorare l'accuratezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd5c807804c1855e0be56b09f08448e3dc2967d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306719"
---
# <a name="using-context-to-improve-accuracy"></a>Uso del contesto per migliorare l'accuratezza

Un motore di riconoscimento della grafia, o un riconoscimento, è un software che elabora input penna e converte tale input penna in testo. Un contesto è pertinente, le informazioni specifiche dell'applicazione fornite a un riconoscimento per migliorare l'accuratezza del riconoscimento. In altre parole, context è qualsiasi informazione sull'input che aiuta il riconoscimento nell'elaborare accuratamente l'input penna in un campo.

In questa sezione vengono descritti i diversi modi in cui è possibile sfruttare il contesto nell'applicazione per Tablet PC, ponendo l'accento sulla tecnica di programmazione preferita per le applicazioni che non sono abilitate per l'input penna.

> [!Note]  
> Sono disponibili alcune sezioni della tecnologia Tablet PC di Windows Vista Software Development Kit (SDK) in cui viene usato il termine "contesto" in relazione all'oggetto [**RecognizerContext**](inkrecognizercontext-class.md) e alle relative proprietà [**PrefixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_prefixtext) e [**SuffixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_suffixtext) . Non confondere questi altri utilizzi di "context" con la definizione in questa sezione.

 

 

 



