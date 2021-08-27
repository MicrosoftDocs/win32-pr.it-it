---
title: Istanza di Gestione tabelle di routing
description: Un'istanza è una tabella separata utilizzata dal gestore tabelle di routing per gestire le informazioni di routing su un subset di interfacce.
ms.assetid: a17233fc-2c40-4d00-8a6b-86f08fef5690
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3215baf7a3cf093ecf47e8cf9965a71e75dea17a0527949e68b2c5f929d336ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073921"
---
# <a name="routing-table-manager-instance"></a>Istanza di Gestione tabelle di routing

Un'istanza è una tabella separata utilizzata dal gestore tabelle di routing per gestire le informazioni di routing su un subset di interfacce. Le istanze vengono in genere usate per consentire a un router fisico di fungere da set di router virtuali, un router virtuale per ogni rete logica.

Attualmente, il gestore tabelle di routing supporta una sola istanza (identificata come zero, il valore predefinito). Il client può eseguire la registrazione con altre istanze, ma nessun router virtuale, ad eccezione di quello predefinito, viene riconosciuto o usato dal gestore router.

 

 




