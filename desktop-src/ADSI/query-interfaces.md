---
title: Interfacce di query
description: Per eseguire ricerche nella directory è possibile usare tre tipi di interfacce ADSI. L'ambiente dell'applicazione e altri requisiti possono indicare quale interfaccia viene utilizzata.
ms.assetid: 42843e02-b685-492e-9046-aea460e84584
ms.tgt_platform: multiple
keywords:
- Interfacce di query ADSI
- Query ADSI, interfacce di query
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 805303a972b4a8140a9e632857287aeebca9b32f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855261"
---
# <a name="query-interfaces"></a>Interfacce di query

Per eseguire ricerche nella directory è possibile usare tre tipi di interfacce ADSI. L'ambiente dell'applicazione e altri requisiti possono indicare quale interfaccia viene utilizzata.

-   [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch). **IDirectorySearch** è un'interfaccia com di base disponibile solo per i programmatori C/C++. Per ulteriori informazioni, vedere [ricerca con l'interfaccia IDirectorySearch](searching-with-idirectorysearch.md).
-   ADO. Le interfacce ADO (ActiveX Data Object) sono interfacce di automazione che utilizzano OLE DB. Usare ADO per le query all'interno di applicazioni che si basano sull'automazione. Sono incluse Visual Basic applicazioni, Active Server pagine e così via. Per ulteriori informazioni, vedere [ricerca con ActiveX Data Objects](searching-with-activex-data-objects-ado.md).
-   OLE DB. OLE DB è un set di interfacce C/C++ utilizzate per eseguire query sui database. Grazie al supporto di queste interfacce, i provider ADSI possono implementare funzionalità di OLE DB avanzate, ad esempio query distribuite con altri provider di OLE DB. Per ulteriori informazioni, vedere [ricerca con OLE DB](searching-with-ole-db.md).

 

 




