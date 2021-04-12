---
title: Errori di allocazione del buffer RPC
description: Poiché la libreria di runtime RPC alloca memoria per i buffer di invio e di ricezione, la funzione dovrebbe prevedere errori di allocazione RPC.
ms.assetid: be9105df-1183-48d6-8cea-391ca628c8b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbe48c113d644447b5ff7b69988f2534d7de3a9e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329852"
---
# <a name="rpc-buffer-allocation-errors"></a>Errori di allocazione del buffer RPC

Poiché la libreria di runtime RPC alloca memoria per i buffer di invio e di ricezione, la funzione dovrebbe prevedere errori di allocazione RPC. In caso di errore di allocazione RPC, un handle ripristinabile viene invalidato. Questo è un requisito perché le funzioni ripristinabili non sono riavvolgibili.

 

 




