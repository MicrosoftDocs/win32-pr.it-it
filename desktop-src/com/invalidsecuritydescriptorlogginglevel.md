---
title: InvalidSecurityDescriptorLoggingLevel
description: Imposta il livello di dettaglio delle voci del registro eventi relative ai descrittori di sicurezza non validi per l'avvio del componente e le autorizzazioni di accesso.
ms.assetid: 44f680b8-083d-44f0-a353-e66b87787ab7
keywords:
- Valore com del Registro di sistema InvalidSecurityDescriptorLoggingLevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c2362b38c19acd8d895e5fa9640475fa401a7d5bd88c8016056df2d22c3a579
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854341"
---
# <a name="invalidsecuritydescriptorlogginglevel"></a>InvalidSecurityDescriptorLoggingLevel

Imposta il livello di dettaglio delle voci del registro eventi relative ai descrittori di sicurezza non validi per l'avvio del componente e le autorizzazioni di accesso.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   InvalidSecurityDescriptorLoggingLevel = value
```

## <a name="remarks"></a>Commenti

Si tratta di **un valore \_ DWORD REG.**



| Valore | Descrizione                                                                                                                                                                    |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | Registra sempre gli errori quando COM rileva un descrittore di sicurezza non valido. Si tratta del valore predefinito.                                                                                  |
| 2     | Non registrare mai errori quando COM rileva un descrittore di sicurezza non valido. Non è consigliabile disabilitare la registrazione degli eventi, perché può rendere più difficile la diagnosi dei problemi. |



 

Se si impostano direttamente i descrittori di sicurezza delle autorizzazioni di avvio e accesso (comunemente denominati ACL), è possibile costruire un descrittore di sicurezza il cui significato non può essere interpretato senza ambiguità. COM crea una voce del registro eventi quando rileva un descrittore di sicurezza non valido.

Si noti che [**ActivationFailureLoggingLevel**](activationfailurelogginglevel.md) e [**CallFailureLoggingLevel**](callfailurelogginglevel.md) non hanno alcun controllo sulla registrazione degli errori del descrittore di sicurezza non validi. Usare **InvalidSecurityDescriptorLoggingLevel** per il controllo completo su questa funzionalità.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazione della sicurezza per le applicazioni COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




