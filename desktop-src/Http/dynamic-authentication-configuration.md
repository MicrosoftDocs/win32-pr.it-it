---
title: Configurazione dell'autenticazione dinamica
description: Le applicazioni possono modificare le configurazioni di autenticazione in un gruppo di URL o in una sessione del server in qualsiasi momento.
ms.assetid: 8a5cc119-0427-487d-a155-74c14e2104d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84c68daf04d870d4aa50596397f4f021ac1729af
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328895"
---
# <a name="dynamic-authentication-configuration"></a>Configurazione dell'autenticazione dinamica

Per impostazione predefinita, l'API server HTTP non esegue l'autenticazione a meno che l'applicazione non lo consenta in modo specifico. Le applicazioni possono modificare le configurazioni di autenticazione in un gruppo di URL o in una sessione del server in qualsiasi momento. Le modifiche apportate alla configurazione dell'autenticazione non influiscono sulle richieste già autenticate o inviate all'applicazione

Per gli schemi di autenticazione in cui sono necessari più cicli di handshake, l'API server HTTP elimina l'handshake di autenticazione se lo schema corrente non è più supportato a causa delle modifiche di configurazione dell'applicazione. Se, ad esempio, l'applicazione Abilita Negotiate e Disabilita NTLM e l'API del server HTTP è nell'handshake di autenticazione intermedia per NTLM, l'handshake per NTLM viene ignorato e la richiesta viene passata all'applicazione. L'applicazione invia una richiesta di autenticazione 401 con i nuovi tipi di autenticazione specificati nell'intestazione del WWW-Authenticate.

 

 




