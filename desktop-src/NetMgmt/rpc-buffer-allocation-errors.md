---
title: Errori di allocazione del buffer RPC
description: Poiché la libreria di runtime RPC alloca memoria per i buffer di invio e ricezione, la funzione deve prevedere errori di allocazione RPC.
ms.assetid: be9105df-1183-48d6-8cea-391ca628c8b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d68c484837f1f03bce8a8175ddb343065051e3695eec7c65d8a9de89c15fb5d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745011"
---
# <a name="rpc-buffer-allocation-errors"></a>Errori di allocazione del buffer RPC

Poiché la libreria di runtime RPC alloca memoria per i buffer di invio e ricezione, la funzione deve prevedere errori di allocazione RPC. In caso di errore di allocazione RPC, viene invalidato un handle resumable. Si tratta di un requisito perché le funzioni riutilizzabili non sono riavvolgibili.

 

 




