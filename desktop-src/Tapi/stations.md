---
description: I set di stazioni monitorati tramite un collegamento di terze parti vengono modellati come un dispositivo a linee e possibilmente un dispositivo telefonico associato.
ms.assetid: 1d116734-cd8f-40f1-9069-2dad351a24bf
title: Stazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff497eb70d1a1fd8441eeb8ad24bae6e5d1cd03e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318932"
---
# <a name="stations"></a>Stazioni

I set di stazioni monitorati tramite un collegamento di terze parti vengono modellati come un dispositivo a linee e possibilmente un dispositivo telefonico associato. Il dispositivo a linee può avere più indirizzi, se il terminale modellato supporta più di un numero di directory (DN). È possibile modellare più aspetti della chiamata nello stesso DN come un singolo indirizzo che supporta più chiamate.

Le chiamate tra due stazioni sull'opzione hanno due handle di chiamata, uno che fornisce la visualizzazione chiamata dalla prima stazione (sul dispositivo linea) e l'altro che fornisce la visualizzazione chiamata dalla seconda stazione (sul dispositivo a linee). Ad esempio, un [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) di terze parti inserito da un'applicazione sul server verrebbe indirizzato al dispositivo a linee associato alla stazione da cui deve essere stabilita la chiamata; viene creato un handle di chiamata su tale riga, sull'indirizzo specificato in [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) , dando così il controllo su quale DN viene usato in un telefono che supporta più DNS. Quando la chiamata viene offerta all'indirizzo di destinazione, viene creato un nuovo handle di chiamata che mostra una chiamata nello stato *offering* ; le applicazioni saprebbero che era un'altra visualizzazione della stessa chiamata eseguita dal membro **dwCallID** in [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) per entrambe le chiamate. Entrambe le chiamate diventano *inattive* quando la chiamata è stata eliminata; una chiamata può essere eliminata dall'applicazione di terze parti eseguendo un [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) su uno degli handle di chiamata.

 

 



