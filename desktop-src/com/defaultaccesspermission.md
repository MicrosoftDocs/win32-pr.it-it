---
title: DefaultAccessPermission
description: Imposta l'elenco di controllo di accesso (ACL) delle entità che possono accedere alle classi per le quali non è disponibile alcuna impostazione di AccessPermission.
ms.assetid: 02675d0e-a96c-476e-820e-e6ff3c2d1be1
keywords:
- Valore DefaultAccessPermission del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e6c132096807b8c234259071758ebd361421f8f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297748"
---
# <a name="defaultaccesspermission"></a>DefaultAccessPermission

Imposta l'elenco di controllo di accesso (ACL) delle entità che possono accedere alle classi per le quali non è disponibile alcuna impostazione di [**AccessPermission**](accesspermission.md) . Questo ACL viene usato solo da applicazioni che non chiamano [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) e non hanno un valore **AccessPermission** nella chiave [**AppID**](appid-key.md) .

> [!Caution]  
> Non è consigliabile modificare questo valore, perché questo influirà su tutte le applicazioni server COM che non impostano la propria sicurezza a livello di processo e potrebbe impedire il corretto funzionamento. Se si modifica questo valore in modo da influire sulle impostazioni di sicurezza di una particolare applicazione COM, è necessario modificare le impostazioni di sicurezza a livello di processo per quella particolare applicazione COM. Per altre informazioni sull'impostazione della sicurezza a livello di processo, vedere [impostazione della sicurezza a livello di processo](setting-processwide-security.md).

 

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DefaultAccessPermission = ACL
```

## <a name="remarks"></a>Commenti

Si tratta di un valore **\_ binario REG** .

Il runtime COM nel server controlla l'ACL descritto da questo valore durante la rappresentazione del chiamante che sta tentando di connettersi all'oggetto e il suo esito positivo determina se l'accesso è consentito o non consentito. Se la verifica dell'accesso ha esito negativo, la connessione all'oggetto non è consentita. Se questo valore denominato non esiste, solo l'entità server e il sistema locale possono chiamare il server.

Per impostazione predefinita, questo valore non contiene voci. Solo l'entità server e il sistema sono autorizzati a chiamare il server.

Questo valore fornisce un semplice livello di amministrazione centralizzata dell'accesso alla connessione predefinito per l'esecuzione di oggetti in un computer.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**AccessPermission**](accesspermission.md)
</dt> <dt>

[Registrazione di server COM](registering-com-servers.md)
</dt> <dt>

[Impostazione della sicurezza a livello di processo](setting-processwide-security.md)
</dt> </dl>

 

 




