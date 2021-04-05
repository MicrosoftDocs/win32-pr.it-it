---
description: WSPGetSockName viene utilizzato per recuperare l'indirizzo locale per i socket associati.
ms.assetid: 5f3c9aa8-97fe-48a1-a3f5-156c9bddb1b2
title: Determinazione dei nomi locali e remoti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 265cf8013dcadaedbef786ab78f48e63de81a992
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049488"
---
# <a name="determining-local-and-remote-names"></a>Determinazione dei nomi locali e remoti

[**WSPGetSockName**](/previous-versions/windows/desktop/legacy/ms742280(v=vs.85)) viene utilizzato per recuperare l'indirizzo locale per i socket associati. Questa operazione è particolarmente utile quando viene effettuata una chiamata [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) senza eseguire prima un [**WSPBind**](/previous-versions/windows/hardware/network/ff566268(v=vs.85)) ; **WSPGetSockName** fornisce l'unico mezzo per determinare l'associazione locale che è stata impostata in modo implicito dal provider.

Una volta configurata una connessione, è possibile usare [**WSPGetPeerName**](/previous-versions/windows/desktop/legacy/ms742278(v=vs.85)) per determinare l'indirizzo del peer a cui è connesso un socket.

 

 
