---
title: Routine di _aulldiv
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
ms.openlocfilehash: 2fce346ee9608f20667c76841a63a8a3fb9cfe21
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2020
ms.locfileid: "104472203"
---
# <a name="_aulldiv-routine"></a>\_Routine aulldiv

Divide due interi **ULONGLONG** .
Ad esempio, per dividere due valori UInt64, il compilatore potrebbe generare una chiamata alla routine **\_ aulldiv** .

## <a name="remarks"></a>Commenti

La routine **\_ aulldiv** è una routine di supporto per il compilatore C.
Il fatto che il compilatore usi **\_ aulldiv** dipenda completamente dal set di ottimizzazione.

Questa funzione viene utilizzata solo su piattaforme x86.
