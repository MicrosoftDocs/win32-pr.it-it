---
description: Non è possibile creare istanze delle classi modificate nello spazio dei nomi localizzato. Le classi modificate nello spazio dei nomi localizzato vengono considerate come se fossero astratte, sebbene non contengano il qualificatore astratto.
ms.assetid: a0583153-f5d2-4f4c-ab2e-6ec468e665c7
ms.tgt_platform: multiple
title: Considerazioni sulle classi modificate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f77a2caa315ab4878fe619c13c69bd5d2e1a2610
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234320"
---
# <a name="amended-class-considerations"></a>Considerazioni sulle classi modificate

Non è possibile creare istanze delle classi modificate nello spazio dei nomi localizzato. Le classi modificate nello spazio dei nomi localizzato vengono considerate come se fossero astratte, sebbene non contengano il qualificatore [**astratto**](standard-qualifiers.md) .

Se si recupera una classe modificata da uno spazio dei nomi localizzato usando il flag WBEM \_ \_ , usare il \_ flag dei \_ qualificatori modificati e generare un'istanza da essa, l'istanza contiene tutti i qualificatori modificati della classe modificata. Non è possibile archiviare questa nuova classe nello spazio dei nomi che contiene la definizione di classe di base, a meno che non si esegua l'operazione **put** con il flag WBEM \_ usare il flag dei \_ \_ \_ qualificatori modificati. Questo flag indica a WMI di eliminare tutti i qualificatori modificati prima di salvare l'oggetto. Se non si specifica \_ il flag WBEM \_ usare \_ \_ i qualificatori modificati, l'operazione **put** ha esito negativo con un errore di \_ oggetto WBEM E \_ modificato \_ .

 

 



