---
title: API per dispositivi UPnP
description: Il framework UPnP consente la rete dinamica di appliance intelligenti, dispositivi wireless e PC.
ms.assetid: 1dc05d6e-19ae-45e2-82c2-d3b63b16bf9d
keywords:
- UPnP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfadd64dbee845f62052e8b140ca1f0b69837ece78cf7b0cc5f24e61563a6e22
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124801"
---
# <a name="upnp-apis"></a>API per dispositivi UPnP

## <a name="purpose"></a>Scopo

Il framework UPnP consente la rete dinamica di appliance intelligenti, dispositivi wireless e PC. Esistono due API per l'uso di dispositivi con certificazione UPnP:

-   API del punto di controllo, costituita da un set di interfacce COM usate per trovare e controllare i dispositivi.
-   L'API Host dispositivo, costituita da un set di interfacce COM usate per implementare i dispositivi ospitati da un computer.

## <a name="where-applicable"></a>Se applicabile

L'API Punto di controllo consente agli sviluppatori di scrivere applicazioni che ricercano e controllano i dispositivi certificati UPnP. L'API Host dispositivi consente agli sviluppatori di implementare le funzionalità dei dispositivi con certificazione UPnP e di usare l'host del dispositivo per gestire le funzioni di individuazione, descrizione, controllo, presentazione e evento di un dispositivo certificato UPnP.

## <a name="developer-audience"></a>Sviluppatori

Gli sviluppatori che usano le API del punto di controllo e le API host del dispositivo devono avere familiarità con l'architettura del dispositivo UPnP. Per altre informazioni, vedere la documentazione [sull'implementazione di UPnP](https://openconnectivity.org/resources/upnpresources.zip) e il [forum UPnP](https://openconnectivity.org/).

Gli sviluppatori che usano le API host del dispositivo devono avere familiarità con le interfacce ACTIVE TEMPLATE LIBRARY (ATL) e COM.

Le API del punto di controllo e le API host del dispositivo vengono usate da un'ampia gamma di applicazioni, dagli script incorporati nelle pagine HTML ai programmi C++ e Microsoft Visual Basic completi.

Solo l'API del punto di controllo supporta Visual Basic Scripting Edition (VBScript).

## <a name="run-time-requirements"></a>Requisiti di runtime

L'API Punto di controllo viene usata nei computer che eseguono Microsoft Windows Millennium Edition, Windows XP, Windows XP Professional e Windows CE .NET.

L'API Host dispositivi viene usata nei computer che eseguono Windows XP, Windows XP Professional e Windows CE .NET.

Per informazioni più specifiche sui sistemi operativi che supportano una determinata funzione, vedere "Requisiti" nella documentazione.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                          | Descrizione                                                                                        |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Panoramica dell'architettura UPnP](overview-of-universal-plug-and-play.md)<br/>            | Informazioni generali e informazioni di base.<br/>                                                     |
| [Panoramica del punto di controllo](control-point-api.md)<br/>                                     | Informazioni generali sull'API del punto di controllo.<br/>                                        |
| [Uso dell'API del punto di controllo](using-the-control-point-api-with-upnp-technology.md)<br/> | Codice di esempio che illustra come sviluppare applicazioni che controllano i dispositivi certificati UPnP.<br/> |
| [Informazioni di riferimento sulle API del punto di controllo](control-point-api-with-upnp-technology-reference.md)<br/> | Documentazione di interfacce, metodi ed eventi dei componenti del punto di controllo.<br/>               |
| [Panoramica dell'API Host dispositivo](device-host-api.md)<br/>                                     | Informazioni generali sull'API Host dispositivi.<br/>                                          |
| [Uso dell'API Host dispositivo](using-the-device-host-api-with-upnp-technology.md)<br/>     | Codice di esempio che illustra come sviluppare un'applicazione per dispositivi con certificazione UPnP.<br/>        |
| [Informazioni di riferimento sulle API dell'host del dispositivo](device-host-api-with-upnp-technology-reference.md)<br/>     | Documentazione di interfacce, metodi ed eventi dei componenti dell'host del dispositivo.<br/>                 |



 

 

 





