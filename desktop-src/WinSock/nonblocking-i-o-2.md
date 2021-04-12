---
description: Se un socket si trova in modalità non di blocco, tutte le operazioni di I/O devono essere completate immediatamente o restituire il codice di errore WSAEWOULDBLOCK che indica che l'operazione non può essere completata immediatamente.
ms.assetid: badd279b-ec71-4761-9066-d501aa2485c2
title: Input/output non di blocco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df9f6fec896c8daf1998e71a20a23a296b7b5a72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526130"
---
# <a name="nonblocking-inputoutput"></a>Input/output non di blocco

Se un socket si trova in modalità non di blocco, tutte le operazioni di I/O devono essere completate immediatamente o restituire il codice di errore WSAEWOULDBLOCK che indica che l'operazione non può essere completata immediatamente. Nel secondo caso, è necessario un meccanismo per individuare quando è opportuno riprovare a eseguire l'operazione con la previsione che l'operazione avrà esito positivo. A questo scopo è stato definito un set di eventi di rete. È possibile eseguire il polling o l'attesa di questi eventi tramite [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85))oppure è possibile registrarli per il recapito asincrono chiamando [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) o [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)). Per ulteriori informazioni, vedere [notifica degli eventi di rete](notification-of-network-events-2.md) .

 

 
