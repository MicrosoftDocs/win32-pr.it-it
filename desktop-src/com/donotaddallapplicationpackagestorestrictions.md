---
title: DoNotAddAllApplicationPackagesToRestrictions
description: Determina se RPCSS aggiunge automaticamente un \_ SID ALL APPLICATION \_ PACKAGES alle restrizioni COM per impostazione predefinita.
ms.assetid: 4DC1237E-F3EF-40EA-8E64-57320F0C4CC5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1608d49d7e5bebc977ace8e59e4b31c5b13da8ab4f743e89095b9f31632453c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117737007"
---
# <a name="donotaddallapplicationpackagestorestrictions"></a>DoNotAddAllApplicationPackagesToRestrictions

Determina se RPCSS aggiunge automaticamente un \_ SID ALL APPLICATION \_ PACKAGES alle restrizioni COM per impostazione predefinita.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DoNotAddAllApplicationPackagesToRestrictions = value
```

## <a name="remarks"></a>Commenti

Si tratta di **un valore \_ DWORD REG.**



| Valore | Descrizione                                                                               |
|-------|-------------------------------------------------------------------------------------------|
| 0     | Disabilita le Windows Store al momento della migrazione da Windows 7 a Windows 8.                   |
| 1     | Non aggiunge il \_ \_ SID ALL APPLICATION PACKAGES alle restrizioni COM. Questo è il valore predefinito. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazione della sicurezza per le applicazioni COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




