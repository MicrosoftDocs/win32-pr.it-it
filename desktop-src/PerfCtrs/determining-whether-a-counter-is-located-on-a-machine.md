---
description: Per determinare se un contatore è installato in un computer specifico, chiamare PdhValidatePath con il percorso completo del contatore. La funzione restituisce l'errore \_ esito positivo se il contatore si trova nel computer specificato.
ms.assetid: 5533a8d8-3621-4ce7-984c-c3895adef531
title: Determinare se un contatore si trova in un computer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 795878e2f9c97989fe924737ec7f8e7f14bdc67c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967517"
---
# <a name="determining-whether-a-counter-is-located-on-a-computer"></a>Determinare se un contatore si trova in un computer

Per determinare se un contatore è installato in un computer specifico, chiamare [**PdhValidatePath**](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepatha) con il percorso completo del contatore. La funzione restituisce l'errore \_ esito positivo se il contatore si trova nel computer specificato.

[**PdhValidatePath**](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepatha) convalida l'intero percorso. Pertanto, se un oggetto, un'istanza o un contatore nel percorso non esiste, il valore restituito indica. **PdhValidatePath** verifica il percorso del contatore specificato in questo ordine: computer, oggetto prestazioni, istanza e contatore.

 

 



