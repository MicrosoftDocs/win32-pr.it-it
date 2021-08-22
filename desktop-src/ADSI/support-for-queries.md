---
title: Supporto per le query
description: Implementando l'interfaccia IDirectorySearch, i provider ADSI ottengono l'accesso a un subset OLE DB funzionalità di sola lettura.
ms.assetid: 73ebed18-0e56-4902-a229-3b03f9be1cf6
ms.tgt_platform: multiple
keywords:
- Supporto per query ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30ad1892cf7c0e619ef55b9c3e5af6885d4cbdc7ac68fbcbd206524128b283d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023229"
---
# <a name="support-for-queries"></a>Supporto per le query

Implementando [**l'interfaccia IDirectorySearch,**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) i provider ADSI ottengono l'accesso a un subset di OLE DB di sola lettura.

L'implementazione ADSI dei metodi [**di IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) stesso usa le interfacce OLE DB descritte in ADSI versione 1.0, incluso l'elenco seguente di oggetti COM:

-   Oggetto origine dati (servizio directory), che supporta **IDBInitialize**, **IDBCreateSession**, **IDBProperties** e **IPersist**.
-   Oggetto DBSessions, che supporta **IOpenRowSet,** **ISessionProperties** e **ICreateCommand.**
-   Oggetto Command, che supporta **ICommand**, **IAccessor**, **IColumnsInfo**, **ICommandProperties**, **ICommandText** e **IConvertType**.
-   Oggetto rowset, che supporta **IAccessor**, **IColumnsInfo**, **IConvertType**, **IRowset** e **IRowsetInfo**.

Per altre informazioni sui OLE DB, vedere la guida OLE DB per programmatori in Platform Software Development Kit (SDK).

 

 




