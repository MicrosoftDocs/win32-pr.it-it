---
title: Enumerazione delle partizioni di directory applicative in una foresta
description: Analogamente alle partizioni di dominio, ogni partizione di directory applicativa viene rappresentata da un oggetto crossRef nel contenitore partizioni della partizione di configurazione.
ms.assetid: dd1ff72d-ed19-4e8c-a401-a5b1b3d577e8
ms.tgt_platform: multiple
keywords:
- Enumerazione delle partizioni di directory applicative in una foresta AD
- Directory dell'applicazione partizioni di Active Directory, enumerazione in una foresta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d42bbe28ef37932394721d0c234ba3970ac263b
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046515"
---
# <a name="enumerating-application-directory-partitions-in-a-forest"></a>Enumerazione delle partizioni di directory applicative in una foresta

Analogamente alle partizioni di dominio, ogni partizione di directory applicativa viene rappresentata da un oggetto [**crossRef**](/windows/desktop/ADSchema/c-crossref) nel contenitore partizioni della partizione di configurazione. Ogni oggetto **crossRef** archivia i dati sulla partizione corrispondente.

Un oggetto [**crossRef**](/windows/desktop/ADSchema/c-crossref) che rappresenta una partizione di dominio si distingue da un oggetto **crossRef** che rappresenta una partizione di directory applicativa in base al contenuto dell'attributo [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) . L'oggetto **crossRef** che rappresenta una partizione di dominio avrà entrambi i flag di **\_ \_ \_ \_ dominio NTDS** di [**Ads \_ SYSTEMFLAG \_ CR \_ NTDS \_ NC**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum) e ADS SYSTEMFLAG CR impostati nell'attributo **systemFlags** . L'oggetto **crossRef** che rappresenta una partizione di directory applicativa avrà il flag **\_ SYSTEMFLAG \_ CR \_ NTDS \_ NC** set e il flag di **\_ \_ \_ \_ dominio NTDS SYSTEMFLAG CR ADS** non verrà impostato nell'attributo **systemFlags** .

Gli oggetti [**crossRef**](/windows/desktop/ADSchema/c-crossref) che rappresentano le partizioni dello schema e della configurazione avranno anche il flag del controller di dominio con [**Ads \_ SYSTEMFLAG \_ CR \_ NTDS \_**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum) impostato e il flag di **\_ \_ \_ \_ dominio NTDS di ADS SYSTEMFLAG CR** non verrà impostato nell'attributo [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) . Questa operazione richiede che questi due oggetti **crossRef** siano distinti dal contenuto dell'attributo [**NCName**](/windows/desktop/ADSchema/a-ncname) . L'attributo **NCName** per l'oggetto **crossRef** che rappresenta il contenitore dello schema sarà identico all'attributo **schemaNamingContext** dell'oggetto RootDSE. Analogamente, l'attributo **NCName** per l'oggetto **crossRef** che rappresenta il contenitore di configurazione sarà identico all'attributo **configurationNamingContext** dell'oggetto RootDSE.

**Per identificare tutte le partizioni di directory applicative in una foresta, seguire questa procedura**

1.  Nel contenitore partizioni della partizione di configurazione cercare o enumerare tutti gli oggetti [**crossRef**](/windows/desktop/ADSchema/c-crossref) .
2.  Se per un oggetto [**crossRef**](/windows/desktop/ADSchema/c-crossref) non è stato impostato il flag del controller di dominio di [**\_ SYSTEMFLAG \_ CR \_ NTDS \_ di ADS**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum) o il flag di **\_ \_ \_ \_ dominio NTDS di ADS SYSTEMFLAG CR** è impostato nel valore dell'attributo [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) , escludere l'oggetto dal set di risultati.
3.  Escludere la partizione dello schema dal set di risultati confrontando l'attributo [**NCName**](/windows/desktop/ADSchema/a-ncname) dell'oggetto [**crossRef**](/windows/desktop/ADSchema/c-crossref) con l'attributo **schemaNamingContext** dell'oggetto RootDSE.
4.  Escludere la partizione di configurazione dal set di risultati confrontando l'attributo [**NCName**](/windows/desktop/ADSchema/a-ncname) dell'oggetto [**crossRef**](/windows/desktop/ADSchema/c-crossref) con l'attributo **configurationNamingContext** dell'oggetto RootDSE.
5.  Gli oggetti [**crossRef**](/windows/desktop/ADSchema/c-crossref) rimanenti nel set di risultati rappresentano tutti le partizioni di directory applicative.

 

 