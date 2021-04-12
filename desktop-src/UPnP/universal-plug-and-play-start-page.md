---
title: API per dispositivi UPnP
description: Il Framework UPnP consente la rete dinamica di Appliance intelligenti, dispositivi wireless e PC.
ms.assetid: 1dc05d6e-19ae-45e2-82c2-d3b63b16bf9d
keywords:
- UPnP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 022ede01a62230194969d7789e0ace70f960debb
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "104118614"
---
# <a name="upnp-apis"></a>API per dispositivi UPnP

## <a name="purpose"></a>Scopo

Il Framework UPnP consente la rete dinamica di Appliance intelligenti, dispositivi wireless e PC. Sono disponibili due API per l'uso di dispositivi certificati da UPnP:

-   API del punto di controllo, che è costituita da un set di interfacce COM usate per trovare e controllare i dispositivi.
-   L'API host del dispositivo, che è costituita da un set di interfacce COM usate per implementare i dispositivi ospitati da un computer.

## <a name="where-applicable"></a>Se applicabile

L'API del punto di controllo consente agli sviluppatori di scrivere applicazioni per la ricerca e il controllo dei dispositivi certificati UPnP. L'API host del dispositivo consente agli sviluppatori di implementare la funzionalità di dispositivi certificati da UPnP e di usare l'host del dispositivo per gestire le funzioni di individuazione, descrizione, controllo, presentazione e evento di un dispositivo certificato UPnP.

## <a name="developer-audience"></a>Sviluppatori

Gli sviluppatori che usano le API del punto di controllo e le API host del dispositivo devono avere familiarità con l'architettura del dispositivo UPnP. Per ulteriori informazioni, vedere la [documentazione sull'implementazione di UPnP](https://openconnectivity.org/resources/upnpresources.zip) e il [Forum di UPnP](https://openconnectivity.org/).

Gli sviluppatori che usano le API host del dispositivo devono avere familiarità con le interfacce Active Template Library (ATL) e COM.

Le API del punto di controllo e le API dell'host del dispositivo sono utilizzate da un'ampia gamma di applicazioni, dagli script incorporati nelle pagine HTML ai programmi completi C++ e Microsoft Visual Basic.

Solo l'API del punto di controllo supporta Visual Basic Scripting Edition (VBScript).

## <a name="run-time-requirements"></a>Requisiti di runtime

L'API del punto di controllo viene utilizzata in computer che eseguono Microsoft Windows Millennium Edition, Windows XP, Windows XP Professional e Windows CE .NET.

L'API host del dispositivo viene utilizzata in computer che eseguono Windows XP, Windows XP Professional e Windows CE .NET.

Per informazioni più specifiche sui sistemi operativi che supportano una particolare funzione, vedere la sezione relativa ai requisiti nella documentazione.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                          | Descrizione                                                                                        |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Panoramica dell'architettura UPnP](overview-of-universal-plug-and-play.md)<br/>            | Informazioni generali e background.<br/>                                                     |
| [Panoramica sui punti di controllo](control-point-api.md)<br/>                                     | Informazioni generali sull'API del punto di controllo.<br/>                                        |
| [Uso dell'API del punto di controllo](using-the-control-point-api-with-upnp-technology.md)<br/> | Codice di esempio che illustra come sviluppare applicazioni che controllano i dispositivi certificati UPnP.<br/> |
| [Riferimento all'API del punto di controllo](control-point-api-with-upnp-technology-reference.md)<br/> | Documentazione delle interfacce, dei metodi e degli eventi del componente del punto di controllo.<br/>               |
| [Panoramica dell'API dell'host del dispositivo](device-host-api.md)<br/>                                     | Informazioni generali sull'API dell'host del dispositivo.<br/>                                          |
| [Uso dell'API host del dispositivo](using-the-device-host-api-with-upnp-technology.md)<br/>     | Codice di esempio che illustra come sviluppare un'applicazione per i dispositivi certificati UPnP.<br/>        |
| [Informazioni di riferimento sull'API dell'host del dispositivo](device-host-api-with-upnp-technology-reference.md)<br/>     | Documentazione delle interfacce, dei metodi e degli eventi del componente host del dispositivo.<br/>                 |



 

 

 





