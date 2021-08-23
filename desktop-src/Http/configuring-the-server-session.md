---
title: Configurazione della sessione del server
description: Configurazione della sessione del server
ms.assetid: 1e4e9440-8d70-44df-90a7-2d5e25b2f680
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 321d2710a0d9a0f7f3c70ad6de84336d382ae161b938ee2e22f20ddde5012604
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746591"
---
# <a name="configuring-the-server-session"></a>Configurazione della sessione del server

L'ID sessione del server viene creato con [**la funzione HttpCreateServerSession**](/windows/desktop/api/Http/nf-http-httpcreateserversession) e usato nella chiamata a [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty). Il *parametro pPropertyInformation* punta alla struttura di configurazione per il tipo di proprietà impostato. Il *parametro PropertyInformationLength* specifica le dimensioni, in byte, della struttura di configurazione. Ad esempio, quando si imposta **HttpServerTimeoutsProperty,** il parametro **pPropertyInformation** deve puntare a un buffer che sia almeno delle dimensioni della struttura [**HTTP TIMEOUT LIMIT \_ \_ \_ INFO.**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info)

In genere un'applicazione HTTP crea una sessione a server singolo e può impostare proprietà a livello di applicazione, ad esempio la limitazione della larghezza di banda globale o abilitare la registrazione centralizzata in questa sessione del server. [**HttpSetServerSessionProperty esegue l'override**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) delle configurazioni dell'API del server HTTP per l'applicazione chiamante. non influisce sulle proprietà a livello di API del server HTTP. Le configurazioni di sessione del server vengono sottoposti a query chiamando [**HttpQueryServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty).

 

 




