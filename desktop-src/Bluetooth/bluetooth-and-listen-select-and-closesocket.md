---
title: Bluetooth e ascolto, selezione e chiamata closesocket
description: Bluetooth usa le funzioni Listen, Select e chiamata closesocket senza alcuna modifica dalla programmazione standard di Windows Sockets.
ms.assetid: b64440de-bc63-4e3b-bfd9-5cf783f36c23
keywords:
- Bluetooth
- chiamata closesocket
- ascolto
- Proprietà
- Bluetooth e ascolto
- Bluetooth e ascolto, selezionare
- Bluetooth e ascolto, selezione e chiamata closesocket
- ascolto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e442cfc0593ab5be297902487c7c3ccdf056b4e0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473502"
---
# <a name="bluetooth-and-listen-select-and-closesocket"></a>Bluetooth e ascolto, selezione e chiamata closesocket

Bluetooth usa le funzioni [**Listen**](/windows/desktop/api/winsock2/nf-winsock2-listen), [**SELECT**](/windows/desktop/api/winsock2/nf-winsock2-select)e [**chiamata closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) senza alcuna modifica dalla programmazione standard di Windows Sockets.

Come per i socket di Windows, la funzione [**chiamata closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) libera le risorse associate al socket.

Quando si chiama la funzione [**Listen**](/windows/desktop/api/winsock2/nf-winsock2-listen) , è consigliabile usare un valore basso per il parametro *backlog* (in genere da 2 a 4), perché vengono accettate solo alcune connessioni client. In questo modo si riducono le risorse di sistema allocate per l'utilizzo da parte del socket di ascolto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**chiamata closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket)
</dt> <dt>

[**ascoltare**](/windows/desktop/api/winsock2/nf-winsock2-listen)
</dt> <dt>

[**Selezionare**](/windows/desktop/api/winsock2/nf-winsock2-select)
</dt> </dl>

 

 