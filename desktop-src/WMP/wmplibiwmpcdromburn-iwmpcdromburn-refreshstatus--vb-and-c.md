---
title: Metodo IWMPCdromBurn refreshStatus
description: Il metodo refreshStatus aggiorna le informazioni sullo stato per la playlist Burn corrente.
ms.assetid: 4dd90e76-92b5-4a00-b027-b54502e56804
keywords:
- Metodo refreshStatus Windows Media Player
- Metodo refreshStatus Windows Media Player, interfaccia IWMPCdromBurn
- Interfaccia IWMPCdromBurn Windows Media Player, metodo refreshStatus
topic_type:
- apiref
api_name:
- IWMPCdromBurn.refreshStatus
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55205e684d055d20c8e8f218ba58716de8472916
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329655"
---
# <a name="iwmpcdromburnrefreshstatus-method"></a>Metodo IWMPCdromBurn:: refreshStatus

Il metodo **refreshStatus** aggiorna le informazioni sullo stato per la playlist Burn corrente.

## <a name="syntax"></a>Sintassi


```CSharp
public void refreshStatus();
```


```VB

Public Sub refreshStatus()
Implements IWMPCdromBurn.refreshStatus
```





## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

È consigliabile chiamare questo metodo dopo avere creato o modificato una playlist di masterizzazione prima di leggere le informazioni sullo stato o di masterizzare il CD. È possibile verificare se è necessario un aggiornamento ottenendo il valore di **burnState** e verificando la presenza di wmpbsRefreshStatusPending.

L'aggiornamento dello stato è un'operazione sincrona. Ciò significa che un periodo di tempo prolungato può trascorrere prima che questo metodo restituisca se la playlist Burn corrente è di grandi dimensioni e contiene numerose modifiche.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPCdromBurn (VB e C#)**](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[**IWMPCdromBurn. burnState (VB e C#)**](wmplibiwmpcdromburn-iwmpcdromburn-burnstate--vb-and-c.md)
</dt> <dt>

[**WMPBurnState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate)
</dt> </dl>

 

 





