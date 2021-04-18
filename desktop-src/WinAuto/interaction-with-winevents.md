---
title: Interazione con WinEvents
description: Il tempo di esecuzione dell'annotazione dinamica non invierà WinEvents; è responsabilità dell'annotatore inviare gli eventi appropriati, quando necessario. Se è necessario inviare WinEvents, assicurarsi di inviarli dopo aver eseguito l'annotazione.
ms.assetid: 657a540b-8838-4d2e-ade6-c4fa1ad08e21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2aedd09a22371f91a92eca891c77f6c424583b5
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "106299343"
---
# <a name="interaction-with-winevents"></a>Interazione con WinEvents

Il tempo di esecuzione dell'annotazione dinamica non invierà [winEvents](winevents-infrastructure.md); è responsabilità dell'annotatore inviare gli eventi appropriati, quando necessario. Se è necessario inviare WinEvents, assicurarsi di inviarli dopo aver eseguito l'annotazione.

Se ad esempio si usa [**IAccPropServices:: SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) per impostare la proprietà [**Name**](name-property.md) di un elemento, inviare un evento [**\_ \_ NAMECHANGE dell'oggetto evento**](event-constants.md) per quell'oggetto dopo la restituzione di **SetPropValue** .

Tuttavia, se si usa [**IAccPropServices:: SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) per impostare ValueMap per un dispositivo di scorrimento, non è necessario alcun evento perché l'impostazione di ValueMap non comporta la modifica del valore del dispositivo di scorrimento.

 

 




