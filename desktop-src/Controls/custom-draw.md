---
title: Disegno personalizzato
description: Il disegno personalizzato non è un controllo comune. è un servizio fornito da molti controlli comuni.
ms.assetid: vs|controls|~\controls\custdraw\custdraw.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16271e915a942e21f3f3763237a25c37a8b934fc1a44a016bb7e3938491a3c66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118413179"
---
# <a name="custom-draw"></a>Disegno personalizzato

Il disegno personalizzato non è un controllo comune. è un servizio fornito da molti controlli comuni. Il servizio di disegno personalizzato consente a un'applicazione una maggiore flessibilità nella personalizzazione dell'aspetto di un controllo. L'applicazione può sfruttare le notifiche di disegno personalizzate per modificare facilmente il tipo di carattere usato per visualizzare gli elementi o disegnare manualmente un elemento senza dover eseguire un disegno completo del proprietario.

Questa sezione contiene informazioni sugli elementi di programmazione usati con il disegno personalizzato.

## <a name="overviews"></a>Cenni preliminari



| Argomento                                      | Contenuto                                                                                                                                                               |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informazioni sul disegno personalizzato](about-custom-draw.md) | Questa sezione contiene informazioni generali sulla funzionalità di disegno personalizzato e offre una panoramica concettuale del modo in cui un'applicazione può supportare il disegno personalizzato.<br/> |
| [Uso del disegno personalizzato](using-custom-draw.md) | Questa sezione contiene esempi che illustrano come implementare il disegno personalizzato. <br/>                                                                              |



 

## <a name="notifications"></a>Notifiche



| Argomento                               | Contenuto                                                                                                                                                                 |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NM \_ CUSTOMDRAW](nm-customdraw.md) | Notifica alla finestra padre di un controllo le operazioni di disegno personalizzate. Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md) <br/> |



 

## <a name="structures"></a>Strutture



| Argomento                                | Contenuto                                                                                              |
|--------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) | Contiene informazioni specifiche di un [codice di notifica NM \_ CUSTOMDRAW.](nm-customdraw.md)<br/> |



 

 

 





