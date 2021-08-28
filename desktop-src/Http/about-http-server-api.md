---
title: Informazioni sull'API server HTTP
description: L'API server HTTP fornisce agli sviluppatori un'interfaccia di basso livello sul lato server della funzionalità HTTP, come definito in RFC 2616.
ms.assetid: 74ad3a1d-cde2-4849-a412-d9d4101eaf12
keywords:
- API server HTTP, panoramica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55883fa75b366a2f5c5ef434f1eef3a95651440738735b025cfe5ef1b0534106
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015009"
---
# <a name="about-http-server-api"></a>Informazioni sull'API server HTTP

L'API server HTTP fornisce agli sviluppatori un'interfaccia di basso livello sul lato server della funzionalità HTTP, come definito in [RFC 2616.](https://www.ietf.org/rfc/rfc2616.txt) L'API consente a un'applicazione di ricevere richieste HTTP indirizzate agli URL e di inviare risposte HTTP. Per l'invio di risposte dinamiche, è consigliabile utilizzare le interfacce ISAPI o ASP.NET.

L'API server HTTP consente a più applicazioni di coesistere in un sistema, condividendo la stessa porta TCP (ad esempio, la porta 80 per HTTP o la porta 443 per HTTPS) e servendo parti diverse dello spazio dei nomi URL.

L'API server HTTP richiede la conoscenza del linguaggio di programmazione C e una familiarità con la Windows api. Le applicazioni che non richiedono l'accesso di basso livello a HTTP devono usare iis ISAPI o le classi .NET Framework per le soluzioni basate su HTTP.

 

 




