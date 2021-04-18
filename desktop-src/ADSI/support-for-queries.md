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
# <a name="support-for-queries"></a><span data-ttu-id="7c6f0-104">Supporto per le query</span><span class="sxs-lookup"><span data-stu-id="7c6f0-104">Support for Queries</span></span>

<span data-ttu-id="7c6f0-105">Implementando l'interfaccia [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) , i provider ADSI ottengono l'accesso a un subset di OLE DB funzionalità di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="7c6f0-105">By implementing the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface, ADSI providers gain access to a subset of OLE DB read-only features.</span></span>

<span data-ttu-id="7c6f0-106">L'implementazione ADSI dei metodi di [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) stesso usa le interfacce OLE DB descritte in adsi versione 1,0, incluso il seguente elenco di oggetti com:</span><span class="sxs-lookup"><span data-stu-id="7c6f0-106">The ADSI implementation of the methods of [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) itself uses the OLE DB interfaces described in ADSI Version 1.0, including the following list of COM objects:</span></span>

-   <span data-ttu-id="7c6f0-107">Oggetto origine dati (il servizio directory), che supporta **IDBInitialize**, **IDBCreateSession**, **IDBProperties** e **IPersist**.</span><span class="sxs-lookup"><span data-stu-id="7c6f0-107">Data Source Object (the directory service), supporting **IDBInitialize**, **IDBCreateSession**, **IDBProperties**, and **IPersist**.</span></span>
-   <span data-ttu-id="7c6f0-108">Oggetto DBSessions, che supporta **IOpenRowSet**, **ISessionProperties** e **ICreateCommand**.</span><span class="sxs-lookup"><span data-stu-id="7c6f0-108">DBSessions Object, supporting **IOpenRowSet**, **ISessionProperties**, and **ICreateCommand**.</span></span>
-   <span data-ttu-id="7c6f0-109">Oggetto Command, che supporta **ICommand**, **IAccessor**, **IColumnsInfo**, **ICommandProperties**, **ICommandText** e **IConvertType**.</span><span class="sxs-lookup"><span data-stu-id="7c6f0-109">Command Object, supporting **ICommand**, **IAccessor**, **IColumnsInfo**, **ICommandProperties**, **ICommandText**, and **IConvertType**.</span></span>
-   <span data-ttu-id="7c6f0-110">Oggetto rowset, che supporta **IAccessor**, **IColumnsInfo**, **IConvertType**, **IRowset** e **IRowsetInfo**.</span><span class="sxs-lookup"><span data-stu-id="7c6f0-110">Rowset Object, supporting **IAccessor**, **IColumnsInfo**, **IConvertType**, **IRowset**, and **IRowsetInfo**.</span></span>

<span data-ttu-id="7c6f0-111">Per ulteriori informazioni su OLE DB, vedere la Guida di riferimento per i programmatori OLE DB nella piattaforma Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="7c6f0-111">For more information about OLE DB, see the OLE DB Programmer's Reference in the Platform Software Development Kit (SDK).</span></span>

 

 




