---
description: Le applicazioni possono restare in ascolto degli eventi di sistema usando l'oggetto InkCollector e restare in ascolto dell'evento SystemGesture su di esso.
ms.assetid: 141afdbe-b5a7-47dc-b505-46089a5eda75
title: Ascolto di eventi di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a02d9d5ae20ac70e648071dfef904cb1ac7983c79c4aca3b02309ce1d20ac52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119031819"
---
# <a name="listening-to-system-events"></a>Ascolto di eventi di sistema

Le applicazioni possono restare in ascolto degli eventi di sistema [**usando l'oggetto InkCollector**](inkcollector-class.md) e restare in ascolto [**dell'evento SystemGesture**](inkcollector-systemgesture.md) su di esso. È possibile impostare gli eventi a cui un'applicazione è in ascolto. Quando si verifica un'azione della penna del tablet, **l'evento SystemGesture** corrispondente viene inviato all'applicazione sul relativo **oggetto InkCollector.** Un'applicazione può annullare il messaggio del mouse che corrisponde a un determinato **evento SystemGesture** quando riceve l'evento. Per informazioni dettagliate sull'annullamento dei messaggi del mouse, vedere **Evento SystemGesture.**

 

 



