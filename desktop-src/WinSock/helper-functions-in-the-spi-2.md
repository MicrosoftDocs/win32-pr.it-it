---
description: NSPGetServiceClassInfo
ms.assetid: 6fbe9c0c-ac1f-4f2b-a542-eae2195b1335
title: Funzioni helper in SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e687529bf1ede1598225708cf288e49bb7e9b5c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306954"
---
# <a name="helper-functions-in-the-spi"></a>Funzioni helper in SPI

-   [**NSPGetServiceClassInfo**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo)

La funzione [**NSPGetServiceClassInfo**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo) recupera le informazioni sullo schema della classe di servizio mantenute da un provider dello spazio dei nomi. Viene inoltre utilizzata dalla DLL di Windows Sockets 2 nell'implementazione di [**WSAGetServiceClassNameByClassId**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida).

Le macro seguenti sono definite nel file di intestazione *Svcguid. h* e possono contribuire al mapping tra le classi di servizio note e questi spazi dei nomi.

| Nome macro                                                                              | Descrizione                                                                                                                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| **SVCID \_ TCP (porta)**<br/> **\_UDP SVCID (porta)**<br/>                         | Data una porta TCP o UDP per il protocollo Internet, restituisce il GUID.                                                                               |
| **\_SVCID \_ TCP (Guid)**<br/> **\_UDP SVCID \_ (Guid)**<br/>                 | Restituisce **true** se il GUID per TCP o UDP è compreso nell'intervallo consentito.                                                                         |
| **PORTA \_ da \_ SVCID \_ TCP (Guid)**<br/> **PORTA \_ da \_ SVCID \_ UDP (Guid)**<br/> | Restituisce la porta TCP o UDP associata al GUID.                                                                                              |
| **SVCID \_ NetWare (SAPI)**<br/>                                                    | Dato l'identificatore di Service Advertising Protocol (SAP), restituisce il GUID. Questa macro viene usata con lo spazio dei nomi SAP all'interno di un ambiente NetWare. |
| **SAPIDO \_ da \_ SVCID \_ NetWare (Guid)**<br/>                                        | Restituisce l'identificatore SAP di NetWare associato al GUID. Questa macro viene usata con lo spazio dei nomi SAP all'interno di un ambiente NetWare.               |
| **è \_ SVCID \_ NetWare (Guid)**<br/>                                                 | Restituisce **true** se il GUID per NetWare è compreso nell'intervallo consentito. Questa macro viene usata con lo spazio dei nomi SAP all'interno di un ambiente NetWare.    |



 

> [!Note]  
> Il file di intestazione *Svcguid. h* non è incluso automaticamente nel file di intestazione *Winsock2. h* .

 

 

 




