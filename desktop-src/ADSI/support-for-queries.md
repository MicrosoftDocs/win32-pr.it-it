---
title: Supporto per le query
description: Implementando l'interfaccia IDirectorySearch, i provider ADSI ottengono l'accesso a un subset di OLE DB funzionalità di sola lettura.
ms.assetid: 73ebed18-0e56-4902-a229-3b03f9be1cf6
ms.tgt_platform: multiple
keywords:
- Supporto per le query ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1304dcabd9c008b0f645982e695554225f59bac9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297647"
---
# <a name="support-for-queries"></a>Supporto per le query

Implementando l'interfaccia [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) , i provider ADSI ottengono l'accesso a un subset di OLE DB funzionalità di sola lettura.

L'implementazione ADSI dei metodi di [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) stesso usa le interfacce OLE DB descritte in adsi versione 1,0, incluso il seguente elenco di oggetti com:

-   Oggetto origine dati (il servizio directory), che supporta **IDBInitialize**, **IDBCreateSession**, **IDBProperties** e **IPersist**.
-   Oggetto DBSessions, che supporta **IOpenRowSet**, **ISessionProperties** e **ICreateCommand**.
-   Oggetto Command, che supporta **ICommand**, **IAccessor**, **IColumnsInfo**, **ICommandProperties**, **ICommandText** e **IConvertType**.
-   Oggetto rowset, che supporta **IAccessor**, **IColumnsInfo**, **IConvertType**, **IRowset** e **IRowsetInfo**.

Per ulteriori informazioni su OLE DB, vedere la Guida di riferimento per i programmatori OLE DB nella piattaforma Software Development Kit (SDK).

 

 




