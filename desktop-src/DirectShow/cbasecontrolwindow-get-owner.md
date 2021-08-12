---
description: Il metodo get \_ Owner recupera il proprietario della finestra corrente.
ms.assetid: f0eea5e7-4dfa-4973-ae12-487657e6be80
title: CBaseControlWindow.get_Owner metodo (Ctlutil.h)
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
ms.openlocfilehash: 3a64325fddebc410c5a75a5c2fb8811241012feb6a046b9059897f9b13e0206f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660514"
---
# <a name="cbasecontrolwindowget_owner-method"></a>Metodo CBaseControlWindow.get \_ Owner

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

Restituisce un **valore HRESULT.**

## <a name="remarks"></a>Commenti

La finestra video può essere riprodotta all'interno di un ambiente di documento. A tale scopo, la finestra deve essere resa figlio di un'altra finestra (in modo che sia ritagliata e spostata in modo appropriato). Questa proprietà consente di impostare e recuperare il proprietario della finestra. Quando la finestra è di proprietà di un'altra finestra, chiama semplicemente la funzione **SetParent** di Microsoft Win32. Un'applicazione che chiama questa funzione modificherà gli stili della finestra per impostare il \_ bit WS CHILD.

Quando la finestra è di proprietà di un'altra finestra, inoltra automaticamente determinati set di messaggi ,in particolare i messaggi del mouse e della tastiera. In questo modo un'applicazione può eseguire semplici operazioni di modifica dell'area sensibile e altre interazioni.

Questa funzione membro deve essere chiamata da oggetti esterni tramite [**l'interfaccia IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) e pertanto blocca la sezione critica per la sincronizzazione con il filtro associato. Chiamare la [**funzione membro CBaseControlWindow::GetOwnerWindow**](cbasecontrolwindow-getownerwindow.md) per recuperare questa proprietà se non viene chiamata da un oggetto esterno.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




