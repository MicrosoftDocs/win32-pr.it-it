---
description: Carica la DLL di monitoraggio.
ms.assetid: 6de2750f-3f12-4c0a-af8d-3ebd227fa123
title: Funzione OnLoadingDLL (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OnLoadingDLL
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: b2d9d728065818b1e94fa436f4d1e9b62dbeb5cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308159"
---
# <a name="onloadingdll-function"></a>OnLoadingDLL (funzione)

La funzione **OnLoadingDLL** carica la dll di monitoraggio.

## <a name="syntax"></a>Sintassi


```C++
HRESULT OnLoadingDLL(
  _Inout_ HBLOB hFilterBlob,
  _In_    DWORD *pCreateFlags,
  _Out_   char  **ppDefaultName,
  _Out_   char  **ppDescription,
  _Out_   char  **ppDefaultScript,
  _Out_   char  **ppDefaultConfig
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hFilterBlob* \[ in uscita\]
</dt> <dd>

Un BLOB utilizzato dal MCSVC per trovare la corrispondenza con un monitoraggio con NIC disponibili. Questo parametro contiene sempre una richiesta per un'interfaccia [IRTC](irtc.md) , quindi la maggior parte dei monitoraggi non è necessario aggiungere alcuna voce al BLOB. Un monitoraggio personalizzato, tuttavia, può aggiungere altri criteri di filtro, ad esempio il tipo MAC deve essere Ethernet.

</dd> <dt>

*pCreateFlags* \[ in\]
</dt> <dd>

Flag che indicano il modo in cui MCSVC controlla la creazione di un monitoraggio. Questo parametro deve essere uno dei valori seguenti:



| Valore                                                                                                                                                                                                            | Significato                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCS_CREATE_ONE_PER_NETCARD"></span><span id="mcs_create_one_per_netcard"></span><dl> <dt>**MCS \_ crearne \_ uno \_ per ogni \_ scheda**</dt> </dl>          | MCSVC garantisce che esista una sola istanza di questo monitoraggio per ogni scheda di interfaccia di rete. Una seconda istanza può essere creata solo se la prima viene distrutta.<br/> |
| <span id="MCS_CREATE_CONFIGS_BY_DEFAULT"></span><span id="mcs_create_configs_by_default"></span><dl> <dt>**\_ \_ \_ per \_ impostazione predefinita, MCS crea le configurazioni**</dt> </dl> | Se il monitoraggio ha una configurazione interna predefinita, MCSVC non richiede all'utente di configurare il monitoraggio prima della creazione dell'istanza.<br/>  |



 

</dd> <dt>

*ppDefaultName* \[ out\]
</dt> <dd>

Puntatore a un puntatore all'indirizzo del nome predefinito del monitoraggio. MCSVC utilizza il nome predefinito durante la creazione di istanze del monitoraggio.

Se, ad esempio, il nome predefinito restituito è "Monitoraggio router", la prima istanza di monitoraggio sarà "router monitor 1", il secondo sarà "RouterMonitor2 e così via. Se viene restituito **null** , MCSVC usa il nome della dll.

</dd> <dt>

*ppDescription* \[ out\]
</dt> <dd>

Puntatore a un puntatore all'indirizzo della descrizione del monitoraggio. La descrizione viene passata allo strumento di controllo del monitoraggio, che utilizza la descrizione per indicare all'utente che il monitoraggio esiste. Questo parametro può restituire **null**.

</dd> <dt>

*ppDefaultScript* \[ out\]
</dt> <dd>

Puntatore a un puntatore all'indirizzo dello script del modulo HTML predefinito utilizzato per configurare il monitoraggio. Sebbene le istanze del monitoraggio possano modificare il proprio script, la maggior parte dei monitoraggi caricano semplicemente lo script una sola volta, da un file. Il valore di *ppDefaultScript* può essere **null**. Tuttavia, il monitoraggio non può essere configurato esternamente o deve fornire uno script in un secondo momento. È più efficiente fornire uno script predefinito.

</dd> <dt>

*ppDefaultConfig* \[ out\]
</dt> <dd>

Indirizzo della stringa predefinita utilizzata per configurare il monitoraggio quando viene creato. Questo parametro può essere impostato su **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è S \_ OK, che corrisponde a NOERROR.

Se la funzione ha esito negativo, MCSVC omette il monitor specificato da tutti i relativi elenchi; in seguito, non è possibile creare alcun monitoraggio di questo tipo.

## <a name="remarks"></a>Commenti

La funzione **OnLoadingDLL** viene chiamata una volta da MCSVC, quando carica la dll per la prima volta. La DLL fornisce quindi i valori predefiniti che verranno usati da MCSVC durante la creazione di un'istanza di un monitoraggio.

Il monitoraggio deve allocare tutta la memoria necessaria per le stringhe restituite a MCSVC. Quando viene restituito, MCSVC crea copie di tutte le stringhe e non tenta di liberare le stringhe restituite.

Il monitoraggio deve usare funzioni helper BLOB per modificare il BLOB del filtro.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




