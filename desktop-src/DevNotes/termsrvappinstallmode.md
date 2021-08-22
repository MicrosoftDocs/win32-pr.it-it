---
description: Determina se Terminal Server è in modalità INSTALL.
ms.assetid: edf362e6-c1a4-49fe-8e07-1188c66616be
title: Funzione TermsrvAppInstallMode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TermsrvAppInstallMode
api_type:
- DllExport
api_location:
- Kernel32.dll
ms.openlocfilehash: f6bf6408fb7bd72b1757b8ca2219e1bbd2cc612829359fdcaf090786e8e7e98b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119570891"
---
# <a name="termsrvappinstallmode-function"></a>Funzione TermsrvAppInstallMode

\[Questa funzione non è supportata e non deve essere usata. Può cambiare o scomparire completamente senza preavviso.\]

Determina se Terminal Server è in modalità INSTALL.

## <a name="syntax"></a>Sintassi


```C++
BOOL TermsrvAppInstallMode(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Questa funzione restituisce **TRUE se** Terminal Server è in modalità INSTALL e **FALSE** se è in modalità EXECUTE.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Kernel32.dll</dt> </dl> |



 

 




