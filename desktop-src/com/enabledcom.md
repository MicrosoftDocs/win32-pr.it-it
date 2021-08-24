---
title: Enabledcom
description: Controlla i criteri di attivazione e chiamata globali del computer. Solo gli amministratori e il sistema hanno accesso completo a questa parte del Registro di sistema. Tutti gli altri utenti hanno accesso in sola lettura.
ms.assetid: 8533270d-f1b0-42b9-a50d-b05a0dfeee22
keywords:
- Valore del Registro di sistema EnableDCOM COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a74aea79cf600aad4407b96b5c4a10e8f44633a1c928f8b7e376c192b108cb75
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793600"
---
# <a name="enabledcom"></a>Enabledcom

Controlla i criteri di attivazione e chiamata globali del computer. Solo gli amministratori e il sistema hanno accesso completo a questa parte del Registro di sistema. Tutti gli altri utenti hanno accesso in sola lettura.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   EnableDCOM = value
```

## <a name="remarks"></a>Commenti

Si tratta di **un valore \_ REG SZ.**



| Valore    | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| N (o n) | Nessun client remoto può avviare server o connettersi a oggetti in questo computer. I client locali non possono accedere ai server DCOM remoti. tutto il traffico DCOM è bloccato. L'avvio locale del codice della classe e la connessione agli oggetti sono consentiti per ogni classe in base al valore e alle autorizzazioni di accesso del valore del Registro di sistema [**LaunchPermission**](launchpermission.md) della classe e del valore globale del Registro di sistema [**DefaultLaunchPermission.**](defaultlaunchpermission.md) |
| Y (o y) | L'avvio di server e la connessione agli oggetti da parte di client remoti sono consentiti per ogni classe in base al valore e alle autorizzazioni di accesso del valore del Registro di sistema [**LaunchPermission**](launchpermission.md) della classe e del valore globale del Registro di sistema [**DefaultLaunchPermission.**](defaultlaunchpermission.md)                                                                                                                                                    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**DefaultLaunchPermission**](defaultlaunchpermission.md)
</dt> <dt>

[**LaunchPermission**](launchpermission.md)
</dt> <dt>

[Sicurezza in COM](security-in-com.md)
</dt> </dl>

 

 




