---
title: CallFailureLoggingLevel
description: Imposta il livello di dettaglio delle voci del registro eventi sulle chiamate non riuscite ai componenti.
ms.assetid: 68a7210c-f2a0-4db6-9759-08ff9132a563
keywords:
- Valore CallFailureLoggingLevel del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4432f21f333d5aa5f8b3cebbd6f0fa339cf0f13a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855886"
---
# <a name="callfailurelogginglevel"></a>CallFailureLoggingLevel

Imposta il livello di dettaglio delle voci del registro eventi sulle chiamate non riuscite ai componenti.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   CallFailureLoggingLevel = value
```

## <a name="remarks"></a>Commenti

Si tratta di un valore **reg \_ DWORD** .



| Valore | Descrizione                                                                            |
|-------|----------------------------------------------------------------------------------------|
| 1     | Registrare sempre gli errori durante una chiamata nel processo del server COM.                           |
| 2     | Non registrare mai errori durante una chiamata nel processo del server COM. Si tratta del valore predefinito. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazione della sicurezza per le applicazioni COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




