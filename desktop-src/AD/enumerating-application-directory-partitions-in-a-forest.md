---
title: Enumerazione delle partizioni di directory applicative in una foresta
description: Analogamente alle partizioni di dominio, ogni partizione di directory applicativa è rappresentata da un oggetto crossRef nel contenitore Partizioni della partizione di configurazione.
ms.assetid: dd1ff72d-ed19-4e8c-a401-a5b1b3d577e8
ms.tgt_platform: multiple
keywords:
- Enumerazione delle partizioni di directory applicative in una foresta AD
- Partizioni di directory applicative AD , enumerazione in una foresta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c4e8d48b2fc93ad7a879f76f2bbaa130186706ef957320612c866cb3b9f892c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191368"
---
# <a name="enumerating-application-directory-partitions-in-a-forest"></a>Enumerazione delle partizioni di directory applicative in una foresta

Analogamente alle partizioni di dominio, ogni partizione di directory applicativa è rappresentata da un [**oggetto crossRef**](/windows/desktop/ADSchema/c-crossref) nel contenitore Partizioni della partizione di configurazione. Ogni **oggetto crossRef** archivia i dati relativi alla partizione corrispondente.

Un [**oggetto crossRef**](/windows/desktop/ADSchema/c-crossref) che rappresenta una partizione di dominio viene distinto da un oggetto **crossRef** che rappresenta una partizione di directory applicativa in base al contenuto dell'attributo [**systemFlags.**](/windows/desktop/ADSchema/a-systemflags) L'oggetto **crossRef** che rappresenta una partizione di dominio avrà entrambi i flag [**ADS \_ SYSTEMFLAG \_ CR \_ NTDS \_ NC**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum) e **ADS \_ SYSTEMFLAG \_ CR \_ NTDS \_ DOMAIN** impostati nell'attributo **systemFlags.** L'oggetto **crossRef** che rappresenta una partizione di directory applicativa avrà il flag **NC ADS \_ SYSTEMFLAG \_ CR \_ NTDS \_** impostato e il flag **ADS \_ SYSTEMFLAG \_ CR \_ NTDS \_ DOMAIN** non verrà impostato nell'attributo **systemFlags.**

Per gli oggetti [**crossRef**](/windows/desktop/ADSchema/c-crossref) che rappresentano le partizioni schema e di configurazione sarà impostato anche il flag [**NC ADS \_ SYSTEMFLAG \_ CR \_ NTDS \_**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum) e il flag **ADS \_ SYSTEMFLAG \_ CR \_ NTDS \_ DOMAIN** non verrà impostato nell'attributo [**systemFlags.**](/windows/desktop/ADSchema/a-systemflags) Ciò richiede che questi due **oggetti crossRef** siano distinti in base al contenuto dell'attributo [**nCName.**](/windows/desktop/ADSchema/a-ncname) **L'attributo nCName** per l'oggetto **crossRef** che rappresenta il contenitore Schema sarà identico all'attributo **schemaNamingContext** dell'oggetto RootDSE. Analogamente, **l'attributo nCName** per l'oggetto **crossRef** che rappresenta il contenitore Configuration sarà identico all'attributo **configurationNamingContext** dell'oggetto RootDSE.

**Per identificare tutte le partizioni di directory applicative in una foresta, seguire questa procedura**

1.  Nel contenitore Partizioni della partizione di configurazione cercare o enumerare tutti gli [**oggetti crossRef.**](/windows/desktop/ADSchema/c-crossref)
2.  Se per un oggetto [**crossRef**](/windows/desktop/ADSchema/c-crossref) non è impostato il flag [**NC ADS \_ SYSTEMFLAG \_ CR \_ NTDS \_**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum) o il flag **ADS \_ SYSTEMFLAG \_ CR \_ NTDS \_ DOMAIN** è impostato nel valore dell'attributo [**systemFlags,**](/windows/desktop/ADSchema/a-systemflags) escludere l'oggetto dal set di risultati.
3.  Escludere la partizione dello schema dal set di risultati confrontando l'attributo [**nCName**](/windows/desktop/ADSchema/a-ncname) dell'oggetto [**crossRef**](/windows/desktop/ADSchema/c-crossref) con l'attributo **schemaNamingContext** dell'oggetto RootDSE.
4.  Escludere la partizione di configurazione dal set di risultati confrontando l'attributo [**nCName**](/windows/desktop/ADSchema/a-ncname) dell'oggetto [**crossRef**](/windows/desktop/ADSchema/c-crossref) con l'attributo **configurationNamingContext** dell'oggetto RootDSE.
5.  Gli oggetti [**crossRef rimanenti**](/windows/desktop/ADSchema/c-crossref) nel set di risultati rappresentano tutte le partizioni di directory dell'applicazione.

 

 