---
title: InvalidSecurityDescriptorLoggingLevel
description: Imposta il livello di dettaglio delle voci del registro eventi relative a descrittori di sicurezza non validi per le autorizzazioni di avvio e accesso dei componenti.
ms.assetid: 44f680b8-083d-44f0-a353-e66b87787ab7
keywords:
- Valore InvalidSecurityDescriptorLoggingLevel del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25ac333a7cb8b54f383f93a71131cbb0a9314466
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328279"
---
# <a name="invalidsecuritydescriptorlogginglevel"></a>InvalidSecurityDescriptorLoggingLevel

Imposta il livello di dettaglio delle voci del registro eventi relative a descrittori di sicurezza non validi per le autorizzazioni di avvio e accesso dei componenti.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   InvalidSecurityDescriptorLoggingLevel = value
```

## <a name="remarks"></a>Commenti

Si tratta di un valore **reg \_ DWORD** .



| Valore | Descrizione                                                                                                                                                                    |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | Registra sempre gli errori quando COM trova un descrittore di sicurezza non valido. Si tratta del valore predefinito.                                                                                  |
| 2     | Non registrare mai errori quando COM trova un descrittore di sicurezza non valido. Non è consigliabile disabilitare la registrazione degli eventi, in quanto può rendere più difficile la diagnosi dei problemi. |



 

Se si impostano direttamente i descrittori di sicurezza per le autorizzazioni di avvio e di accesso, chiamati comunemente ACL, è possibile creare un descrittore di sicurezza il cui significato non può essere interpretato in modo non ambiguo. COM crea una voce del registro eventi quando rileva un descrittore di sicurezza non valido.

Si noti che [**ActivationFailureLoggingLevel**](activationfailurelogginglevel.md) e [**CallFailureLoggingLevel**](callfailurelogginglevel.md) non sono in grado di controllare la registrazione di errori descrittori di sicurezza non validi Usare **InvalidSecurityDescriptorLoggingLevel** per il controllo completo di questa funzionalità.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazione della sicurezza per le applicazioni COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




