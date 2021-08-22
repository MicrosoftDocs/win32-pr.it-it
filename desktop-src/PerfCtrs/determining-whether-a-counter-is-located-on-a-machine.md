---
description: Per determinare se un contatore è installato in un computer specifico, chiamare PdhValidatePath con il percorso completo del contatore. La funzione restituisce ERROR \_ SUCCESS se il contatore si trova nel computer specificato.
ms.assetid: 5533a8d8-3621-4ce7-984c-c3895adef531
title: Determinare se un contatore si trova in un computer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc2cc6672125f961fc2759d264caa6c33ab68f46347c915e82d1666f667692fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061199"
---
# <a name="determining-whether-a-counter-is-located-on-a-computer"></a>Determinare se un contatore si trova in un computer

Per determinare se un contatore è installato in un computer specifico, chiamare [**PdhValidatePath**](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepatha) con il percorso completo del contatore. La funzione restituisce ERROR \_ SUCCESS se il contatore si trova nel computer specificato.

[**PdhValidatePath convalida**](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepatha) l'intero percorso; Pertanto, se un oggetto, un'istanza o un contatore nel percorso non esiste, il valore restituito lo indica. **PdhValidatePath verifica** il percorso del contatore specificato in questo ordine: computer, oggetto prestazione, istanza e contatore.

 

 



