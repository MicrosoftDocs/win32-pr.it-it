---
title: Data binding
description: Data binding
ms.assetid: 7fc5f036-8b36-4e0e-a257-173010fe127a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c2040aa29c83615f42c321483c87be378737dcdef47e43873fbe3b8c0902dd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048369"
---
# <a name="databinding"></a>Data binding

È stato aggiunto un nuovo attributo di databinding per consentire alle proprietà di distinguere tra la comunicazione delle modifiche solo quando lo stato attivo lascia il controllo o durante tutte le notifiche di modifica delle proprietà.

Il nuovo attributo, noto come ImmediateBind, consente ai controlli di distinguere due diversi tipi di proprietà associabili. Un tipo di proprietà associabile deve notificare ogni modifica al database, ad esempio con un controllo casella di controllo in cui ogni modifica deve essere inviata al database sottostante anche se il controllo non ha perso lo stato attivo. Tuttavia, i controlli, ad esempio una casella di riepilogo, vogliono ricevere una notifica di modifica di una proprietà al database solo quando il controllo perde lo stato attivo, poiché l'utente potrebbe aver modificato la selezione evidenziata con i tasti di direzione prima di trovare l'impostazione desiderata, in modo che la notifica di modifica venga inviata al database ogni volta che l'utente preme il tasto di direzione. La nuova proprietà di associazione immediata consente alle singole proprietà associabili in un form di avere questo comportamento specificato, quando questo bit è impostato verranno notificate tutte le modifiche.

Il nuovo bit ImmediateBind esegue il mapping ai nuovi bit VARFLAG \_ FIMMEDIATEBIND (0x80) e FUNCFLAG \_ FIMMEDIATEBIND (0x80) nelle enumerazioni VARFLAGS e FUNCFLAGS per l'interfaccia [ITypeInfo](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) che consentono di controllare gli attributi delle proprietà.

 

 