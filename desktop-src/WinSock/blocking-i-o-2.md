---
description: La forma più semplice di I/O in Windows Sockets 2 è il blocco di I/O.
ms.assetid: 8ed7e5a8-c577-4b61-9c49-8fd065d84af4
title: Blocco di input/output
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d1c846a22fcf9d10f562a48683c2ead723f9bd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307040"
---
# <a name="blocking-inputoutput"></a>Blocco di input/output

La forma più semplice di I/O in Windows Sockets 2 è il blocco di I/O. Come indicato nelle [modalità e nei flag dell'attributo socket](socket-attribute-flags-and-modes-2.md), per impostazione predefinita i socket vengono creati in modalità di blocco. Qualsiasi operazione di I/O con un socket di blocco non verrà restituita finché l'operazione non è stata completata correttamente. Pertanto, qualsiasi thread può eseguire solo un'operazione di I/O alla volta. Se, ad esempio, un thread esegue un'operazione di ricezione e nessun dato è attualmente disponibile, il thread si bloccherà fino a quando i dati non diventano disponibili e vengono inseriti nel buffer del thread. Sebbene questo sia semplice, non è necessariamente il modo più efficiente per eseguire operazioni di I/O (vedere [pseudo-blocco e vero blocco](pseudo-vs--true-blocking-2.md) per altre informazioni).

 

 



