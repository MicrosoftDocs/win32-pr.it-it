---
description: I set di stazione monitorati tramite un collegamento di terze parti vengono modellati come un dispositivo linea e possibilmente un dispositivo telefonico associato.
ms.assetid: 1d116734-cd8f-40f1-9069-2dad351a24bf
title: Stazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ad9874542a63f05e124ea5df833aa0a433c03713cc3a2d7bb1ca3a471174e86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760719"
---
# <a name="stations"></a>Stazioni

I set di stazione monitorati tramite un collegamento di terze parti vengono modellati come un dispositivo linea e possibilmente un dispositivo telefonico associato. Il dispositivo line può avere più indirizzi, se il terminale modellato supporta più di un numero di directory (DN). È possibile modellare più chiamate sullo stesso DN come un singolo indirizzo che supporta più chiamate.

Le chiamate tra due stazioni sul commutatore hanno due handle di chiamata, uno che visualizza le chiamate dalla prima stazione (sul dispositivo di linea) e l'altro dalla seconda stazione (sul dispositivo di linea). Ad esempio, una [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) di terze parti inserita da un'applicazione nel server verrebbe indirizzata al dispositivo di linea associato alla stazione da cui deve essere chiamata la chiamata; Viene creato un handle di chiamata su tale riga, sull'indirizzo specificato in [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) , dando così il controllo sul DN usato in un telefono che supporta più DN. Quando la chiamata viene offerta all'indirizzo di destinazione, viene creato un nuovo handle di chiamata che mostra una chiamata *nello* stato dell'offerta. Le applicazioni saprebbero che si tratta di un'altra visualizzazione della stessa chiamata da parte del **membro dwCallID** in [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) che è uguale per entrambe le chiamate. Entrambe le chiamate sarebbero *inattive* quando la chiamata è stata eliminata. È possibile eliminare una chiamata dall'applicazione di terze parti eseguendo [**un'operazione lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) su uno degli handle di chiamata.

 

 



