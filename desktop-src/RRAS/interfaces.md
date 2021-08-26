---
title: Interfacce RAS
description: Un'interfaccia rappresenta una rete raggiungibile tramite una scheda LAN o WAN.
ms.assetid: 26eec1af-43b4-4719-bec9-bc3f9b0341e6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef716e0db05fe37a0a7d326fbf5f8da878a0628d1deec9e996fcc49d917cc051
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030141"
---
# <a name="ras-interfaces"></a>Interfacce RAS

Un'interfaccia rappresenta una rete raggiungibile tramite una scheda LAN o WAN. Ogni interfaccia ha un identificatore univoco sul router. Le interfacce attive dispongono di una scheda che fornisce connettività alla rete che rappresentano. Le interfacce inattive non dispongono di un adattatore che fornisce la connettività, a meno che un amministratore non abbia disabilitato l'interfaccia dopo che aveva già un adattatore.

Se si instrada un pacchetto a una rete rappresentata da un'interfaccia, il router alloca una scheda per tale interfaccia e stabilisce una connessione WAN alla rete remota. L'allocazione di un adattatore a un'interfaccia viene definita *associazione*.

Le interfacce sono oggetti gestibili. Ogni interfaccia viene visualizzata come riga nella tabella dell'interfaccia del MIB SNMP appropriato.