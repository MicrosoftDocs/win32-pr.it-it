---
title: Concessione dell'accesso come servizio direttamente nel computer host
description: Quando si installa un servizio per l'esecuzione con un account utente di dominio, l'account deve avere il diritto di accedere come servizio nel computer locale.
ms.assetid: 1b217650-4397-4e28-b53e-8b03f3caf903
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95ef2bb87c3cf461e67cb7da20f36d9ac07fb362
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707612"
---
# <a name="granting-logon-as-service-right-on-the-host-computer"></a>Concessione dell'accesso come servizio direttamente nel computer host

Quando si installa un servizio per l'esecuzione con un account utente di dominio, l'account deve avere il diritto di accedere come servizio nel computer locale. Tenere presente che questo diritto di accesso si applica solo al computer locale e deve essere concesso nei criteri LSA locali di ogni computer host. Questo passaggio non è necessario se il servizio viene eseguito come LocalSystem, a cui, per impostazione predefinita, viene concesso questo diritto.

Per ulteriori informazioni su come concedere il diritto di accesso come servizio a livello di codice, vedere il [codice di esempio LSAPrivs](https://www.google.com/#q=LSAPrivs).

 

 




