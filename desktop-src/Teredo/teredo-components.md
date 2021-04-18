---
title: Componenti Teredo
ms.assetid: 95d83030-b1de-4f09-b9d0-f443d9672ca1
description: 'Altre informazioni su: componenti Teredo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4b4de66f38d5eb64b8321b6bb89e78fbb763e60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305842"
---
# <a name="teredo-components"></a>Componenti Teredo

L'infrastruttura [Teredo](about-teredo.md) è costituita dai componenti seguenti:

## <a name="teredo-clients"></a>Client Teredo

Un client Teredo è un nodo IPv6/IPv4 che supporta un'interfaccia di tunneling Teredo tramite cui i pacchetti vengono sottoutilizzati tramite tunneling per altri client o nodi Teredo nella rete Internet IPv6 (tramite un inoltro Teredo). Un client Teredo comunica con un server Teredo per ottenere un prefisso di indirizzo da cui un indirizzo IPv6 basato su Teredo viene configurato o utilizzato per facilitare la comunicazione con altri client o host Teredo nella rete Internet IPv6.

Windows XP con Service Pack 1 (SP1) con Advanced Networking Pack, Windows XP con Service Pack 2 (SP2), Windows Server 2003 con Service Pack 1 (SP1), Windows Server 2003 con Service Pack 2 (SP2), Windows Vista e Windows Server 2008 includono tutti il client Teredo.

## <a name="teredo-servers"></a>Server Teredo

Un server Teredo è un nodo IPv6/IPv4 connesso sia alla rete Internet IPv4 che alla rete Internet IPv6 e supporta un'interfaccia di tunneling Teredo su cui vengono ricevuti i pacchetti. Il ruolo generale del server Teredo è fornire assistenza nella configurazione degli indirizzi dei client Teredo e facilitare la comunicazione iniziale tra client Teredo e altri client Teredo oppure tra client Teredo e host solo IPv6. Il server Teredo è in ascolto sulla porta UDP 3544 per il traffico Teredo.

Diversamente dal client, il server Teredo non è incluso nelle piattaforme operative Microsoft. Per facilitare la comunicazione tra i computer client Teredo basati su Windows, Microsoft ha distribuito server Teredo sulla rete Internet IPv4.

## <a name="teredo-relays"></a>Inoltri Teredo

Un inoltro Teredo è un router IPv6/IPv4 che può inoltrare pacchetti tra client Teredo nella rete Internet IPv4 (usando un'interfaccia di tunneling Teredo) e host solo IPv6. In alcuni casi, l'inoltro Teredo interagisce con un server Teredo per facilitare la comunicazione iniziale tra client Teredo e host solo IPv6. Il relay Teredo è in ascolto sulla porta UDP 3544 per il traffico Teredo.

Analogamente al server Teredo, le piattaforme operative Microsoft non includono la funzionalità di inoltro Teredo. Microsoft non prevede attualmente la distribuzione di relay Teredo sulla rete Internet IPv4. Gli inoltri Teredo non sono necessari per comunicare con relay specifici dell'host Teredo.

## <a name="teredo-host-specific-relays"></a>Inoltri Host-Specific Teredo

La comunicazione tra client Teredo e host IPv6 configurati con un indirizzo globale deve passare attraverso un inoltro Teredo. Questa operazione è necessaria per gli host solo IPv6 connessi alla rete Internet IPv6. Tuttavia, quando l'host IPv6 è in grado di supportare IPv6 e IPv4 e connesso sia alla rete Internet IPv4 che alla rete Internet IPv6, la comunicazione deve essere eseguita tra il client Teredo e l'host IPv6 sulla rete Internet IPv4, anziché attraversare la rete Internet IPv6 e passare attraverso un inoltro Teredo.

Un inoltro specifico dell'host Teredo è un nodo IPv6/IPv4 che dispone di un'interfaccia e una connettività sia alla rete Internet IPv4 che alla rete Internet IPv6 e può comunicare direttamente con i client Teredo sulla rete Internet IPv4, senza la necessità di un inoltro Teredo intermedio. La connettività alla rete Internet IPv4 può essere tramite un indirizzo IPv4 pubblico o tramite un indirizzo IPv4 privato e una NAT vicina. La connettività alla rete Internet IPv6 può essere tramite una connessione diretta alla rete Internet IPv6 o tramite una tecnologia di transizione IPv6, ad esempio 6to4, in cui i pacchetti IPv6 vengono sottoposti a tunneling attraverso la rete Internet IPv4. Il relay specifico dell'host Teredo è in ascolto sulla porta UDP 3544 per il traffico Teredo.

Windows XP con SP1 con Advanced Networking Pack, Windows XP con SP2, Windows Server 2003 con SP1, Windows Server 2003 con SP2, Windows Vista e Windows Server 2008 includono funzionalità di inoltro specifiche dell'host Teredo, abilitate automaticamente se il computer dispone di un indirizzo globale assegnato. Un indirizzo globale viene assegnato in un messaggio di annuncio router ricevuto da un router IPv6 nativo, da un router ISATAP o da un router 6to4. Se il computer non dispone di un indirizzo globale, è abilitata la funzionalità client Teredo.

Il relay specifico dell'host Teredo consente ai client Teredo di comunicare in modo efficiente con gli host 6to4, gli host IPv6 con un prefisso globale non 6to4 o gli host ISATAP o 6over4 all'interno di organizzazioni che utilizzano un prefisso globale per i rispettivi indirizzi, purché entrambi gli host usino una versione di Windows che supporta Teredo.

 

 




