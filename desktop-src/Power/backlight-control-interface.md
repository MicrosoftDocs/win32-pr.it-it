---
description: L'interfaccia di controllo della retroilluminazione è un'interfaccia IOCTL standardizzata per il controllo della luminosità della retroilluminazione LCD.
ms.assetid: edf2b7ed-2676-483a-80ba-f148951e0e58
title: Interfaccia di controllo retroilluminazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ecbcc3d635d120c1049f8ec586d7296a953dfac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312068"
---
# <a name="backlight-control-interface"></a>Interfaccia di controllo retroilluminazione

L'interfaccia di controllo della retroilluminazione è un'interfaccia IOCTL standardizzata per il controllo della luminosità della retroilluminazione LCD.

Le applicazioni che richiedono il controllo a livello di codice della luminosità della retroilluminazione o forniscono controlli per l'utente devono usare questa interfaccia anziché un'interfaccia proprietaria; in caso contrario, il sistema non è in grado di eseguire query sulla luminosità hardware corrente e potrebbe non essere sincronizzato.

Il primo passaggio consiste nell'eseguire una query sul dispositivo per la luminosità supportata usando il codice di controllo della [**\_ \_ \_ \_ luminosità supportato dalla query video IOCTL**](ioctl-video-query-supported-brightness.md) . Questa operazione restituisce un buffer che specifica i livelli di luminosità disponibili. Successivamente, è possibile eseguire una query sul dispositivo per la luminosità di visualizzazione corrente usando il codice di controllo della [**\_ \_ \_ \_ luminosità della query video IOCTL**](ioctl-video-query-display-brightness.md) . Questa operazione restituisce le impostazioni correnti per la luminosità corrente alternata (CA), la luminosità diretta corrente (DC) e lo stato di alimentazione.

Per modificare la luminosità dello schermo, usare il codice di controllo della [**\_ \_ \_ \_ luminosità del set di video IOCTL**](ioctl-video-set-display-brightness.md) . È possibile impostare la luminosità AC, la luminosità del controller di dominio o entrambi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sul risparmio energia](about-power-management.md)
</dt> </dl>

 

 



