---
title: Archiviazione permanente sul server
description: È possibile ottimizzare l'applicazione in modo che lo stub del server non liberi la memoria sul server al termine di una chiamata di procedura remota.
ms.assetid: 340334e2-94ac-4be2-a16d-38bc4c64e7db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7237fe6136918e5495ee1f22bac0991d71c5dbf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955651"
---
# <a name="persistent-storage-on-the-server"></a>Archiviazione permanente sul server

È possibile ottimizzare l'applicazione in modo che lo stub del server non liberi la memoria sul server al termine di una chiamata di procedura remota. Ad esempio, quando un handle di contesto verrà modificato da diverse procedure remote, è possibile usare l'attributo ACF **\[ allocate (non \_ gratuito) \]** per mantenere la memoria allocata sul server.

L'attributo **\[ allocate (Not \_ free) \]** viene aggiunto alla Dichiarazione **typedef** di ACF in ACF. Ad esempio:

``` syntax
/* ACF file fragment */
typedef [allocate(all_nodes, dont_free)] P_TREE_TYPE;
```

Quando si specifica l'attributo **\[ allocate (non \_ gratuito) \]** , la struttura dei dati dell'albero viene allocata, ma non liberata, dallo stub del server. Quando si rendono i puntatori a tali aree dati persistenti disponibili ad altre routine, ad esempio copiando i puntatori in variabili globali, i dati conservati sono accessibili ad altre funzioni server. L'attributo **\[ allocate (non \_ gratuito) \]** è particolarmente utile per la gestione di strutture di puntatore permanenti come parte delle informazioni sullo stato del server associate a un tipo di handle di contesto.

 

 




