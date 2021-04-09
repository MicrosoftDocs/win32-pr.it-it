---
title: Output del compilatore MIDL
description: Con i file IDL e ACF come input, il compilatore MIDL genera fino a cinque file di origine in linguaggio C.
ms.assetid: 151bd643-1da0-4b33-b8a3-3d7037e63319
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebb45bb369ea9d5faa695bf2658f3bafe2b3cb3d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044348"
---
# <a name="midl-compiler-output"></a>Output del compilatore MIDL

Con i file IDL e ACF come input, il compilatore MIDL genera fino a cinque file di origine in linguaggio C. Per impostazione predefinita, il compilatore MIDL usa il nome del file di base del file IDL come parte dei file stub generati. Quando nel nome del file di base sono presenti più di sei caratteri, è possibile che alcuni file System non accettino il nome dello stub completo. Nella tabella seguente vengono illustrate le convenzioni utilizzate per i nomi di file.



| File        | Parte predefinita del nome del file di base | Esempio      |
|-------------|-----------------------------------|--------------|
| File IDL    | ---                               | Abcdefgh. idl |
| Intestazione      | .h                                | Abcdef. h     |
| Stub client | \_c. c                             | Abcdef \_ c. c  |
| Stub server | \_s. c                             | Abcdef \_ s. c  |



 

 

 




