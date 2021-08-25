---
description: Il messaggio TAPI LINE APPNEWCALL viene inviato per informare un'applicazione quando un nuovo handle di chiamata è stato creato in modo \_ spontaneo per conto di .
ms.assetid: 0c263025-e719-453e-91c4-a9f2d9321db3
title: LINE_APPNEWCALL messaggio (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22efd93febad5e0199f2ff8897841fe57e8e637acfb8f9cd316386ed913876c1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867131"
---
# <a name="line_appnewcall-message"></a>LINE \_ APPNEWCALL message

Il messaggio TAPI **LINE \_ APPNEWCALL** viene inviato per informare un'applicazione quando un nuovo handle di chiamata è stato creato in modo spontaneo per suo conto (diverso da una chiamata API dall'applicazione, nel qual caso l'handle sarebbe stato restituito tramite un parametro puntatore passato alla funzione).


```C++
        
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDevice* 
</dt> <dd>

Handle dell'applicazione per il dispositivo linea in cui è stata creata la chiamata.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Istanza di callback fornita all'apertura della riga della chiamata.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Identificatore dell'indirizzo nella riga in cui viene visualizzata la chiamata. Un identificatore di indirizzo è associato in modo permanente a un indirizzo. l'identificatore rimane costante tra gli aggiornamenti del sistema operativo.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Handle dell'applicazione per la nuova chiamata.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Privilegio delle applicazioni per la nuova chiamata (LINECALLPRIVILEGE \_ OWNER o LINECALLPRIVILEGE \_ MONITOR).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Alle applicazioni che supportano TAPI versione 2.0 o successiva viene inviato un messaggio **LINE \_ APPNEWCALL** ogni volta che all'applicazione viene assegnato un handle a una nuova chiamata. Poiché il messaggio include i *parametri hLine* e *dwAddressID* in cui è presente la chiamata, l'applicazione può creare facilmente un nuovo oggetto chiamata nel contesto corretto. Il **messaggio LINE \_ APPNEWCALL** è sempre seguito da un messaggio [**LINE \_ CALLSTATE**](line-callstate.md) che indica lo stato iniziale della chiamata.

Alle applicazioni precedenti (che hanno negoziato una versione dell'API precedente alla 2.0) viene inviato solo un messaggio [**LINE \_ CALLSTATE,**](line-callstate.md) come documentato nelle versioni precedenti dell'API. Tali applicazioni creano un nuovo oggetto chiamata alla ricezione di un messaggio [**LINE \_ CALLSTATE**](line-callstate.md) con *dwParam3* impostato su un valore diverso da zero e contenente un handle di chiamata non attualmente noto dall'applicazione. Gli svantaggi sono che (a) l'applicazione deve chiamare [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) per determinare i parametri *hLine* e *dwAddressID* associati alla chiamata; (b) l'applicazione deve analizzare tutti gli handle di chiamata noti per determinare che la chiamata è una nuova chiamata; e (c) è possibile, in determinate condizioni, che l'applicazione pensi di ricevere un nuovo handle di chiamata quando in realtà ha appena deallocato l'handle alla chiamata (ad esempio, l'applicazione ha appena deallocato un handle di chiamata, ma un messaggio [**LINE \_ CALLSTATE**](line-callstate.md) che indica la proprietà della chiamata da parte dell'applicazione a causa di [**un lineHandoff**](/windows/desktop/api/Tapi/nf-tapi-linehandoff) da un'altra applicazione era già presente nella coda di messaggi TAPI dell'applicazione).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LINE \_ CALLSTATE**](line-callstate.md)
</dt> <dt>

[**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo)
</dt> <dt>

[**lineHandoff**](/windows/desktop/api/Tapi/nf-tapi-linehandoff)
</dt> </dl>

 

 




