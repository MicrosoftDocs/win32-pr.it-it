---
title: Flag di test
description: Flag di test
ms.assetid: d103a96e-8d55-413d-ac84-15c3d8dccfbe
keywords:
- MCI_TEST flag
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 837b7812a904ed39fa0350d703b1525bbffa6f981b4736d25927840395932f32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117801477"
---
# <a name="the-test-flag"></a>Flag di test

Il flag "test" (MCI TEST) esegue una query sul dispositivo per \_ determinare se è in grado di eseguire il comando. Il dispositivo restituisce un errore se non è in grado di eseguire il comando. Non restituisce alcun errore se è in grado di gestire il comando. Quando si specifica questo flag, MCI restituisce il controllo all'applicazione senza eseguire il comando.

Questo flag è supportato dai dispositivi digital-video e VCR per tutti i comandi tranne [**open**](open.md) ([**MCI \_ OPEN**](mci-open.md)) e [**close**](close.md) ([**MCI \_ CLOSE**](mci-close.md)).

 

 




