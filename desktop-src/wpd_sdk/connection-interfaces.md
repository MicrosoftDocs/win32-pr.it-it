---
description: Interfacce di connessione MTP/Bluetooth
ms.assetid: 7bbd5fe3-85f1-4f0a-9d3e-22746bd23aae
title: Interfacce di connessione MTP/Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97e5194b8a6ababc05c36590ef30ae19ab185efe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058187"
---
# <a name="mtpbluetooth-connection-interfaces"></a>Interfacce di connessione MTP/Bluetooth

Le interfacce seguenti consentono alle applicazioni di enumerare e connettersi solo ai dispositivi che supportano il protocollo MTP (Media Transfer Protocol) su Bluetooth (MTP/Bluetooth). Le interfacce del driver WPD, della raccolta e del client non sono limitate al protocollo MTP/Bluetooth.



| Interfaccia                                                              | Descrizione                                                                                                         |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**IConnectionRequestCallback**](iconnectionrequestcallback.md)       | Definisce un unico metodo di callback utilizzato dalle applicazioni per ricevere la notifica delle richieste completate e annullate. |
| [**IEnumPortableDeviceConnectors**](ienumportabledeviceconnectors.md) | Enumera le interfacce **IPortableDeviceConnector** .                                                                 |
| [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector)           | Supporta i metodi chiamati dalle applicazioni per stabilire connessioni ai dispositivi Bluetooth MTP.                          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida di riferimento alla programmazione**](programming-reference.md)
</dt> </dl>

 

 



