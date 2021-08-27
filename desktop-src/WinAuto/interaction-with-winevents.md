---
title: Interazione con WinEvents
description: La fase di esecuzione dell'annotazione dinamica non invierà WinEvent. è responsabilità dell'annotatore inviare gli eventi appropriati, quando necessario. Se è necessario inviare WinEvent, assicurarsi di inviarli dopo che l'annotazione è stata eseguita.
ms.assetid: 657a540b-8838-4d2e-ade6-c4fa1ad08e21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df1789a152ab37161e1f217639e4ad40d597b0689529da3a5f65bf669b986e14
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098461"
---
# <a name="interaction-with-winevents"></a>Interazione con WinEvents

La fase di esecuzione dell'annotazione dinamica non [invierà WinEvents;](winevents-infrastructure.md) è responsabilità dell'annotatore inviare gli eventi appropriati, quando necessario. Se è necessario inviare WinEvent, assicurarsi di inviarli dopo che l'annotazione è stata eseguita.

Ad esempio, se si usa [**IAccPropServices::SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) per impostare la proprietà [**Name**](name-property.md) di un elemento, inviare un evento [**EVENT OBJECT \_ \_ NAMECHANGE**](event-constants.md) per tale oggetto dopo il ritorno **di SetPropValue.**

Tuttavia, se si usa [**IAccPropServices::SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) per impostare ValueMap per un dispositivo di scorrimento, non è necessario alcun evento perché l'impostazione di ValueMap non modifica il valore del dispositivo di scorrimento.

 

 




