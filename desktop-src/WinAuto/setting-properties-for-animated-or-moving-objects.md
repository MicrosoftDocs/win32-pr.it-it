---
title: Impostazione delle proprietà per gli oggetti animati o mobili
description: Per i controlli di animazione, ad esempio il controllo dell'animazione visualizzato durante la copia dei file, usare il \_ ruolo dell'oggetto animazione del sistema di ruoli \_ .
ms.assetid: 8c5ebbc3-4066-452b-8f37-2fb595adea53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1551899305968471bf1425b5cc043be8329c2bd4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045175"
---
# <a name="setting-properties-for-animated-or-moving-objects"></a>Impostazione delle proprietà per gli oggetti animati o mobili

Per i controlli di animazione, ad esempio il controllo dell'animazione visualizzato durante la copia dei file, usare il ruolo dell'oggetto [**\_ \_ animazione del sistema di ruoli**](object-roles.md) . Per gli elementi grafici a cui è [**stata**](state-property.md) aggiunta un'animazione occasionale, usare il ruolo di oggetto [**grafico del \_ sistema \_ di ruolo**](object-roles.md) con lo stato impostato su [**stato \_ \_ animato**](object-state-constants.md).

Usare il [**flag \_ \_ animato del sistema di stato**](object-state-constants.md) per contrassegnare un oggetto il cui aspetto viene modificato rapidamente. I client utilizzano questo flag per evitare di inviare ripetutamente agli utenti una singola serie di modifiche visive.

Un esempio è il testo Marquee, che viene divulgato progressivamente mentre scorre sullo schermo. A tali oggetti viene assegnato l'attributo [**del \_ sistema di stato \_ animato**](object-state-constants.md). Nella maggior parte dei casi, la stringa [**valore**](value-property.md) dell'oggetto riflette l'intero testo, anche la parte attualmente non visibile. Non è consigliabile modificare spesso la stringa del **valore** in modo che corrisponda al testo attualmente visibile perché comporta un numero eccessivo di eventi [**\_ \_ VALUECHANGE di oggetti evento**](event-constants.md) che non contengono informazioni utili.

Ad esempio, in una finestra contenente un'area rettangolare che mostra la parola "Yes!" lo spostamento in un modello figura-otto, il [**ruolo**](role-property.md) è un [**\_ \_ elemento grafico del sistema di ruoli**](object-roles.md), la proprietà [**value**](value-property.md) è la stringa visualizzata, la proprietà [**location**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) è il rettangolo delimitatore attorno al testo e il flag di attributo [**\_ \_ animato del sistema di stato**](object-state-constants.md) è impostato. La [**Descrizione**](description-property.md) è "The Word ' Yes!' si sposta intorno allo schermo in un modello figura-otto ". Il server genera solo [**eventi \_ \_ STATECHANGE di oggetti evento**](event-constants.md) quando l'oggetto viene avviato o cessa l'animazione.

 

 




