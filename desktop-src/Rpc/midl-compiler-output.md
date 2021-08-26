---
title: Output del compilatore MIDL
description: Con i file IDL e ACF come input, il compilatore MIDL genera fino a cinque file di origine in linguaggio C.
ms.assetid: 151bd643-1da0-4b33-b8a3-3d7037e63319
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aea74b77d8e709d8a71d3c84f457d301bb38d8c35bdccaa77e9e3033d08ed70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019691"
---
# <a name="midl-compiler-output"></a>Output del compilatore MIDL

Con i file IDL e ACF come input, il compilatore MIDL genera fino a cinque file di origine in linguaggio C. Per impostazione predefinita, il compilatore MIDL usa il nome file di base del file IDL come parte dei file stub generati. Quando nel nome del file di base sono presenti più di sei caratteri, alcuni file system potrebbero non accettare il nome stub completo. La tabella seguente illustra le convenzioni usate per i nomi di file.



| File        | Parte predefinita del nome del file di base | Esempio      |
|-------------|-----------------------------------|--------------|
| File IDL    | ---                               | Abcdefgh.idl |
| Intestazione      | .h                                | Abcdef.h     |
| Stub client | \_c.c                             | Abcdef \_ c.c  |
| Stub del server | \_s.c                             | Abcdef \_ s.c  |



 

 

 




