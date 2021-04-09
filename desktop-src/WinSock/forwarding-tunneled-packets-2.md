---
description: Esiste una limitazione nel codice che riceve pacchetti incapsulati (tunneling) e li demultiplexi a un'interfaccia specifica.
ms.assetid: 6148fca7-adf4-460d-afd6-79c43285af6c
title: Pacchetti con tunneling di inoltri IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f95f88a90a358317cf46516808a96f93b792dd5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879213"
---
# <a name="ipv6-forwarding-tunneled-packets"></a>Pacchetti con tunneling di inoltri IPv6

Esiste una limitazione nel codice che riceve pacchetti incapsulati (tunneling) e li demultiplexi a un'interfaccia specifica. Se si vuole inoltrare i pacchetti con tunneling ricevuti tramite un tunnel configurato, è necessario abilitare l'inoltramento su tutte le interfacce 6-over-4 e sull'interfaccia \# 2. L'abilitazione dell'invio solo sull'interfaccia \# 2 non funziona. In genere, quando si configura un router, si Abilita l'invio in tutte le interfacce ad eccezione di loopback.

 

 



