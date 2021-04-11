---
title: Enumerazione delle repliche di una partizione di directory applicativa
description: In questo argomento viene illustrato come enumerare le repliche per una partizione di directory applicativa.
ms.assetid: a1d6865b-ec77-4687-9da7-7fc717568bda
ms.tgt_platform: multiple
keywords:
- Enumerazione delle repliche di una partizione di directory applicativa AD
- Directory dell'applicazione partizioni di Active Directory, enumerazione delle repliche di
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1415c147fe4320e5f8169487a656db4f365f03a
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103956335"
---
# <a name="enumerating-replicas-of-an-application-directory-partition"></a>Enumerazione delle repliche di una partizione di directory applicativa

Quando viene aggiunta una replica di una partizione di directory applicativa, il nome distinto dell'oggetto [**NTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) per il controller di dominio che conterrà la replica viene aggiunto all'attributo [**msDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) dell'oggetto [**crossRef**](/windows/desktop/ADSchema/c-crossref) . L'oggetto **crossRef** usato rappresenta la partizione di directory applicativa.

**Per enumerare le repliche per una partizione di directory applicativa**

1.  Cercare nel contenitore partizioni un oggetto [**crossRef**](/windows/desktop/ADSchema/c-crossref) con un valore di attributo [**NCName**](/windows/desktop/ADSchema/a-ncname) uguale al nome distinto della partizione di directory applicativa.
2.  Utilizzare ogni valore dell'attributo [**msDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) dell'oggetto [**crossRef**](/windows/desktop/ADSchema/c-crossref) per eseguire l'associazione all'oggetto [**NTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) del server.
3.  Ottenere ADsPath per l'elemento padre di ogni oggetto [**NTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) . Si tratta di un oggetto che rappresenta il server del controller di dominio. Usare ADsPath per eseguire l'associazione all'oggetto server.
4.  Ottenere il valore dell'attributo [**dNSHostName**](/windows/desktop/ADSchema/a-dnshostname) dell'oggetto server. Si tratta di una proprietà a valore singolo che contiene il nome DNS del server.

A causa della latenza di replica e dei ritardi di esecuzione pianificata di KCC, è possibile che le repliche attive effettive per una partizione di directory applicativa non corrispondano all'elenco dei controller di dominio indicati dall'attributo [**msDS-NC-Replication-locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) dell'oggetto [**crossRef**](/windows/desktop/ADSchema/c-crossref) . Un modo più accurato, ma meno efficace per determinare le repliche attive effettive di una partizione di directory applicativa consiste nel cercare tutti gli oggetti [**NTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) nella foresta che includono un attributo [**msDS-hasMasterNCs**](/windows/desktop/ADSchema/a-msds-hasmasterncs) che contiene il nome distinto della partizione di directory applicativa. L'attributo **msDS-hasMasterNCs** contiene i nomi distinti di tutte le partizioni di directory scrivibili che il controller di dominio ospita, incluse le partizioni di directory applicative.

 

 