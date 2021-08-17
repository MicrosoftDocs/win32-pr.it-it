---
description: Interfacce di connessione MTP/Bluetooth
ms.assetid: 7bbd5fe3-85f1-4f0a-9d3e-22746bd23aae
title: Interfacce di connessione MTP/Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c0f32717afe14be05cae6e43d097e67fc9790729e5be4ce9c2dfa6f901a126a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843368"
---
# <a name="mtpbluetooth-connection-interfaces"></a>Interfacce di connessione MTP/Bluetooth

Le interfacce seguenti consentono alle applicazioni di enumerare e connettersi solo ai dispositivi che supportano il protocollo MTP (Media Transfer Protocol) su Bluetooth (MTP/Bluetooth). Le interfacce client, di raccolta e di driver WPD non sono limitate al protocollo MTP/Bluetooth.



| Interfaccia                                                              | Descrizione                                                                                                         |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**IConnectionRequestCallback**](iconnectionrequestcallback.md)       | Definisce un singolo metodo di callback utilizzato dalle applicazioni per ricevere la notifica delle richieste completate e annullate. |
| [**IEnumPortableDeviceConnectors**](ienumportabledeviceconnectors.md) | Enumera le **interfacce IPortableDeviceConnector.**                                                                 |
| [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector)           | Supporta i metodi che le applicazioni chiamano per stabilire connessioni a dispositivi Bluetooth MTP.                          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida di riferimento alla programmazione**](programming-reference.md)
</dt> </dl>

 

 



