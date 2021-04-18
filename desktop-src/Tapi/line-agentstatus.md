---
description: Il messaggio della linea TAPI \_ AGENTSTATUS viene inviato quando lo stato di un agente ACD viene modificato su una linea attualmente aperta dall'applicazione. L'applicazione può richiamare lineGetAgentStatus per determinare lo stato corrente dell'agente.
ms.assetid: 48f5d9bc-f20d-4364-8ec1-0b4bdc9cfcb4
title: Messaggio di LINE_AGENTSTATUS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b98242745e2f025f95cfe06fbe22c8956a02b0e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331038"
---
# <a name="line_agentstatus-message"></a>\_Messaggio linea AGENTSTATUS

Il messaggio della **linea TAPI \_ AGENTSTATUS** viene inviato quando lo stato di un agente ACD viene modificato su una linea attualmente aperta dall'applicazione. L'applicazione può richiamare [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa) per determinare lo stato corrente dell'agente.


```C++
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDevice* 
</dt> <dd>

Handle dell'applicazione per il dispositivo della linea in cui è stato modificato lo stato dell'agente.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Istanza di callback fornita all'apertura della riga della chiamata.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Identificatore dell'indirizzo sulla riga in cui è stato modificato lo stato dell'agente. Un identificatore di indirizzo è associato in modo permanente a un indirizzo. l'identificatore rimane costante tra gli aggiornamenti del sistema operativo.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Specifica lo stato dell'agente che è stato modificato. può essere una combinazione di [**\_ costanti LINEAGENTSTATUS**](lineagentstatus--constants.md).

</dd> <dt>

*dwParam3* 
</dt> <dd>

Se *dwParam2* include il \_ bit di stato LINEAGENTSTATUS, *dwParam3* indica il nuovo valore del membro **dwState** in [**LINEAGENTSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus). In caso contrario, questo parametro è impostato su zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Il messaggio di **riga \_ AGENTSTATUS** non viene inviato ad applicazioni che supportano le versioni precedenti di TAPI.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LINEAGENTSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus)
</dt> <dt>

[**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa)
</dt> </dl>

 

 




