---
title: routine _aulldiv
description: Divide due interi ULONGLONG.
ms.assetid: na
ms.topic: reference
ms.date: 04/29/2019
ms.keywords: _aulldiv, ntoskrnl.exe!_aulldiv
topic_type:
- APIRef
api_type:
- DllExport
api_location:
- ntoskrnl.exe
api_name:
- _aulldiv
targetos: Windows
ms.openlocfilehash: 0a37dd5a88d668ed92d79f7bc939119068840741a54cfacb5a15119fcefb774e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538901"
---
# <a name="_aulldiv-routine"></a>\_Routine aulldiv

Divide due **interi ULONGLONG.**
Ad esempio, per dividere due valori uint64 il compilatore potrebbe generare una chiamata alla routine **\_ aulldiv.**

## <a name="remarks"></a>Commenti

La **\_ routine aulldiv** è una routine helper per il compilatore C.
Il fatto che il **\_ compilatore usi aulldiv** dipende completamente dal set di ottimizzazione.

Questa funzione viene usata solo nelle piattaforme x86.
