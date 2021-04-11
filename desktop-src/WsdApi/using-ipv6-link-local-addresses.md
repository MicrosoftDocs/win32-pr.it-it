---
description: L'indirizzamento locale del collegamento IPv6 nei messaggi SOAP costituisce una sfida univoca, poiché gli indirizzi locali del collegamento IPv6 richiedono un ID ambito come significativo, ma l'ID ambito ha solo significato per il computer locale.
ms.assetid: 63495335-e447-4564-b669-0896c7aac63f
title: Uso degli indirizzi locali per il collegamento IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c89356042e8a71b0af19337b7013b8abd1e8a354
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130390"
---
# <a name="using-ipv6-link-local-addresses"></a>Uso degli indirizzi locali per il collegamento IPv6

L'indirizzamento locale del collegamento IPv6 nei messaggi SOAP costituisce una sfida univoca, poiché gli indirizzi locali del collegamento IPv6 richiedono un ID ambito come significativo, ma l'ID ambito ha solo significato per il computer locale. Tutte le implementazioni di client e dispositivi devono rimuovere l'ID ambito prima di inviare un indirizzo locale del collegamento IPv6 in un messaggio SOAP. Inoltre, quando un messaggio viene ricevuto da un indirizzo locale rispetto al collegamento IPv6, è necessario che l'interfaccia in cui è stato ricevuto il messaggio sia nota, quindi è possibile ricostruire l'indirizzo locale completo del collegamento con ID ambito.

 

 



