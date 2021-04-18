---
title: Metodo IWMPCdromBurn startBurn
description: Il metodo startBurn brucia il CD.
ms.assetid: e852c011-5f54-469f-aead-37fa711ef876
keywords:
- Metodo startBurn Windows Media Player
- Metodo startBurn Windows Media Player, interfaccia IWMPCdromBurn
- Interfaccia IWMPCdromBurn Windows Media Player, metodo startBurn
topic_type:
- apiref
api_name:
- IWMPCdromBurn.startBurn
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe185d8993286e4be3935b43f6c1e9757623309d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329654"
---
# <a name="iwmpcdromburnstartburn-method"></a>Metodo IWMPCdromBurn:: startBurn

Il metodo **startBurn** brucia il CD.

## <a name="syntax"></a>Sintassi


```CSharp
public void startBurn();
```


```VB

Public Sub startBurn()
Implements IWMPCdromBurn.startBurn
```





## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Prima di chiamare questo metodo, il valore di **burnstate** deve essere WmpbsReady o wmpbsStopped.

Questo metodo non funzionerà se l'unità CD non è un masterizzatore o se il disco nell'unità non è scrivibile. Utilizzare **l'** oggetto per determinare se è possibile masterizzare un CD.

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

[**IWMPCdromBurn. disavailable (VB e C#)**](wmplibiwmpcdromburn-iwmpcdromburn-isavailable--vb-and-c.md)
</dt> <dt>

[**IWMPCdromBurn. stopBurn (VB e C#)**](wmplibiwmpcdromburn-iwmpcdromburn-stopburn-iwmpcdromburn.md)
</dt> </dl>

 

 





