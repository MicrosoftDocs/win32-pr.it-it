---
title: Creazione di una descrizione del dispositivo
description: Una descrizione del dispositivo basata su UPnP è un documento XML che descrive le proprietà di un dispositivo e la gerarchia di dispositivi annidati al suo interno.
ms.assetid: b2a7d342-958c-439d-8b17-b4fdc5fbad12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b52df95de15481c7004704b6f67cd9478083ac88
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955342"
---
# <a name="creating-a-device-description"></a>Creazione di una descrizione del dispositivo

Una [*Descrizione del dispositivo*](d-gly.md) basata su UPnP è un documento XML che descrive le proprietà di un dispositivo e la gerarchia di dispositivi annidati al suo interno. Lo schema per le descrizioni dei dispositivi basati su UPnP, noto come UTL (UPnP Template Language) per i dispositivi, è definito nell'architettura del dispositivo UPnP. Le descrizioni dei dispositivi contengono collegamenti a [*descrizioni dei servizi*](s-gly.md). Lo schema per le descrizioni dei servizi e UTL per i servizi è definito anche nella specifica "architettura del dispositivo UPnP".

> [!Note]  
> Potrebbero verificarsi problemi durante l'uso della descrizione del servizio da www.upnp.org.

 

Lo sviluppatore di un dispositivo deve fornire descrizioni del dispositivo e del servizio per il dispositivo.

Gli elementi di una descrizione del dispositivo che lo sviluppatore di un dispositivo ospitato deve fornire sono gli stessi di quelli definiti nella specifica "architettura del dispositivo UPnP", con le eccezioni seguenti:

-   Gli elementi **controlURL** e **eventSubURL** sono obbligatori e devono essere vuoti. Quando il dispositivo viene pubblicato e annunciato, l'host del dispositivo compila i valori per questi campi.
-   L'elemento **UDN** deve contenere un identificatore univoco per il documento di descrizione del dispositivo, ovvero non deve essere univoco a livello globale. Questo identificatore viene usato per cercare il UDN generato dall'host del dispositivo.
-   Gli elementi **SCPDURL** non devono contenere URL per le descrizioni dei servizi. Ma devono contenere il nome del file di descrizione del servizio. Il file di descrizione del servizio deve trovarsi nella [*directory delle risorse*](r-gly.md). Il percorso di questa directory deve essere fornito all'host del dispositivo durante il processo di registrazione, ad esempio l'uso di un programma di installazione. Questo percorso e tutti i sottostanti sono percorsi relativi, in base al percorso registrato.
-   L'elemento **URL** all'interno dell'elemento **Icon** non deve contenere URL per le icone del dispositivo. Ma devono contenere il nome del file icona. Se presente, il file icona deve trovarsi nella directory delle risorse. Questo percorso e tutti i sottostanti sono percorsi relativi, in base al percorso registrato.
-   L'elemento **URLBase** non deve essere presente.

> [!Note]  
> Tutti gli URL generati dall'host del dispositivo sono URL relativi. Gli URL sono relativi alla posizione del documento di descrizione del dispositivo, che viene inviato nell'annuncio iniziale del dispositivo.

 

> [!IMPORTANT]
> Non aggiungere commenti al documento di descrizione del dispositivo perché potrebbe causare errori di registrazione quando l'host del dispositivo Plug and Play universale tenta di analizzare il documento.

 

## <a name="string-length-limitations"></a>Limitazioni della lunghezza della stringa

Le lunghezze di stringa seguenti vengono usate nell'API host del dispositivo con la tecnologia UPnP:

-   **DeviceType** -64 byte
-   **FriendlyName** -64 byte
-   **produttore** -64 byte
-   **modelDescription** -128 byte
-   **ModelName** -32 byte
-   **ModelNumber** -32 byte
-   **serialNumber** -64 byte
-   **UPC** – 12 byte
-   **serviceType** -64 byte
-   **ServiceID** -64 byte

 

 




