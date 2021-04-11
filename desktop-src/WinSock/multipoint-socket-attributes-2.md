---
description: Attributi di socket multipoint in Windows Sockets (Winsock).
ms.assetid: f6e779c6-dd9d-470e-aad9-715b69ad8c5f
title: Attributi di socket multipoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5da67fd40c7c3bc7f1e9dbff22a3fef6cdaee4d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226082"
---
# <a name="multipoint-socket-attributes"></a>Attributi di socket multipoint

In alcuni casi, i socket aggiunti a una sessione multipoint possono avere alcune differenze di comportamento rispetto ai socket da punto a punto. Ad esempio, un \_ socket foglia d in uno schema di piano dati radice può inviare informazioni solo al \_ partecipante radice d. In questo modo il client deve essere in grado di indicare l'uso previsto di un socket coincidente con la relativa creazione. Questa operazione viene eseguita tramite quattro flag di attributi multipoint che possono essere impostati tramite il parametro *dwFlags* in [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket):

-   \_ \_ Radice del flag WSA multipoint \_ c \_ , per la creazione di un socket che funge da \_ radice c e consentito solo se un piano di controllo radice è indicato nella voce di [**\_ informazioni WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) corrispondente.
-   Il \_ flag WSA \_ multipoint \_ C \_ foglia, per la creazione di un socket che funge da \_ foglia c e consentito solo se XP1 \_ supporta \_ multipoint è indicato nella voce di [**\_ informazioni WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) corrispondente.
-   FLAG WSA: \_ \_ \_ radice multipoint d \_ , per la creazione di un socket che funge da \_ radice d e consentito solo se un piano dati radice è indicato nella voce di [**\_ informazioni WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) corrispondente.
-   La \_ \_ foglia multipoint \_ d del flag WSA \_ , per la creazione di un socket che funge da \_ foglia d, ed è consentita solo se XP1 \_ supporta \_ multipoint è indicato nella voce di [**\_ informazioni WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) corrispondente.

Quando si crea un socket MultiPoint, esattamente uno dei due flag del piano di controllo e uno dei due flag del piano dati deve essere impostato nel parametro *dwFlags* di [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket). Pertanto, le quattro possibilità per la creazione di socket multipoint sono: "c \_ root/d \_ root", "c \_ root/d \_ Leaf", "c \_ foglia/d \_ root" o "c \_ Leaf/d \_ foglia".

 

 
