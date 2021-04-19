---
description: Il \_ metodo get Owner Recupera il proprietario della finestra corrente.
ms.assetid: f0eea5e7-4dfa-4973-ae12-487657e6be80
title: Metodo CBaseControlWindow.get_Owner (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Owner
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c8f8e3d4a331dbc66397a7b0058fcefcede2cdbb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328356"
---
# <a name="cbasecontrolwindowget_owner-method"></a>Metodo CBaseControlWindow. Get \_ Owner

Il `get_Owner` metodo recupera il proprietario della finestra corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Owner(
   OAHWND *Owner
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Proprietario* 
</dt> <dd>

Puntatore al proprietario della finestra.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** .

## <a name="remarks"></a>Commenti

La finestra video può rientrare in un ambiente di documento. A tale scopo, è necessario che la finestra sia costituita da un elemento figlio di un'altra finestra, in modo che venga ritagliata e spostata in modo appropriato. Questa proprietà consente di impostare e recuperare il proprietario della finestra. Quando la finestra è di proprietà di un'altra finestra, viene semplicemente chiamata la funzione **padre** di Microsoft Win32. Un'applicazione che chiama questa funzione modificherà gli stili della finestra in modo da impostare il \_ bit WS figlio su.

Quando la finestra è di proprietà di un'altra finestra, verranno automaticamente trasmessi determinati set di messaggi (in particolare, i messaggi del mouse e della tastiera). Questo consente a un'applicazione di eseguire semplici modifiche e altre interazioni.

Questa funzione membro deve essere chiamata da oggetti esterni tramite l'interfaccia [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) e pertanto blocca la sezione critica per la sincronizzazione con il filtro associato. Chiamare la funzione membro [**CBaseControlWindow:: GetOwnerWindow**](cbasecontrolwindow-getownerwindow.md) per recuperare questa proprietà se non viene chiamata da un oggetto esterno.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




