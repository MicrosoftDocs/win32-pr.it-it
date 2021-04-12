---
description: Alcuni oggetti supportano un solo handle alla volta.
ms.assetid: 3eafd0e0-3923-4489-8a0a-63007dd3183a
title: Limitazioni della gestione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99caa991b1ffa0a4e0c02ff32225c3260eb4a016
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233487"
---
# <a name="handle-limitations"></a><span data-ttu-id="2121a-103">Limitazioni della gestione</span><span class="sxs-lookup"><span data-stu-id="2121a-103">Handle Limitations</span></span>

<span data-ttu-id="2121a-104">Alcuni oggetti supportano un solo handle alla volta.</span><span class="sxs-lookup"><span data-stu-id="2121a-104">Some objects support only one handle at a time.</span></span> <span data-ttu-id="2121a-105">Il sistema fornisce l'handle quando un'applicazione crea l'oggetto e invalida l'handle quando l'applicazione elimina definitivamente l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2121a-105">The system provides the handle when an application creates the object and invalidates the handle when the application destroys the object.</span></span> <span data-ttu-id="2121a-106">Altri oggetti supportano più handle per un singolo oggetto.</span><span class="sxs-lookup"><span data-stu-id="2121a-106">Other objects support multiple handles to a single object.</span></span> <span data-ttu-id="2121a-107">Il sistema operativo rimuove automaticamente l'oggetto dalla memoria dopo la chiusura dell'ultimo handle per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2121a-107">The operating system automatically removes the object from memory after the last handle to the object is closed.</span></span>

<span data-ttu-id="2121a-108">Il numero totale di handle aperti nel sistema è limitato solo dalla quantità di memoria disponibile.</span><span class="sxs-lookup"><span data-stu-id="2121a-108">The total number of open handles in the system is limited only by the amount of memory available.</span></span> <span data-ttu-id="2121a-109">Alcuni tipi di oggetto supportano un numero limitato di handle per sessione o per processo.</span><span class="sxs-lookup"><span data-stu-id="2121a-109">Some object types support a limited number of handles per session or per process.</span></span>

 

 



