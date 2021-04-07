---
description: La tabella AppId o la tabella del registro di sistema specifica che il programma di installazione configura e registra i server DCOM per eseguire una delle operazioni seguenti durante un'installazione.
ms.assetid: d76ed6df-944b-4996-bf07-e42ceb7a1b69
title: Tabella AppId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07fa202907c094d8c12f73d838f5ad1d6b942125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881134"
---
# <a name="appid-table"></a>Tabella AppId

La tabella AppId o la [tabella del registro di sistema](registry-table.md) specifica che il programma di installazione configura e registra i server DCOM per eseguire una delle operazioni seguenti durante un'installazione.

-   Eseguire il server DCOM con un'identità diversa da quella dell'utente che attiva il server. Ad esempio, per configurare un server DCOM per l'esecuzione sempre come utente interattivo o come utente predefinito.
-   Eseguire il server DCOM come servizio.
-   Configurare l'accesso di sicurezza predefinito per il server DCOM.
-   Registrare il server DCOM in modo che sia attivato in un computer diverso.

Questa tabella viene elaborata in fase di installazione del componente associato al server DCOM nella \_ colonna componente della tabella della [classe](class-table.md). AppId non annunciato.

La tabella AppId contiene le colonne seguenti.



| Colonna               | Tipo                       | Chiave | Nullable |
|----------------------|----------------------------|-----|----------|
| AppId                | [GUID](guid.md)           | S   | N        |
| RemoteServerName     | [Formattato](formatted.md) | N   | S        |
| LocalService         | [Text](text.md)           | N   | S        |
| ServiceParameters    | [Text](text.md)           | N   | S        |
| DllSurrogate         | [Text](text.md)           | N   | S        |
| ActivateAtStorage    | [Integer](integer.md)     | N   | S        |
| RunAsInteractiveUser | [Integer](integer.md)     | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="AppId"></span><span id="appid"></span><span id="APPID"></span>AppId
</dt> <dd>

La colonna AppId della [tabella della classe](class-table.md) è una chiave esterna in questa colonna della tabella AppID. Questa colonna contiene il valore AppId che verrà scritto sotto il CLSID e creerà la chiave del GUID AppId in HKCR \\ AppID.

</dd> <dt>

<span id="RemoteServerName"></span><span id="remoteservername"></span><span id="REMOTESERVERNAME"></span>RemoteServerName
</dt> <dd>

Questa colonna contiene il valore "RemoteServerName" = <xxxx> che verrà scritto in HKCR \\ AppID \\ {AppID} \\ .

</dd> <dt>

<span id="LocalService"></span><span id="localservice"></span><span id="LOCALSERVICE"></span>LocalService
</dt> <dd>

Questa colonna contiene il valore di LocalService che verrà scritto in HKCR \\ AppID \\ { <appid> } "LocalService" = <xxx> .

</dd> <dt>

<span id="ServiceParameters"></span><span id="serviceparameters"></span><span id="SERVICEPARAMETERS"></span>ServiceParameters
</dt> <dd>

Questa colonna contiene il valore di ServiceParameters che verrà scritto in HKCR \\ AppID \\ {AppID>} "ServiceParameters".

</dd> <dt>

<span id="DllSurrogate"></span><span id="dllsurrogate"></span><span id="DLLSURROGATE"></span>DllSurrogate
</dt> <dd>

Questa colonna contiene il valore di DllSurrogate che verrà scritto in HKCR \\ AppID \\ { <appid> } "DllSurrogate" = <xxx> . Se questa colonna è presente, sarà in genere una stringa vuota.

</dd> <dt>

<span id="ActivateAtStorage"></span><span id="activateatstorage"></span><span id="ACTIVATEATSTORAGE"></span>ActivateAtStorage
</dt> <dd>

Un valore integer diverso da zero in questo campo fa in modo che Windows Installer scriva HKCR \\ AppID \\ { <appid> } "ActivateAtStorage" = "Y" nel registro di sistema. Se il campo viene lasciato vuoto o ha un valore pari a zero, non verrà scritto alcun valore.

</dd> <dt>

<span id="RunAsInteractiveUser"></span><span id="runasinteractiveuser"></span><span id="RUNASINTERACTIVEUSER"></span>RunAsInteractiveUser
</dt> <dd>

Un valore integer diverso da zero in questo campo fa in modo che Windows Installer scriva HKCR \\ AppID \\ {AppID>} "RunAs" = "utente interattivo" nel registro di sistema. Se il campo viene lasciato vuoto o ha un valore pari a zero, non verrà scritto alcun valore.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa tabella viene usata dall'azione [registerClassInfo](registerclassinfo-action.md) e dall' [azione UnregisterClassInfo](unregisterclassinfo-action.md).

Si noti che la tabella AppId non contiene una colonna per la registrazione di un nome predefinito. Pertanto, nei casi in cui è necessario scrivere un nome descrittivo per l'utente come valore predefinito, è necessario registrarsi usando la [tabella del registro di sistema](registry-table.md).

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE33](ice33.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
</dl>

 

 



