---
description: La forma più semplice di I/O in Windows Sockets 2 è il blocco dell'I/O.
ms.assetid: 8ed7e5a8-c577-4b61-9c49-8fd065d84af4
title: Blocco di input/output
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c65991f4401a5069718fb39172a9d59db4536a83ab4e2f99948d7c300eb4042
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118322615"
---
# <a name="blocking-inputoutput"></a>Blocco di input/output

La forma più semplice di I/O in Windows Sockets 2 è il blocco dell'I/O. Come accennato in [Flag e modalità degli attributi](socket-attribute-flags-and-modes-2.md)socket, i socket vengono creati in modalità di blocco per impostazione predefinita. Qualsiasi operazione di I/O con un socket di blocco non verrà restituita fino al completamento dell'operazione. Qualsiasi thread può quindi eseguire solo un'operazione di I/O alla volta. Ad esempio, se un thread esegue un'operazione di ricezione e non sono attualmente disponibili dati, il thread si blocca fino a quando i dati non diventano disponibili e vengono inseriti nel buffer del thread. Anche se questo è semplice, non è necessariamente il modo più efficiente per eseguire operazioni di I/O (per altre informazioni, vedere Pseudo blocco e [Blocco](pseudo-vs--true-blocking-2.md) vero).

 

 



