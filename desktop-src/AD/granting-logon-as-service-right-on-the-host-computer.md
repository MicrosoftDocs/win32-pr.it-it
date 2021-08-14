---
title: Concessione del diritto di accesso come servizio nel computer host
description: Quando si installa un servizio da eseguire con un account utente di dominio, l'account deve avere il diritto di accedere come servizio nel computer locale.
ms.assetid: 1b217650-4397-4e28-b53e-8b03f3caf903
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef53e68feb9312bb8efdca285716aa5b6ea077e2e85f6c5538eb13532b51a8ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188955"
---
# <a name="granting-logon-as-service-right-on-the-host-computer"></a>Concessione del diritto di accesso come servizio nel computer host

Quando si installa un servizio da eseguire con un account utente di dominio, l'account deve avere il diritto di accedere come servizio nel computer locale. Tenere presente che questo diritto di accesso si applica solo al computer locale e deve essere concesso nei criteri LSA locali di ogni computer host. Questo passaggio non è necessario se il servizio viene eseguito come LocalSystem, a cui, per impostazione predefinita, viene concesso questo diritto.

Per altre informazioni su come concedere diritti di accesso come servizio a livello di codice, vedere il codice di esempio [LSAPrivs](https://www.google.com/#q=LSAPrivs).

 

 




