---
description: Media Service Provider Interface (MSPI) è un set di interfacce e metodi implementati da un MSP per consentire a un servizio di controllo delle applicazioni TAPI 3 il trasporto multimediale durante una sessione di comunicazione.
ms.assetid: 53b7bcbd-571a-44da-a6db-10d4c3e5d30a
title: Interfaccia del provider di servizi multimediali (MSPI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b1ce09e626ede14515c0abbbd5c3a35921026d6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320656"
---
# <a name="media-service-provider-interface-mspi"></a>Interfaccia del provider di servizi multimediali (MSPI)

Media Service Provider Interface (MSPI) è un set di interfacce e metodi implementati da un MSP per consentire a un servizio di controllo delle applicazioni TAPI 3 il trasporto multimediale durante una sessione di comunicazione. Un MSP gestisce i meccanismi specifici del dispositivo e specifici del protocollo necessari per applicare questi controlli e comunica con il relativo TSP associato o un'applicazione tramite l'uso dei metodi forniti in MSPI.

La sezione seguente (informazioni di [riferimento sull'interfaccia del provider di servizi multimediali (MSPI)](media-service-provider-interface-mspi-reference.md)) indica le interfacce che un MSP espone per interagire con l'ambiente di telefonia Microsoft.

Inoltre, un MSP può esporre metodi e interfacce private specifiche del provider per facilitare ulteriormente il controllo dei contenuti multimediali. Ad esempio, l' [msp della conferenza IP](ipconf-msp.md) espone le interfacce che forniscono il controllo del partecipante. Per informazioni sul funzionamento degli oggetti privati e sulle [interfacce msp IPConf](ipconf-msp-interfaces.md) per un elenco di riferimenti di IPConf, vedere [interfacce specifiche del provider](provider-specific-interfaces.md) .

La maggior parte degli sforzi di programmazione nella creazione di un MSP è molto specifica per una determinata piattaforma, dispositivo e protocollo di trasporto ed esula dall'ambito di questo documento. Tuttavia, Microsoft fornisce un set di classi di base MSP, che saranno utili per la maggior parte degli autori MSP. Per informazioni sull'uso di queste classi, vedere [classi base msp di TAPI 3](tapi-3-msp-base-classes.md) .

L'interfaccia [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress) rappresenta un provider di servizi multimediali per la dll TAPI. Questa interfaccia non viene utilizzata da o esposta a un'applicazione dell'utente finale. La DLL TAPI 3 chiama **CoCreateInstance** su questa interfaccia per creare l'oggetto msp principale. I metodi di questo oggetto consentono a un'applicazione di caricare e scaricare l'MSP, ricevere informazioni da un TSP e creare l'interfaccia [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol) , esposta nell'oggetto chiamata.

Le interfacce [**ITSubStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstreamcontrol) e [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) forniscono metodi paralleli rispetto ai sottoflussi. Il supporto del sottoflusso è facoltativo. Tutte le altre interfacce devono essere implementate da un MSP.

> [!Note]  
> Le operazioni implementate da una coppia TSP/MSP devono trovarsi in una DLL per consentire a un utente di aggiornare il provider di servizi senza riavviare il sistema.

 

 

 
