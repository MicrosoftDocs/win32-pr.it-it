---
title: EnableDCOM
description: Controlla i criteri di attivazione e chiamata globali del computer. Solo gli amministratori e il sistema hanno accesso completo a questa parte del registro di sistema. Tutti gli altri utenti hanno accesso in sola lettura.
ms.assetid: 8533270d-f1b0-42b9-a50d-b05a0dfeee22
keywords:
- Valore EnableDCOM del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b42cc95b24522e87e4b64f6feefc5c6c56ad5341
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395671"
---
# <a name="enabledcom"></a>EnableDCOM

Controlla i criteri di attivazione e chiamata globali del computer. Solo gli amministratori e il sistema hanno accesso completo a questa parte del registro di sistema. Tutti gli altri utenti hanno accesso in sola lettura.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   EnableDCOM = value
```

## <a name="remarks"></a>Commenti

Si tratta di un valore **reg \_ SZ** .



| Valore    | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| N (o n) | Nessun client remoto può avviare Server o connettersi a oggetti nel computer. I client locali non possono accedere ai server DCOM remoti; tutto il traffico DCOM è bloccato. L'avvio locale del codice della classe e la connessione a oggetti sono consentiti per ogni classe in base al valore e alle autorizzazioni di accesso del valore del registro di sistema [**LaunchPermission**](launchpermission.md) della classe e al valore del registro di sistema [**DefaultLaunchPermission**](defaultlaunchpermission.md) globale. |
| Y (o y) | L'avvio di server e la connessione a oggetti da parte di client remoti sono consentiti in base alle singole classi in base al valore e alle autorizzazioni di accesso del valore del registro di sistema [**LaunchPermission**](launchpermission.md) della classe e al valore del registro di sistema [**DefaultLaunchPermission**](defaultlaunchpermission.md) globale.                                                                                                                                                    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**DefaultLaunchPermission**](defaultlaunchpermission.md)
</dt> <dt>

[**LaunchPermission**](launchpermission.md)
</dt> <dt>

[Sicurezza in COM](security-in-com.md)
</dt> </dl>

 

 




