---
title: Proprietà Role
description: La proprietà Role descrive l'elemento dell'interfaccia utente di un oggetto. Tutti gli oggetti supportano la proprietà Role.
ms.assetid: f6abf95b-a77a-406d-9ca0-4663adc8245f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2881b301537e9a25dabb260b84bc889cef4e4a6f9f6a5a2c8fab540d78daf8c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133724"
---
# <a name="role-property"></a>Proprietà Role

La **proprietà Role** descrive l'elemento dell'interfaccia utente di un oggetto. Tutti gli oggetti supportano **la proprietà** Role.

In molti casi, il ruolo dell'oggetto è ovvio. Ad esempio, le finestre hanno il [**ruolo ROLE SYSTEM WINDOW \_ \_ e**](object-roles.md) i pulsanti di comando hanno il [**ruolo ROLE SYSTEM \_ \_ PUSHBUTTON.**](object-roles.md)

La **proprietà Role** viene recuperata chiamando [**IAccessible::get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole).

## <a name="identifying-an-objects-role"></a>Identificazione del ruolo di un oggetto

Microsoft Active Accessibility fornisce [costanti di ruolo](object-roles.md), definite in oleacc.h, che identificano i ruoli oggetto comuni. È consigliabile che gli sviluppatori di server usino questi valori di ruolo predefiniti. Se viene restituita una costante di ruolo predefinita, i client usano la [**funzione GetRoleText**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta) per recuperare una stringa localizzata che descrive il ruolo.

Per i controlli di animazione, ad esempio il controllo di animazione visualizzato durante la copia dei file, usare [**ROLE \_ SYSTEM \_ ANIMATION.**](object-roles.md) Gli elementi grafici a cui viene talvolta animata l'animazione vengono descritti come [**ROLE \_ SYSTEM \_ GRAPHIC**](object-roles.md) con la [**proprietà State**](state-property.md) impostata su STATE [**SYSTEM \_ \_ ANIMATED.**](object-state-constants.md)

Si noti che alcuni ruoli non sono facili da descrivere. Ad esempio, la visualizzazione icone grandi di una cartella consente la disposizione arbitraria delle icone, quindi il suo ruolo può essere descritto come [**ROLE \_ SYSTEM \_ GROUPING**](object-roles.md). Oppure, un controllo che fornisce elementi in righe e colonne fisse può avere il [**ruolo ROLE \_ SYSTEM \_ TABLE.**](object-roles.md) Poiché un ruolo viene usato per comunicare il modello di utilizzo a un utente finale, è importante usare il ruolo appropriato. Ad esempio, se il controllo funge da pulsante, usare [**ROLE \_ SYSTEM \_ PUSHBUTTON**](object-roles.md).

 

 




