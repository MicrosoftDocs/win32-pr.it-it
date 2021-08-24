---
description: Chiamato dal compilatore quando nella funzione sono presenti più pagine di variabili locali.
ms.assetid: 154dd992-88b5-44a4-9594-5d13afb71c28
title: routine _chkstk
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b129b73801c6c18b63b10ac61898ee13a9c5d4f1f0422678bbfe5af82d5b44f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538836"
---
# <a name="_chkstk-routine"></a>\_Routine chkstk

Chiamato dal compilatore quando nella funzione sono presenti più pagine di variabili locali.

## <a name="remarks"></a>Commenti

\_Chkstk Routine è una routine helper per il compilatore C. Per i compilatori x86, la routine chkstk viene chiamata quando le variabili locali superano \_ i 4.000 byte. Per i compilatori x64 è 8K.

 

 



