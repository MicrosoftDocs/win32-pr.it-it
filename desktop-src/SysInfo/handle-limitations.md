---
description: Alcuni oggetti supportano un solo handle alla volta.
ms.assetid: 3eafd0e0-3923-4489-8a0a-63007dd3183a
title: Limitazioni della gestione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99caa991b1ffa0a4e0c02ff32225c3260eb4a016
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233487"
---
# <a name="handle-limitations"></a>Limitazioni della gestione

Alcuni oggetti supportano un solo handle alla volta. Il sistema fornisce l'handle quando un'applicazione crea l'oggetto e invalida l'handle quando l'applicazione elimina definitivamente l'oggetto. Altri oggetti supportano più handle per un singolo oggetto. Il sistema operativo rimuove automaticamente l'oggetto dalla memoria dopo la chiusura dell'ultimo handle per l'oggetto.

Il numero totale di handle aperti nel sistema è limitato solo dalla quantità di memoria disponibile. Alcuni tipi di oggetto supportano un numero limitato di handle per sessione o per processo.

 

 



