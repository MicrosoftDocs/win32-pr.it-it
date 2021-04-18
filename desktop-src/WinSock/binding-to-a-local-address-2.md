---
description: Prima che un Socket possa essere usato per configurare una connessione o ricevere una richiesta di connessione, deve essere associato a un indirizzo locale.
ms.assetid: 8767a209-e293-47cd-b503-ff4cffbf6fb4
title: Associazione a un indirizzo locale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39aa022d17a8862e6092c52b18edd1539f2d95ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307044"
---
# <a name="binding-to-a-local-address"></a>Associazione a un indirizzo locale

Prima che un Socket possa essere usato per configurare una connessione o ricevere una richiesta di connessione, deve essere associato a un indirizzo locale. Questa operazione può essere eseguita in modo esplicito chiamando [**WSPBind**](/previous-versions/windows/hardware/network/ff566268(v=vs.85))oppure in modo implicito da [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) se il socket non è associato quando viene chiamata questa funzione.

 

 
