---
description: Non è possibile creare istanze delle classi modificate nello spazio dei nomi localizzato. Le classi modificate nello spazio dei nomi localizzato vengono considerate come astratte anche se non contengono il qualificatore Abstract.
ms.assetid: a0583153-f5d2-4f4c-ab2e-6ec468e665c7
ms.tgt_platform: multiple
title: Considerazioni sulle classi modificate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30cd38bc6134c4fd3596cc36e8a7638eaa1fd6ed264c90302d921a391982e5d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118320241"
---
# <a name="amended-class-considerations"></a>Considerazioni sulle classi modificate

Non è possibile creare istanze delle classi modificate nello spazio dei nomi localizzato. Le classi modificate nello spazio dei nomi localizzato vengono considerate come astratte anche se non contengono il [**qualificatore Abstract.**](standard-qualifiers.md)

Se si recupera una classe modificata da uno spazio dei nomi localizzato usando il flag WBEM \_ FLAG \_ USE \_ AMENDED QUALIFIERS e si genera un'istanza da essa, l'istanza contiene tutti i qualificatori modificati della classe \_ modificata. Non è possibile archiviare questa nuova classe nello spazio dei nomi che contiene la definizione di classe di base a meno che non si esega l'operazione **put** con il flag WBEM \_ FLAG USE \_ \_ AMENDED \_ QUALIFIERS. Questo flag indica a WMI di rimuovere tutti i qualificatori modificati prima di salvare l'oggetto. Se non si specifica WBEM FLAG USE AMENDED QUALIFIERS, l'operazione put ha esito negativo con un \_ \_ errore \_ \_ WBEM E  \_ \_ AMENDED \_ OBJECT.

 

 



