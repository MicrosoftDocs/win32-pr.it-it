---
description: Per generare una finestra di dialogo in cui viene richiesto all'utente di inserire il disco successivo o di specificare un nuovo percorso di origine, chiamare SetupPromptForDisk.
ms.assetid: a780e7ab-bd96-43e4-9425-e15a758391f4
title: Richiesta di un disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 404e88611ec21b7a29d69ab306dc0e7c4e1b98e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313276"
---
# <a name="prompting-for-a-disk"></a>Richiesta di un disco

Per generare una finestra di dialogo in cui viene richiesto all'utente di inserire il disco successivo o di specificare un nuovo percorso di origine, chiamare [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska). Questa funzione viene utilizzata dalle routine di callback per generare un'interfaccia utente quando la notifica, [**SPFILENOTIFY \_ NEEDMEDIA**](spfilenotify-needmedia.md), viene inviata alla routine di callback.

La finestra di dialogo generata da [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska) offre all'utente la possibilità di inserire un disco, specificare un nuovo percorso di origine o annullare l'installazione.

È possibile utilizzare i flag specificati durante la chiamata a [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska) per modificare il layout e il comportamento della finestra di dialogo. Utilizzando questi flag, è possibile controllare se nella finestra di dialogo sono inclusi pulsanti che consentono all'utente di cercare un nuovo percorso di origine oppure ignorare il file corrente. I flag consentono inoltre di controllare il comportamento della finestra di dialogo, ad esempio il segnale acustico quando viene visualizzato per la prima volta e la possibilità di essere visualizzata come finestra in primo piano.

 

 



