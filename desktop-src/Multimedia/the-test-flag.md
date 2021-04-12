---
title: Flag di test
description: Flag di test
ms.assetid: d103a96e-8d55-413d-ac84-15c3d8dccfbe
keywords:
- Flag di MCI_TEST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a36cddaa186a9be260cf87b7a323a6e05ed9fc4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332527"
---
# <a name="the-test-flag"></a>Flag di test

Il flag "test" ( \_ test MCI) esegue una query sul dispositivo per determinare se può eseguire il comando. Il dispositivo restituisce un errore se non è possibile eseguire il comando. Non restituisce alcun errore se può gestire il comando. Quando si specifica questo flag, MCI restituisce il controllo all'applicazione senza eseguire il comando.

Questo flag è supportato dai dispositivi Digital-video e VCR per tutti i comandi tranne [**Open**](open.md) ([**MCI \_ Open**](mci-open.md)) e [**Close**](close.md) ([**MCI \_ Close**](mci-close.md)).

 

 




