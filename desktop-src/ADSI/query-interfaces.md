---
title: Interfacce di query
description: Per eseguire ricerche nella directory, è possibile usare tre tipi di interfacce ADSI. L'ambiente dell'applicazione e altri requisiti possono indicare quale interfaccia viene usata.
ms.assetid: 42843e02-b685-492e-9046-aea460e84584
ms.tgt_platform: multiple
keywords:
- Interfacce di query ADSI
- Esegue query ad ADSI, interfacce di query
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 967f111107549fd0e6352f0e93d3a747b287c040ea7d5e6cee48415aa7f7925f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637721"
---
# <a name="query-interfaces"></a>Interfacce di query

Per eseguire ricerche nella directory, è possibile usare tre tipi di interfacce ADSI. L'ambiente dell'applicazione e altri requisiti possono indicare quale interfaccia viene usata.

-   [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch). **IDirectorySearch è** un'interfaccia COM di base disponibile solo per i programmatori C/C++. Per altre informazioni, vedere [Ricerca con l'interfaccia IDirectorySearch.](searching-with-idirectorysearch.md)
-   Ado. Le ActiveX ADO (Data Object) sono interfacce di automazione che usano OLE DB. Usare ADO per le query all'interno di applicazioni che si basano su Automazione. Queste includono Visual Basic applicazioni, Active Server pagine e così via. Per altre informazioni, vedere [Ricerca con oggetti ActiveX dati.](searching-with-activex-data-objects-ado.md)
-   OLE DB. OLE DB è un set di interfacce C/C++ usate per eseguire query nei database. Grazie al supporto di queste interfacce, i provider ADSI possono implementare funzionalità OLE DB, ad esempio query distribuite con altri provider OLE DB. Per altre informazioni, vedere [Ricerca con OLE DB](searching-with-ole-db.md).

 

 




