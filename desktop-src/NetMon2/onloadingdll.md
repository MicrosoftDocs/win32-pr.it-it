---
description: Carica la DLL del monitoraggio.
ms.assetid: 6de2750f-3f12-4c0a-af8d-3ebd227fa123
title: Funzione OnLoadingDLL (Netmon.h)
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
ms.openlocfilehash: 6049684798d6dda9030abd667c28a62f4b19f9b4e66a831ef4c1d2caa880fb1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676871"
---
# <a name="onloadingdll-function"></a>Funzione OnLoadingDLL

La **funzione OnLoadingDLL** carica la DLL di monitoraggio.

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

*hFilterBlob* \[ in, out\]
</dt> <dd>

BLOB utilizzato da MCSVC per associare un monitoraggio a schede di interfaccia di rete disponibili. Questo parametro contiene sempre una richiesta per [un'interfaccia IRTC,](irtc.md) quindi la maggior parte dei monitoraggi non deve aggiungere voci al BLOB. Tuttavia, un monitoraggio personalizzato può aggiungere altri criteri di filtro,ad esempio che il tipo MAC deve essere Ethernet.

</dd> <dt>

*pCreateFlags* \[ Pollici\]
</dt> <dd>

Flag che indicano il modo in cui MCSVC controlla la creazione di un monitoraggio. Questo parametro deve essere uno dei valori seguenti:



| Valore                                                                                                                                                                                                            | Significato                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCS_CREATE_ONE_PER_NETCARD"></span><span id="mcs_create_one_per_netcard"></span><dl> <dt>**MCS \_ \_ CREARNE UNO \_ PER \_ NETCARD**</dt> </dl>          | MCSVC garantisce l'esistenza di una sola istanza di questo monitoraggio per ogni scheda di interfaccia di rete. È possibile creare una seconda istanza solo se la prima viene distrutta.<br/> |
| <span id="MCS_CREATE_CONFIGS_BY_DEFAULT"></span><span id="mcs_create_configs_by_default"></span><dl> <dt>**MCS \_ CREATE \_ CONFIGS PER IMPOSTAZIONE \_ \_ PREDEFINITA**</dt> </dl> | Se il monitoraggio ha una configurazione interna predefinita, MCSVC non richiede all'utente di configurare il monitoraggio prima della creazione dell'istanza.<br/>  |



 

</dd> <dt>

*ppDefaultName* \[ Cambio\]
</dt> <dd>

Puntatore a un puntatore all'indirizzo del nome predefinito del monitoraggio. MCSVC usa il nome predefinito durante la creazione di istanze del monitoraggio.

Ad esempio, se il nome predefinito restituito è "Monitoraggio router", la prima istanza di monitoraggio sarà "Monitoraggio router 1", la seconda sarà "RouterMonitor2 e così via. Se **viene restituito** NULL, MCSVC usa il nome della DLL.

</dd> <dt>

*ppDescription* \[ Cambio\]
</dt> <dd>

Puntatore a un puntatore all'indirizzo della descrizione del monitoraggio. La descrizione viene passata a Monitor Control Tool, che usa la descrizione per indicare all'utente che il monitoraggio esiste. Questo parametro può restituire **NULL.**

</dd> <dt>

*ppDefaultScript* \[ Cambio\]
</dt> <dd>

Puntatore a un puntatore all'indirizzo dello script form HTML predefinito usato per configurare il monitoraggio. Anche se le istanze del monitoraggio possono modificare il proprio script, la maggior parte dei monitoraggi carica semplicemente lo script una sola volta, da un file. Il valore di *ppDefaultScript* può essere **NULL.** Tuttavia, il monitoraggio non può essere configurato esternamente o deve fornire uno script in un secondo momento. È più efficiente fornire uno script predefinito qui.

</dd> <dt>

*ppDefaultConfig* \[ Cambio\]
</dt> <dd>

Indirizzo della stringa predefinita utilizzata per configurare il monitoraggio al momento della creazione. Questo parametro può essere impostato su **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è S OK, che \_ corrisponde a NOERROR.

Se la funzione ha esito negativo, MCSVC omette il monitoraggio specificato da tutti i relativi elenchi. dopo, non è possibile creare alcun monitoraggio di questo tipo.

## <a name="remarks"></a>Commenti

La **funzione OnLoadingDLL** viene chiamata una volta da MCSVC, quando carica per la prima volta la DLL. La DLL fornisce quindi i valori predefiniti che verranno usati da MCSVC durante la creazione di un'istanza di un monitoraggio.

Il monitoraggio deve allocare tutta la memoria necessaria per le stringhe restituite a MCSVC. In caso di restituzione, MCSVC esegue copie di tutte le stringhe e non tenterà di liberare le stringhe restituite.

Il monitoraggio deve usare le funzioni helper BLOB per modificare il BLOB del filtro.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




