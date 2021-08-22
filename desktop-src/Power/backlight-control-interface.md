---
description: L'interfaccia di controllo retroilluminazione è un'interfaccia IOCTL standardizzata per controllare la luminosità della retroilluminazione LCD.
ms.assetid: edf2b7ed-2676-483a-80ba-f148951e0e58
title: Interfaccia di controllo retroilluminazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18a6a82cede03d18f9d237bab09a590f9bcdc0da86651dacd0912357c32d36ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143724"
---
# <a name="backlight-control-interface"></a>Interfaccia di controllo retroilluminazione

L'interfaccia di controllo retroilluminazione è un'interfaccia IOCTL standardizzata per controllare la luminosità della retroilluminazione LCD.

Le applicazioni che richiedono il controllo a livello di codice della luminosità retroilluminazione o forniscono controlli per l'utente a tale scopo devono usare questa interfaccia anziché un'interfaccia proprietaria; In caso contrario, il sistema non può eseguire query sulla luminosità hardware corrente e potrebbe non essere sincronizzato.

Il primo passaggio consiste nell'eseguire una query sul dispositivo per la luminosità supportata usando il codice di controllo [**IOCTL \_ VIDEO QUERY SUPPORTED \_ \_ \_ BRIGHTNESS.**](ioctl-video-query-supported-brightness.md) Questa operazione restituisce un buffer che specifica i livelli di luminosità disponibili. Successivamente, è possibile eseguire una query sul dispositivo per la luminosità dello schermo corrente usando il codice di controllo [**IOCTL \_ VIDEO QUERY DISPLAY \_ \_ \_ BRIGHTNESS.**](ioctl-video-query-display-brightness.md) Questa operazione restituisce le impostazioni correnti per la luminosità corrente alternata (AC), la luminosità corrente diretta (DC) e lo stato di alimentazione.

Per modificare la luminosità dello schermo, usare il codice [**di controllo IOCTL \_ VIDEO SET DISPLAY \_ \_ \_ BRIGHTNESS.**](ioctl-video-set-display-brightness.md) È possibile impostare la luminosità ac, la luminosità del controller di dominio o entrambi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sul risparmio energia](about-power-management.md)
</dt> </dl>

 

 



