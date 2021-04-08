---
description: Le applicazioni possono restare in ascolto di eventi di sistema utilizzando l'oggetto InkCollector e in ascolto dell'evento SystemGesture.
ms.assetid: 141afdbe-b5a7-47dc-b505-46089a5eda75
title: Ascolto degli eventi di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1429e652140cc9624d324401edef7817dad40ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058284"
---
# <a name="listening-to-system-events"></a>Ascolto degli eventi di sistema

Le applicazioni possono restare in ascolto di eventi di sistema utilizzando l'oggetto [**InkCollector**](inkcollector-class.md) e in ascolto dell'evento [**SystemGesture**](inkcollector-systemgesture.md) . È possibile impostare gli eventi a cui un'applicazione è in ascolto. Quando si verifica un'azione della penna del tablet, l'evento **SystemGesture** corrispondente viene inviato all'applicazione nell'oggetto **InkCollector** . Un'applicazione può annullare il messaggio del mouse corrispondente a un evento **SystemGesture** specificato quando riceve l'evento. Per informazioni dettagliate sull'annullamento dei messaggi del mouse, vedere evento **SystemGesture** .

 

 



