---
description: Esiste una limitazione nel codice che riceve pacchetti incapsulati (tunneled) e li demultiplexa a un'interfaccia specifica.
ms.assetid: 6148fca7-adf4-460d-afd6-79c43285af6c
title: Inoltro di pacchetti tunneling IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42138c746ea9d0ec8ea61bc3801b84a97a6bdd4c6fb6de0871e6b74447fdf28b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132434"
---
# <a name="ipv6-forwarding-tunneled-packets"></a>Inoltro di pacchetti tunneling IPv6

Esiste una limitazione nel codice che riceve pacchetti incapsulati (tunneled) e li demultiplexa a un'interfaccia specifica. Se si desidera inoltrare i pacchetti tunnel ricevuti tramite un tunnel configurato, è necessario abilitare l'inoltro su qualsiasi interfaccia 6 su 4 e sull'interfaccia \# 2. La semplice abilitazione dell'inoltro \# sull'interfaccia 2 non funzionerà. In genere, quando si configura un router, si abilita l'inoltro su tutte le interfacce, ad eccezione del loopback.

 

 



