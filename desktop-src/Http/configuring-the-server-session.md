---
title: Configurazione della sessione del server
description: Configurazione della sessione del server
ms.assetid: 1e4e9440-8d70-44df-90a7-2d5e25b2f680
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d41c1606cce397c49a15c62dae10531edfde93f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090939"
---
# <a name="configuring-the-server-session"></a><span data-ttu-id="a666a-103">Configurazione della sessione del server</span><span class="sxs-lookup"><span data-stu-id="a666a-103">Configuring the Server Session</span></span>

<span data-ttu-id="a666a-104">L'ID sessione del server viene creato con [**la funzione HttpCreateServerSession**](/windows/desktop/api/Http/nf-http-httpcreateserversession) e usato nella chiamata a [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty).</span><span class="sxs-lookup"><span data-stu-id="a666a-104">The server session ID is created with the [**HttpCreateServerSession**](/windows/desktop/api/Http/nf-http-httpcreateserversession) function, and used in the call to [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty).</span></span> <span data-ttu-id="a666a-105">Il *parametro pPropertyInformation* punta alla struttura di configurazione per il tipo di proprietà impostato.</span><span class="sxs-lookup"><span data-stu-id="a666a-105">The *pPropertyInformation* parameter points to the configuration structure for the property type that is set.</span></span> <span data-ttu-id="a666a-106">Il *parametro PropertyInformationLength* specifica le dimensioni, in byte, della struttura di configurazione.</span><span class="sxs-lookup"><span data-stu-id="a666a-106">The *PropertyInformationLength* parameter specifies the size, in bytes, of the configuration structure.</span></span> <span data-ttu-id="a666a-107">Ad esempio, quando si imposta **HttpServerTimeoutsProperty,** il parametro **pPropertyInformation** deve puntare a un buffer che sia almeno delle dimensioni della struttura [**HTTP TIMEOUT LIMIT \_ \_ \_ INFO.**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info)</span><span class="sxs-lookup"><span data-stu-id="a666a-107">For example, when setting the **HttpServerTimeoutsProperty** the **pPropertyInformation** parameter must point to a buffer that is at least the size of the [**HTTP\_TIMEOUT\_LIMIT\_INFO**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) structure.</span></span>

<span data-ttu-id="a666a-108">In genere un'applicazione HTTP crea una sessione a server singolo e può impostare proprietà a livello di applicazione, ad esempio la limitazione della larghezza di banda globale o abilitare la registrazione centralizzata in questa sessione del server.</span><span class="sxs-lookup"><span data-stu-id="a666a-108">Typically an HTTP application creates a single server session and may set application wide properties such as global bandwidth throttling limit or enable centralized logging on this server session.</span></span> <span data-ttu-id="a666a-109">[**HttpSetServerSessionProperty esegue l'override**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) delle configurazioni dell'API del server HTTP per l'applicazione chiamante. non influisce sulle proprietà a livello di API del server HTTP.</span><span class="sxs-lookup"><span data-stu-id="a666a-109">[**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) overrides the HTTP Server API configurations for the calling application; it does not affect the HTTP Server API-wide properties.</span></span> <span data-ttu-id="a666a-110">Le configurazioni di sessione del server vengono sottoposti a query chiamando [**HttpQueryServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty).</span><span class="sxs-lookup"><span data-stu-id="a666a-110">The server session configurations are queried by calling [**HttpQueryServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty).</span></span>

 

 




