---
title: Progetto personalizzato
description: Il progetto personalizzato non è un controllo comune; si tratta di un servizio che molti controlli comuni forniscono.
ms.assetid: vs|controls|~\controls\custdraw\custdraw.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5184d06dbb8e04185bf12a43c6c71dd96b933a6a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955271"
---
# <a name="custom-draw"></a>Progetto personalizzato

Il progetto personalizzato non è un controllo comune; si tratta di un servizio che molti controlli comuni forniscono. Il servizio di personalizzazione personalizzato consente a un'applicazione una maggiore flessibilità nella personalizzazione dell'aspetto di un controllo. L'applicazione può sfruttare le notifiche di traccia personalizzate per modificare facilmente il tipo di carattere usato per visualizzare gli elementi o per tracciare manualmente un elemento senza dover eseguire un Owner Draw completo.

Questa sezione contiene informazioni sugli elementi di programmazione usati con il progetto personalizzato.

## <a name="overviews"></a>Cenni preliminari



| Argomento                                      | Contenuto                                                                                                                                                               |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informazioni sul progetto personalizzato](about-custom-draw.md) | Questa sezione contiene informazioni generali sulla funzionalità di personalizzazione personalizzata e fornisce una panoramica concettuale del modo in cui un'applicazione può supportare il progetto personalizzato.<br/> |
| [Uso di un progetto personalizzato](using-custom-draw.md) | Questa sezione contiene esempi che illustrano come implementare un progetto personalizzato. <br/>                                                                              |



 

## <a name="notifications"></a>Notifiche



| Argomento                               | Contenuto                                                                                                                                                                 |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_CUSTOMDRAW Nm](nm-customdraw.md) | Notifica alla finestra padre di un controllo informazioni sulle operazioni di disegno personalizzate. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) . <br/> |



 

## <a name="structures"></a>Strutture



| Argomento                                | Contenuto                                                                                              |
|--------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) | Contiene informazioni specifiche di un codice di notifica [ \_ CUSTOMDRAW Nm](nm-customdraw.md) .<br/> |



 

 

 





