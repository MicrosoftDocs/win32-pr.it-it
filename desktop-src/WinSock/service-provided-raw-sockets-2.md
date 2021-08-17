---
description: Un socket non elaborato è un tipo di socket che consente l'accesso al provider di trasporto sottostante. L'uso di socket non elaborati quando si esegue il porting delle applicazioni in Winsock non è consigliato per diversi motivi.
ms.assetid: b78c75b7-255c-4e85-9a88-0efb3b5f0e51
title: Socket non elaborati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9c1522c2b8499e2ba8f1bb693513105804ec936fc2224fccaa55dd90a1b0dc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740535"
---
# <a name="raw-sockets"></a>Socket non elaborati

Un socket non elaborato è un tipo di socket che consente l'accesso al provider di trasporto sottostante. L'uso di socket non elaborati quando si esegue il porting delle applicazioni in Winsock non è consigliato per diversi motivi.

La Windows Sockets non impone a un provider di servizi Winsock di supportare socket non elaborati, ad esempio socket di tipo **SOCK \_ RAW.** Tuttavia, i provider di servizi sono invitati a fornire il supporto per socket non elaborati. Un'applicazione conforme Windows Sockets che vuole usare socket non elaborati deve tentare di aprire il socket con la chiamata [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) e se non riesce a usare un altro tipo di socket o indicare l'errore per l'utente.

In Windows 7, Windows Server 2008 R2, Windows Vista e Windows XP con Service Pack 2 (SP2), la possibilità di inviare traffico su socket non elaborati è stata limitata in diversi modi. Per altre informazioni, vedere [TCP/IP Raw Sockets](tcp-ip-raw-sockets-2.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Porting di applicazioni socket in Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket)
</dt> <dt>

[Socket non elaborati TCP/IP](tcp-ip-raw-sockets-2.md)
</dt> <dt>

[Considerazioni sulla programmazione di Winsock](winsock-programming-considerations.md)
</dt> </dl>

 

 



