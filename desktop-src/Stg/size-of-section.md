---
title: Dimensione della sezione
description: Il tipo di dati della sezione dimensione indica le dimensioni, in byte, della sezione.
ms.assetid: 6438fbce-42b9-4b16-a6b0-80c80246e546
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71b19df1c2f9a65f6952855a4ab325565c759af
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221999"
---
# <a name="size-of-section"></a>Dimensione della sezione

Il tipo di dati della sezione dimensione indica le dimensioni, in byte, della sezione. Poiché le dimensioni della sezione sono i primi 4 byte, le sezioni possono essere copiate come una matrice di byte. Le dimensioni della sezione devono essere sempre un multiplo di quattro.

Ad esempio, una sezione vuota, ovvero una con zero proprietà, avrà un numero di byte pari a otto (il conteggio dei byte **DWORD** e il numero **DWORD** di proprietà). La sezione stessa conterrebbe gli 8 byte: **08 00 00 00 00 00 00 00**.

 

 




