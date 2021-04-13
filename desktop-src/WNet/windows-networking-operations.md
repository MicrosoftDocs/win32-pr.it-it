---
title: Operazioni di rete di Windows
description: Un'applicazione può utilizzare le funzioni WNet per esplorare, aggiungere o annullare le connessioni di rete in qualsiasi punto della gerarchia di rete.
ms.assetid: 8f17af6c-e1b2-4b53-b3f0-698d42beb704
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e30326d9ad1299e577c65586cff3df3010c086f8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337919"
---
# <a name="windows-networking-operations"></a>Operazioni di rete di Windows

Un'applicazione può utilizzare le funzioni WNet per esplorare, aggiungere o annullare le connessioni di rete in qualsiasi punto della gerarchia di rete.

Una *connessione permanente* è una connessione di rete ripristinata automaticamente dal sistema quando l'utente esegue l'accesso. È possibile chiamare le funzioni [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) (o [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a)) e [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a) per controllare se una connessione di rete è permanente da una sessione a quella successiva.

Per trovare il nome utente predefinito o il nome utente utilizzato per stabilire una connessione di rete, chiamare la funzione [**WNetGetUser**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera) .

Oltre a chiamare le funzioni WNet, un processo può utilizzare anche mailslot e named pipe per comunicare con un altro processo. Per altre informazioni, vedere [mailslot](/windows/desktop/ipc/mailslots) e [Pipes](/windows/desktop/ipc/pipes).

 

 