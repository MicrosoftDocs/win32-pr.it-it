---
description: Un socket non elaborato è un tipo di socket che consente l'accesso al provider di trasporto sottostante. Per diversi motivi, non è consigliabile usare i socket non elaborati durante il porting di applicazioni a Winsock.
ms.assetid: b78c75b7-255c-4e85-9a88-0efb3b5f0e51
title: Socket non elaborati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 209c884e85327a7a8c1d21292d9342a0c032747a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131023"
---
# <a name="raw-sockets"></a>Socket non elaborati

Un socket non elaborato è un tipo di socket che consente l'accesso al provider di trasporto sottostante. Per diversi motivi, non è consigliabile usare i socket non elaborati durante il porting di applicazioni a Winsock.

La specifica di Windows Sockets non impone che un provider di servizi Winsock supporti i socket non elaborati, ovvero i socket di tipo **Sock \_ RAW**. Tuttavia, i provider di servizi sono invitati a fornire supporto per socket non elaborato. Un'applicazione compatibile con Windows Sockets che desidera utilizzare i socket non elaborati deve tentare di aprire il socket con la chiamata al [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) e, in caso di esito negativo, tentare di utilizzare un altro tipo di socket o indicare l'errore all'utente.

In Windows 7, Windows Server 2008 R2, Windows Vista e Windows XP con Service Pack 2 (SP2), la possibilità di inviare traffico su socket non elaborati è stata limitata in diversi modi. Per ulteriori informazioni, vedere [TCP/IP raw Sockets](tcp-ip-raw-sockets-2.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Porting delle applicazioni socket in Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[**presa**](/windows/desktop/api/Winsock2/nf-winsock2-socket)
</dt> <dt>

[Socket TCP/IP raw](tcp-ip-raw-sockets-2.md)
</dt> <dt>

[Considerazioni sulla programmazione Winsock](winsock-programming-considerations.md)
</dt> </dl>

 

 



