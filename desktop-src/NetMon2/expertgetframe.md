---
description: Restituisce il frame richiesto da un'acquisizione caricata.
ms.assetid: efd1cff5-a3a1-4910-b003-25b6e10dad6e
title: Funzione ExpertGetFrame (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertGetFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2bd02bde8caf157b6df6b1dd772a8f7574df0e57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878665"
---
# <a name="expertgetframe-function"></a>ExpertGetFrame (funzione)

La funzione **ExpertGetFrame** restituisce il frame richiesto da un'acquisizione caricata.

## <a name="syntax"></a>Sintassi


```C++
DWORD WINAPI ExpertGetFrame(
  _In_  HEXPERTKEY              hExpertKey,
  _In_  DWORD                   Direction,
  _In_  DWORD                   RequestFlags,
  _In_  DWORD                   RequestedFrameNumber,
  _In_  HFILTER                 hFilter,
  _Out_ LPEXPERTFRAMEDESCRIPTOR pEFrameDescriptor
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hExpertKey* \[ in\]
</dt> <dd>

Identificatore univoco di un esperto. Network Monitor passa l'identificatore *hExpertKey* all'esperto quando chiama la funzione [**Run**](run.md) .

</dd> <dt>

*Direzione* \[ in\]
</dt> <dd>

Valore che identifica il modo in cui Network Monitor cerca il frame.



| Valore                                                                                                                                                                                         | Significato                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="GET_SPECIFIED_FRAME"></span><span id="get_specified_frame"></span><dl> <dt>**OTTENERE \_ il \_ frame specificato**</dt> </dl>              | Restituisce il frame richiesto.<br/> |
| <span id="GET_FRAME_NEXT_FORWARD"></span><span id="get_frame_next_forward"></span><dl> <dt>**OTTENERE il \_ frame \_ successivo \_**</dt> </dl>    | Restituisce il frame successivo.<br/>      |
| <span id="GET_FRAME_NEXT_BACKWARD"></span><span id="get_frame_next_backward"></span><dl> <dt>**OTTENERE il \_ frame \_ successivo all' \_ indietro**</dt> </dl> | Restituisce il frame precedente.<br/>  |



 

</dd> <dt>

*RequestFlags* \[ in\]
</dt> <dd>

Flag che specificano il modo in cui Network Monitor deve gestire la richiesta. Specificare uno o più dei flag seguenti.



| Valore                                                                                                                                                                                             | Significato                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FLAGS_DEFER_TO_UI_FILTER"></span><span id="flags_defer_to_ui_filter"></span><dl> <dt>**FLAG \_ rinviato \_ al \_ filtro dell'interfaccia utente \_**</dt> </dl> | Prima di applicare il parametro del filtro di visualizzazione dell'esperto specificato in *hFilter*, applicare il filtro di visualizzazione che Network Monitor sta utilizzando all'avvio dell'esperto.<br/>                                                                                                                              |
| <span id="FLAGS_ATTACH_PROPERTIES"></span><span id="flags_attach_properties"></span><dl> <dt>**FLAGs \_ Connetti \_ Proprietà**</dt> </dl>      | Le proprietà individuate da tutti i parser di protocollo con le sezioni richieste di questo frame sono collegate al frame. Se il flag non è impostato, il campo **lpPropertyTable** della struttura [**EXPERTFRAMEDESCRIPTOR**](expertframedescriptor.md) (restituito da **PEFrameDescriptor**) verrà impostato su **null**.<br/> |



 

</dd> <dt>

*RequestedFrameNumber* \[ in\]
</dt> <dd>

Numero del frame richiesto.

</dd> <dt>

*hFilter* \[ in\]
</dt> <dd>

Handle per il filtro di visualizzazione esperto. Se l'esperto non dispone di un filtro di visualizzazione, impostare il parametro su **null**.

</dd> <dt>

*pEFrameDescriptor* \[ out\]
</dt> <dd>

Struttura [**EXPERTFRAMEDESCRIPTOR**](expertframedescriptor.md) che, al ritorno, descrive il frame. L'esperto deve allocare e liberare la memoria utilizzata da questa struttura.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.

Se la funzione ha esito negativo, il valore restituito indica il motivo dell'errore. Se il valore restituito è NMERR \_ Expert \_ Terminate, l'esperto deve eseguire immediatamente la pulizia e la restituzione; l'utente ha interrotto l'esecuzione dell'esperto.

## <a name="remarks"></a>Commenti

Se si impostano le \_ proprietà di associazione dei flag \_ , la chiamata richiede più risorse rispetto a quando non si imposta il flag. Se il flag non è impostato, un puntatore punta al frame non elaborato e ai dati relativi al frame. Se questo flag è impostato, Network Monitor connette tutte le proprietà al frame chiamando ogni parser che attesta una parte del frame. Questo può essere un processo lento.

Gli esperti non devono impostare il \_ flag delle proprietà di associazione dei flag \_ a meno che gli esperti non richiedano le proprietà che i parser alleghino al frame. Se possibile, gli esperti devono chiamare la funzione **ExpertGetFrame** senza il flag, quindi estrarre i dati richiesti direttamente dal frame.

Se l'esperto chiama **ExpertGetFrame** senza il flag delle proprietà di associazione dei flag \_ \_ e richiede le proprietà associate a tale frame (ad esempio, un evento), l'esperto chiama **ExpertGetFrame** con gli stessi parametri tranne i seguenti:

``` syntax
Direction = EXPERT_GET_SPECIFIED_FRAME;
RequestFlags &= (~EXPERT_DEFER_TO_UI_FILTER) | EXPERT_ATTACH_PROPERTIES;
RequestedFrameNumber= (The actual frame number you want);
hFilter = NULL;
pEFrameDescriptor = (The same one as last time);
```

L'uso del codice precedente garantisce che l'esperto ottenga il frame necessario senza dover chiamare di nuovo il codice di filtro.

È possibile impostare il parametro *hFilter* come **LPVOID**. Se esiste, il frame restituito passa il filtro. Se l'esperto non dispone di un filtro di visualizzazione da passare alla funzione (se *hFilter* è **null** ), il frame restituito non viene filtrato.

La funzione **ExpertGetFrame** può essere chiamata solo da esperti che implementano la funzione di esportazione [**Run**](run.md) o [**Configure**](configure.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmap. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




