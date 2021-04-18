---
title: DefaultLaunchPermission
description: Definisce l'elenco di controllo di accesso (ACL) delle entità che possono avviare classi che non specificano il proprio ACL tramite il valore del registro di sistema LaunchPermission.
ms.assetid: 23ca87fc-7829-46a9-9fc3-2cd7f677bbff
keywords:
- Valore DefaultLaunchPermission del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 599a0993a4a1238e57e357f428f7046331412cc0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298985"
---
# <a name="defaultlaunchpermission"></a>DefaultLaunchPermission

Definisce l'elenco di controllo di accesso (ACL) delle entità che possono avviare classi che non specificano il proprio ACL tramite il valore del registro di sistema [**LaunchPermission**](launchpermission.md) .

> [!Caution]  
> Non è consigliabile modificare questo valore, perché questo influirà su tutte le applicazioni server COM che non impostano la propria sicurezza a livello di processo e potrebbe impedire il corretto funzionamento. Se si modifica questo valore in modo da influire sulle impostazioni di sicurezza di una particolare applicazione COM, è necessario modificare le impostazioni di sicurezza a livello di processo per quella particolare applicazione COM. Per altre informazioni sull'impostazione della sicurezza a livello di processo, vedere [impostazione della sicurezza a livello di processo](setting-processwide-security.md).

 

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DefaultLaunchPermission = ACL
```

## <a name="remarks"></a>Commenti

Si tratta di un valore **\_ binario REG** .

Di seguito sono riportate le autorizzazioni di accesso predefinite:

-   Amministratori: Consenti avvio
-   SISTEMA: Consenti avvio
-   INTERATTIVO: Consenti avvio

Se il valore [**LaunchPermission**](launchpermission.md) è impostato per un server, avrà la precedenza sul valore di **DefaultLaunchPermission** . Quando riceve una richiesta locale o remota per l'avvio di un server la cui chiave [**AppID**](appid-key.md) non ha un valore **LAUNCHPERMISSION** , l'ACL descritto da questo valore viene verificato durante la rappresentazione del client e il relativo esito positivo consente o impedisce l'avvio del codice della classe.

Questo valore fornisce un semplice livello di amministrazione centralizzata dell'accesso di avvio predefinito a classi altrimenti non amministrate in un computer. Ad esempio, un amministratore può utilizzare lo strumento DCOMCNFG per configurare il sistema in modo da consentire l'accesso in sola lettura per gli utenti esperti. OLE limita quindi le richieste di avvio del codice della classe ai membri del gruppo Power Users. Un amministratore potrebbe successivamente configurare le autorizzazioni di avvio per le singole classi per concedere la possibilità di avviare il codice della classe ad altri gruppi o singoli utenti in base alle esigenze.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**LaunchPermission**](launchpermission.md)
</dt> <dt>

[Registrazione di server COM](registering-com-servers.md)
</dt> <dt>

[Impostazione della sicurezza a livello di processo](setting-processwide-security.md)
</dt> </dl>

 

 




