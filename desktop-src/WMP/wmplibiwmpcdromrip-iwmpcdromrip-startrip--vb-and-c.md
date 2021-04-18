---
title: Metodo IWMPCdromRip startRip
description: Il metodo startRip strappa il CD.
ms.assetid: 3569e29c-e593-4bdd-8afb-74e39721cf80
keywords:
- Metodo startRip Windows Media Player
- Metodo startRip Windows Media Player, interfaccia IWMPCdromRip
- Interfaccia IWMPCdromRip Windows Media Player, metodo startRip
topic_type:
- apiref
api_name:
- IWMPCdromRip.startRip
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 327ac9009cf1b8fb9ccfbcc460cde78ef40b3802
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329286"
---
# <a name="iwmpcdromripstartrip-method"></a>Metodo IWMPCdromRip:: startRip

Il metodo **startRip** strappa il CD.

## <a name="syntax"></a>Sintassi


```CSharp
public void startRip();
```


```VB

Public Sub startRip()
Implements IWMPCdromRip.startRip
```





## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

La copia di un CD usando l'interfaccia **IWMPCdromRip** ha lo stesso effetto del ritaglio di musica usando l'interfaccia utente di Windows Media Player. Il contenuto Ripped viene aggiunto automaticamente alla libreria in base alle preferenze dell'utente. Per ulteriori informazioni sulle preferenze utente per il ritaglio di CD, vedere la sezione relativa alla copia di musica da CDs nella Guida di Windows Media Player.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPCdromRip (VB e C#)**](iwmpcdromrip--vb-and-c.md)
</dt> <dt>

[**IWMPCdromRip.stopRip**](wmplibiwmpcdromrip-iwmpcdromrip-stoprip--vb-and-c.md)
</dt> <dt>

[**Copia di un CD**](ripping-a-cd.md)
</dt> </dl>

 

 





