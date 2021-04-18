---
title: Proprietà Role
description: La proprietà Role descrive l'elemento dell'interfaccia utente di un oggetto. Tutti gli oggetti supportano la proprietà Role.
ms.assetid: f6abf95b-a77a-406d-9ca0-4663adc8245f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f2b285d9242542f83c6b4478df93e888a7a23cd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297902"
---
# <a name="role-property"></a>Proprietà Role

La proprietà **Role** descrive l'elemento dell'interfaccia utente di un oggetto. Tutti gli oggetti supportano la proprietà **Role** .

In molti casi, il ruolo dell'oggetto è ovvio. Ad esempio, Windows ha il [**ruolo \_ \_ finestra del sistema ruolo**](object-roles.md) e i pulsanti di push hanno il ruolo [**\_ \_ pulsante sistema ruolo**](object-roles.md) .

La proprietà **Role** viene recuperata chiamando [**IAccessible:: Get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole).

## <a name="identifying-an-objects-role"></a>Identificazione del ruolo di un oggetto

Microsoft Active Accessibility fornisce [costanti Role](object-roles.md), definite in oleacc. h, che identificano i ruoli comuni degli oggetti. È consigliabile che gli sviluppatori di server usino questi valori di ruolo predefiniti. Se viene restituita una costante di ruolo predefinita, i client usano la funzione [**GetRoleText**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta) per recuperare una stringa localizzata che descrive il ruolo.

Per i controlli di animazione, ad esempio il controllo dell'animazione visualizzato durante la copia dei file, usare l' [**\_ \_ animazione del sistema del ruolo**](object-roles.md). Le immagini talvolta animate vengono descritte come [**\_ \_ Immagini del sistema di ruolo**](object-roles.md) con la proprietà [**stato**](state-property.md) impostata su [**stato del \_ sistema \_ animato**](object-state-constants.md).

Si noti che alcuni ruoli non sono facili da descrivere. Ad esempio, la visualizzazione icone grandi di una cartella consente la disposizione arbitraria delle icone, quindi il suo ruolo può essere descritto come [**\_ \_ raggruppamento del sistema di ruoli**](object-roles.md). In alternativa, un controllo che fornisce elementi in righe e colonne fisse potrebbe avere il ruolo di [**\_ \_ tabella del sistema Role**](object-roles.md) . Poiché un ruolo viene utilizzato per comunicare il modello di utilizzo a un utente finale, è importante utilizzare il ruolo appropriato. Ad esempio, se il controllo funziona come un pulsante, usare il pulsante del [**sistema di ruolo \_ \_**](object-roles.md).

 

 




