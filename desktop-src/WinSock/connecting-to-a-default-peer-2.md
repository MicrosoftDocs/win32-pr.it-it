---
description: WSPConnect stabilisce un indirizzo di destinazione predefinito per consentire l'uso di un socket con le successive operazioni Send (WSPSend) e Receive (WSPRecv).
ms.assetid: efd57cb1-9736-4527-8e20-ab9304e3a8f6
title: Connessione a un peer predefinito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f22ca4aff0cdc8560459dd2571d79a71a85fcc71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307009"
---
# <a name="connecting-to-a-default-peer"></a>Connessione a un peer predefinito

Per un socket associato a un protocollo senza connessione, l'operazione eseguita da [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) è semplicemente la definizione di un indirizzo di destinazione predefinito, in modo che il Socket possa essere utilizzato con le successive operazioni di invio e ricezione orientate alla connessione ([**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) e [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85))). Tutti i datagrammi ricevuti da un indirizzo diverso dall'indirizzo di destinazione specificato verranno rimossi.

 

 
