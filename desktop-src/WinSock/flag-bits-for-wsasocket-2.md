---
description: In alcuni casi, i socket aggiunti a una sessione multipoint possono presentare alcune differenze nel comportamento dei socket da punto a punto.
ms.assetid: e59b701f-f85f-4fd6-8d6d-e46199250c22
title: Bit del flag per WSASocket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51fede5d160d89b08064d8dff1c1a901c048526f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306982"
---
# <a name="flag-bits-for-wsasocket"></a>Bit del flag per WSASocket

In alcuni casi, i socket aggiunti a una sessione multipoint possono presentare alcune differenze nel comportamento dei socket da punto a punto. Ad esempio, un \_ socket foglia d in uno schema di piano dati radice può inviare informazioni solo al \_ partecipante radice d. In questo modo l'applicazione deve essere in grado di indicare l'uso previsto di un socket coincidente con la relativa creazione. Questa operazione viene eseguita tramite un bit di quattro flag che può essere impostato nel parametro *dwFlags* su [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa):

-   \_ \_ Radice del flag WSA multipoint \_ c \_ , per la creazione di un socket che funge da \_ radice c e consentito solo se un piano di controllo radice è indicato nella voce di [**\_ informazioni WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) corrispondente.
-   Il \_ flag WSA \_ multipoint \_ C \_ foglia, per la creazione di un socket che funge da \_ foglia c e consentito solo se XP1 \_ supporta \_ multipoint è indicato nella voce di [**\_ informazioni WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) corrispondente.
-   FLAG WSA: \_ \_ \_ radice multipoint d \_ , per la creazione di un socket che funge da \_ radice d e consentito solo se un piano dati radice è indicato nella voce di [**\_ informazioni WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) corrispondente.
-   La \_ \_ foglia multipoint \_ d del flag WSA \_ , per la creazione di un socket che funge da \_ foglia d, ed è consentita solo se XP1 \_ supporta \_ multipoint è indicato nella voce di [**\_ informazioni WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) corrispondente.

Si noti che quando si crea un socket MultiPoint, esattamente uno dei due flag del piano di controllo e uno dei due flag del piano dati deve essere impostato nel parametro *dwFlags* di [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa). Quindi, le quattro possibilità per la creazione di socket multipoint sono:

-   " \_ radice c radice/d \_ "
-   " \_ foglia radice c/d \_ "
-   " \_ radice foglia/d c \_ "
-   "foglia c \_ /d \_ foglia"

 

 
