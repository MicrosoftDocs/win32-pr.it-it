---
description: In alcuni casi i socket aggiunti a una sessione multipoint possono avere alcune differenze di comportamento rispetto ai socket da punto a punto.
ms.assetid: e59b701f-f85f-4fd6-8d6d-e46199250c22
title: Bit di flag per WSASocket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd1bbe8a282fe0255e3efd9889216b7d44aee2a41feedb611ba5c2b1d38bae68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132474"
---
# <a name="flag-bits-for-wsasocket"></a>Bit di flag per WSASocket

In alcuni casi i socket aggiunti a una sessione multipoint possono avere alcune differenze di comportamento rispetto ai socket da punto a punto. Ad esempio, un socket foglia d in uno schema del piano dati rooted può inviare informazioni \_ solo al partecipante radice \_ d. Ciò crea la necessità che l'applicazione sia in grado di indicare l'uso previsto di un socket coincidente con la sua creazione. Questa operazione viene eseguita tramite bit a quattro flag che possono essere impostati nel *parametro dwFlags* su [**WSASocket:**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)

-   WSA FLAG MULTIPOINT C ROOT, per la creazione di un socket che funge da radice c e consentito solo se un piano di controllo rooted è indicato nella voce \_ \_ \_ \_ \_ [**WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) corrispondente.
-   WSA FLAG MULTIPOINT C LEAF, per la creazione di un socket che funge da foglia c e consentito solo se XP1 SUPPORT MULTIPOINT è indicato nella voce \_ \_ \_ \_ \_ \_ \_ [**WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) corrispondente.
-   WSA FLAG MULTIPOINT D ROOT, per la creazione di un socket che funge da radice d e consentito solo se un piano dati rooted è indicato nella voce \_ \_ \_ \_ \_ [**WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) corrispondente.
-   WSA FLAG MULTIPOINT D LEAF, per la creazione di un socket che funge da foglia d e consentito solo se XP1 SUPPORT MULTIPOINT è indicato nella voce \_ \_ \_ \_ \_ \_ \_ [**WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) corrispondente.

Si noti che quando si crea un socket multipunto, è necessario impostare esattamente uno dei due flag del piano di controllo e uno dei due flag del piano dati nel parametro *dwFlags* di [**WSASocket.**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) Di conseguenza, le quattro possibilità per la creazione di socket multipoint sono:

-   "c \_ root/d \_ root"
-   "c \_ root/d \_ leaf"
-   "c \_ leaf/d \_ root"
-   "c \_ leaf /d \_ leaf"

 

 
