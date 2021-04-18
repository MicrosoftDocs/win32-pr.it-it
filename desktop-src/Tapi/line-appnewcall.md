---
description: Il messaggio della linea TAPI \_ APPNEWCALL viene inviato per informare un'applicazione quando un nuovo handle di chiamata è stato creato spontaneamente per suo conto.
ms.assetid: 0c263025-e719-453e-91c4-a9f2d9321db3
title: Messaggio di LINE_APPNEWCALL (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33d24ca816fb69384e90e4215edbc90b9410b887
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331035"
---
# <a name="line_appnewcall-message"></a>\_Messaggio linea APPNEWCALL

Il messaggio della **linea TAPI \_ APPNEWCALL** viene inviato per informare un'applicazione quando un nuovo handle di chiamata è stato creato spontaneamente per suo conto (ad eccezione di una chiamata API dall'applicazione, nel qual caso l'handle verrebbe restituito tramite un parametro puntatore passato nella funzione).


```C++
        
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDevice* 
</dt> <dd>

Handle dell'applicazione per il dispositivo della linea in cui è stata creata la chiamata.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Istanza di callback fornita all'apertura della riga della chiamata.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Identificatore dell'indirizzo sulla riga in cui viene visualizzata la chiamata. Un identificatore di indirizzo è associato in modo permanente a un indirizzo. l'identificatore rimane costante tra gli aggiornamenti del sistema operativo.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Handle dell'applicazione per la nuova chiamata.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Il privilegio delle applicazioni per la nuova chiamata (LINECALLPRIVILEGE \_ owner o LINECALLPRIVILEGE \_ monitor).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Le applicazioni che supportano la versione 2,0 o successive di TAPI ricevono un messaggio di **riga \_ APPNEWCALL** ogni volta che all'applicazione viene assegnato un handle per una nuova chiamata in modo spontaneo. Poiché il messaggio include i parametri *hLine* e *dwAddressID* in cui è presente la chiamata, l'applicazione può creare rapidamente un nuovo oggetto chiamata nel contesto corretto. Il messaggio di **riga \_ APPNEWCALL** è sempre seguito immediatamente da un messaggio di [**riga \_ CALLSTATE**](line-callstate.md) che indica lo stato iniziale della chiamata.

Le applicazioni meno recenti (che hanno negoziato una versione API precedente alla 2,0) vengono inviate solo un messaggio di [**riga \_ CALLSTATE**](line-callstate.md) , come documentato nelle versioni precedenti dell'API. Tali applicazioni creeranno un nuovo oggetto chiamata al momento della ricezione di un messaggio di [**riga \_ CALLSTATE**](line-callstate.md) con *dwParam3* impostato su un valore diverso da zero e contenente un handle di chiamata attualmente non noto dall'applicazione. Gli svantaggi sono che (a) l'applicazione deve chiamare [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) per determinare i parametri *hLine* e *dwAddressID* associati alla chiamata; (b) l'applicazione deve analizzare tutti gli handle di chiamata noti per determinare che la chiamata è una nuova chiamata; e (c) è possibile, in determinate condizioni, affinché l'applicazione ritenga che riceva un nuovo handle di chiamata quando in realtà ha appena deallocato l'handle alla chiamata (ad esempio, l'applicazione ha appena deallocato un handle di chiamata, ma un messaggio di [**riga \_ CALLSTATE**](line-callstate.md) che fornisce la proprietà dell'applicazione della chiamata a causa di un [**lineHandoff**](/windows/desktop/api/Tapi/nf-tapi-linehandoff) da un'altra applicazione è già presente nella coda di messaggi TAPI dell'applicazione).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LINEA \_ CALLSTATE**](line-callstate.md)
</dt> <dt>

[**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo)
</dt> <dt>

[**lineHandoff**](/windows/desktop/api/Tapi/nf-tapi-linehandoff)
</dt> </dl>

 

 




