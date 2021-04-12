---
title: SRPTrustLevel
description: Imposta il livello di attendibilità del criterio di restrizione software per le applicazioni.
ms.assetid: 2ec10eb5-f83a-4ce7-8e03-36cdafadf169
keywords:
- Valore SRPTrustLevel del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c1e9290cbe04cfe33e1192b95b86ca03fd5ea5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395658"
---
# <a name="srptrustlevel"></a>SRPTrustLevel

Imposta il livello di attendibilità del criterio di restrizione software per le applicazioni.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      SRPTrustLevel = value
```

## <a name="remarks"></a>Commenti

Si tratta di un valore **reg \_ DWORD** disponibile a partire da Windows XP.



| Valore                                 | Descrizione                                                                          |
|---------------------------------------|--------------------------------------------------------------------------------------|
| 0x0 (LEVELID più sicuro non \_ \_ consentito)      | L'applicazione non è consentita per l'accesso e i privilegi utente sensibili alla sicurezza. |
| 0x40000 (SAFE \_ LEVELID \_ FULLYTRUSTED) | L'applicazione dispone di accesso illimitato ai privilegi dell'utente.                    |



 

Se il valore **SRPTrustLevel** non esiste, viene utilizzato il valore predefinito di LEVELID più sicuro non \_ \_ consentito. Se **SRPTrustLevel** è del tipo errato o non è compreso nell'intervallo, com restituisce l'errore COMAdmin \_ E \_ SAFERINVALID. Se l'attivazione di un ordinamento ha esito negativo a causa dei controlli di attendibilità SRP, COM restituisce l'errore CO \_ E \_ ACTIVATIONFAILED.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sicurezza in COM](security-in-com.md)
</dt> <dt>

[**SRPActivateAsActivatorChecks**](srpactivateasactivatorchecks.md)
</dt> <dt>

[**SRPRunningObjectChecks**](srprunningobjectchecks.md)
</dt> </dl>

 

 




