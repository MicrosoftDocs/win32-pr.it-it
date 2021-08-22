---
title: Enumerazione delle repliche di una partizione di directory applicativa
description: In questo argomento viene illustrato come enumerare le repliche per una partizione di directory applicativa.
ms.assetid: a1d6865b-ec77-4687-9da7-7fc717568bda
ms.tgt_platform: multiple
keywords:
- Enumerazione delle repliche di una partizione di directory applicativa AD
- Partizioni di directory applicative AD , enumerazione delle repliche di
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b52ff0ea5c2b4737079f4a44997f39dd027299f50c8acd96fe0456b0e5b60d03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118694888"
---
# <a name="enumerating-replicas-of-an-application-directory-partition"></a>Enumerazione delle repliche di una partizione di directory applicativa

Quando viene aggiunta una replica di una partizione di directory applicativa, il nome distinto dell'oggetto [**nTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) per il controller di dominio che conterrà la replica viene aggiunto all'attributo [**msDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) [**dell'oggetto crossRef.**](/windows/desktop/ADSchema/c-crossref) **L'oggetto crossRef** usato rappresenta la partizione di directory applicativa.

**Per enumerare le repliche per una partizione di directory applicativa**

1.  Cercare nel contenitore Partizioni un oggetto [**crossRef**](/windows/desktop/ADSchema/c-crossref) con un valore di [**attributo nCName**](/windows/desktop/ADSchema/a-ncname) uguale al nome distinto della partizione di directory applicativa.
2.  Usare ogni valore [**dell'attributo msDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) dell'oggetto [**crossRef**](/windows/desktop/ADSchema/c-crossref) per l'associazione all'oggetto [**nTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) del server.
3.  Ottenere ADsPath per l'elemento padre di [**ogni oggetto nTDSDSA.**](/windows/desktop/ADSchema/c-ntdsdsa) Si tratta di un oggetto che rappresenta il server controller di dominio. Usare ADsPath per eseguire l'associazione all'oggetto server.
4.  Ottenere il [**valore dell'attributo dNSHostName**](/windows/desktop/ADSchema/a-dnshostname) dell'oggetto server. Si tratta di una proprietà a valore singolo che contiene il nome DNS del server.

A causa della latenza di replica e dei ritardi di esecuzione KCC pianificati, è possibile che le repliche attive effettive per una partizione di directory applicativa non corrispondano all'elenco di controller di dominio indicato dall'attributo [**msDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) [**dell'oggetto crossRef.**](/windows/desktop/ADSchema/c-crossref) Un modo più accurato, ma meno efficiente per determinare le repliche attive effettive di una partizione di directory applicativa è cercare tutti gli oggetti [**nTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) nella foresta che dispongono di un attributo [**msDS-hasMasterNCs**](/windows/desktop/ADSchema/a-msds-hasmasterncs) che contiene il nome distinto della partizione di directory applicativa. **L'attributo msDS-hasMasterNCs** contiene i nomi distinti di tutte le partizioni di directory scrivibili ospitate dal controller di dominio, incluse le partizioni di directory applicative.

 

 