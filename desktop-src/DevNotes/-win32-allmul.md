---
title: Routine di _allmul
description: Moltiplica due Integer LONGLONG o ULONGLONG.
ms.assetid: na
ms.topic: reference
ms.date: 04/29/2019
ms.keywords: _allmul, ntoskrnl.exe!_allmul
topic_type:
- APIRef
api_type:
- DllExport
api_location:
- ntoskrnl.exe
api_name:
- _allmul
targetos: Windows
ms.openlocfilehash: a82a4d56ecb657e19b9849d10c9b51521af6c262
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2020
ms.locfileid: "104046221"
---
# <a name="_allmul-routine"></a>\_Routine allmul

Moltiplica due integer **LONGLONG** o **ULONGLONG** .
Ad esempio, per moltiplicare due valori Int64, il compilatore potrebbe generare una chiamata alla routine **\_ allmul** .

## <a name="remarks"></a>Commenti

La routine **\_ allmul** è una routine di supporto per il compilatore C.
Il fatto che il compilatore usi **\_ allmul** dipenda completamente dal set di ottimizzazione.

Questa routine viene utilizzata solo su piattaforme x86.
