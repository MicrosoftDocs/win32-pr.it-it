---
description: La tabella AppId o la tabella Registry specifica che il programma di installazione configura e registra i server DCOM per eseguire una delle operazioni seguenti durante un'installazione.
ms.assetid: d76ed6df-944b-4996-bf07-e42ceb7a1b69
title: Tabella AppId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e8452635cd7c167d6a8618629eaec2f6f6c1aa2e72e0b3628a7d4542a9e7160
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066271"
---
# <a name="appid-table"></a>Tabella AppId

La tabella AppId o la [tabella Registry](registry-table.md) specifica che il programma di installazione configura e registra i server DCOM per eseguire una delle operazioni seguenti durante un'installazione.

-   Eseguire il server DCOM con un'identità diversa rispetto all'utente che attiva il server. Ad esempio, per configurare un server DCOM in modo che sia sempre eseguito come utente interattivo o come utente predefinito.
-   Eseguire il server DCOM come servizio.
-   Configurare l'accesso di sicurezza predefinito per il server DCOM.
-   Registrare il server DCOM in modo che sia attivato in un computer diverso.

Questa tabella viene elaborata durante l'installazione del componente associato al server DCOM nella \_ colonna Componente della tabella [Class](class-table.md). Un AppId non è annunciato.

La tabella AppId contiene le colonne seguenti.



| Colonna               | Tipo                       | Chiave | Nullable |
|----------------------|----------------------------|-----|----------|
| AppId                | [GUID](guid.md)           | S   | N        |
| RemoteServerName     | [Formattato](formatted.md) | N   | S        |
| LocalService         | [Text](text.md)           | N   | S        |
| Parametri del servizio    | [Text](text.md)           | N   | S        |
| DllSurrogate         | [Text](text.md)           | N   | S        |
| ActivateAtStorage    | [Integer](integer.md)     | N   | S        |
| RunAsInteractiveUser | [Integer](integer.md)     | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="AppId"></span><span id="appid"></span><span id="APPID"></span>Appid
</dt> <dd>

La colonna AppId della [tabella Class è](class-table.md) una chiave esterna in questa colonna della tabella AppId. Questa colonna contiene il valore AppId che verrà scritto sotto il CLSID e crea la chiave GUID AppId in HKCR \\ AppId.

</dd> <dt>

<span id="RemoteServerName"></span><span id="remoteservername"></span><span id="REMOTESERVERNAME"></span>RemoteServerName
</dt> <dd>

Questa colonna contiene il valore di "RemoteServerName"= che verrà <xxxx> scritto in HKCR \\ AppID \\ {AppID} \\ .

</dd> <dt>

<span id="LocalService"></span><span id="localservice"></span><span id="LOCALSERVICE"></span>Localservice
</dt> <dd>

Questa colonna contiene il valore di LocalService che verrà scritto in HKCR \\ AppID \\ { } <appid> "LocalService"= <xxx> .

</dd> <dt>

<span id="ServiceParameters"></span><span id="serviceparameters"></span><span id="SERVICEPARAMETERS"></span>Parametri del servizio
</dt> <dd>

Questa colonna contiene il valore di ServiceParameters che verrà scritto in HKCR \\ AppID \\ {appid>} "ServiceParameters".

</dd> <dt>

<span id="DllSurrogate"></span><span id="dllsurrogate"></span><span id="DLLSURROGATE"></span>DllSurrogate
</dt> <dd>

Questa colonna contiene il valore di DllSurrogate che verrà scritto in HKCR \\ AppId \\ { } <appid> "DllSurrogate"= <xxx> . Se questa colonna è presente, sarà in genere una stringa vuota.

</dd> <dt>

<span id="ActivateAtStorage"></span><span id="activateatstorage"></span><span id="ACTIVATEATSTORAGE"></span>ActivateAtStorage
</dt> <dd>

Un valore intero diverso da zero in questo campo fa sì che Windows Installer scrivo HKCR \\ AppID \\ { } <appid> "ActivateAtStorage"="Y" nel Registro di sistema. Se il campo viene lasciato vuoto o ha un valore pari a zero, non verrà scritto alcun valore.

</dd> <dt>

<span id="RunAsInteractiveUser"></span><span id="runasinteractiveuser"></span><span id="RUNASINTERACTIVEUSER"></span>RunAsInteractiveUser
</dt> <dd>

Un valore intero diverso da zero in questo campo fa in modo che Windows Installer scrivo HKCR \\ AppID \\ {appid>} "RunAs"="Interactive User" nel Registro di sistema. Se il campo viene lasciato vuoto o ha un valore pari a zero, non verrà scritto alcun valore.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa tabella viene usata [dall'azione RegisterClassInfo e](registerclassinfo-action.md) [dall'azione UnregisterClassInfo](unregisterclassinfo-action.md).

Si noti che la tabella AppId non include una colonna per la registrazione di un nome predefinito. Pertanto, nei casi in cui è necessario scrivere un nome descrittivo come valore nome predefinito, è necessario eseguire la registrazione usando la [tabella Registry](registry-table.md).

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE33](ice33.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
</dl>

 

 



