---
title: Interfacce RAS
description: Un'interfaccia rappresenta una rete che può essere raggiunta tramite un adapter LAN o WAN.
ms.assetid: 26eec1af-43b4-4719-bec9-bc3f9b0341e6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dea285a625377709a4eca3bc8b9947106c2f5cfd
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/23/2019
ms.locfileid: "103857834"
---
# <a name="ras-interfaces"></a>Interfacce RAS

Un'interfaccia rappresenta una rete che può essere raggiunta tramite un adapter LAN o WAN. Ogni interfaccia ha un identificatore univoco sul router. Le interfacce attive hanno un adapter che fornisce la connettività alla rete che rappresentano. Le interfacce inattive non dispongono di un adapter che fornisce la connettività, a meno che un amministratore non abbia disabilitato l'interfaccia dopo che era già presente un adapter.

Il routing di un pacchetto a una rete rappresentata da un'interfaccia provocherà l'allocazione di un adapter per l'interfaccia da parte del router e la connessione WAN alla rete remota. L'allocazione di un adapter a un'interfaccia viene definita *Binding*.

Le interfacce sono oggetti gestibili. Ogni interfaccia viene visualizzata come riga nella tabella di interfaccia del MIB SNMP appropriato.