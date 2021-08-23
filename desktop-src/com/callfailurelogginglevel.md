---
title: CallFailureLoggingLevel
description: Imposta il livello di dettaglio delle voci del registro eventi relative alle chiamate non riuscite ai componenti.
ms.assetid: 68a7210c-f2a0-4db6-9759-08ff9132a563
keywords:
- Valore com del Registro di sistema CallFailureLoggingLevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 819d132a8cd0f1741eb3b825a17f02387b200e80f2dba6913821e77f9a0913cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793821"
---
# <a name="callfailurelogginglevel"></a>CallFailureLoggingLevel

Imposta il livello di dettaglio delle voci del registro eventi relative alle chiamate non riuscite ai componenti.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   CallFailureLoggingLevel = value
```

## <a name="remarks"></a>Commenti

Si tratta di **un valore \_ DWORD REG.**



| Valore | Descrizione                                                                            |
|-------|----------------------------------------------------------------------------------------|
| 1     | Registrare sempre gli errori durante una chiamata nel processo del server COM.                           |
| 2     | Non registrare mai gli errori durante una chiamata nel processo del server COM. Si tratta del valore predefinito. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazione della sicurezza per le applicazioni COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




