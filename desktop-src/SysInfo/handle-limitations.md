---
description: Alcuni oggetti supportano un solo handle alla volta.
ms.assetid: 3eafd0e0-3923-4489-8a0a-63007dd3183a
title: Gestire le limitazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f194ed8464d2731c15e9b88ae62549f9fa090928c14cf7dc66e139944863b72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117764409"
---
# <a name="handle-limitations"></a>Gestire le limitazioni

Alcuni oggetti supportano un solo handle alla volta. Il sistema fornisce l'handle quando un'applicazione crea l'oggetto e invalida l'handle quando l'applicazione elimina l'oggetto. Altri oggetti supportano più handle per un singolo oggetto. Il sistema operativo rimuove automaticamente l'oggetto dalla memoria dopo la chiusura dell'ultimo handle per l'oggetto.

Il numero totale di handle aperti nel sistema è limitato solo dalla quantità di memoria disponibile. Alcuni tipi di oggetto supportano un numero limitato di handle per sessione o per processo.

 

 



