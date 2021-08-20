---
title: Configurazione dell'autenticazione dinamica
description: Le applicazioni possono modificare le configurazioni di autenticazione in un gruppo di URL o in una sessione del server in qualsiasi momento.
ms.assetid: 8a5cc119-0427-487d-a155-74c14e2104d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fda33e150826ed7d84ac45c4ab0771136991aa9aeb2766d5d395a65da270775
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014839"
---
# <a name="dynamic-authentication-configuration"></a>Configurazione dell'autenticazione dinamica

Per impostazione predefinita, l'API del server HTTP non esegue l'autenticazione a meno che l'applicazione non lo consenta in modo specifico. Le applicazioni possono modificare le configurazioni di autenticazione in un gruppo di URL o in una sessione del server in qualsiasi momento. Le modifiche alla configurazione dell'autenticazione non influiscono sulle richieste già autenticate o inviate all'applicazione

Per gli schemi di autenticazione in cui sono necessari più round di handshake, l'API del server HTTP elimina l'handshake di autenticazione se lo schema corrente non è più supportato a causa di modifiche di configurazione dall'applicazione. Ad esempio, se l'applicazione abilita Negotiate e disabilita NTLM e l'API del server HTTP si trova nell'handshake di autenticazione intermedio per NTLM, l'handshake per NTLM viene eliminato e la richiesta viene passata all'applicazione. L'applicazione invia una richiesta di autenticazione 401 con i nuovi tipi di autenticazione specificati nell'intestazione WWW-Authenticate richiesta.

 

 




