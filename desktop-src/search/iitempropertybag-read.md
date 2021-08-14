---
description: Fa in modo che una o più proprietà siano lette dal contenitore delle proprietà. L'interfaccia IItemPropertyBag è supportata solo in Windows XP e Windows Server 2003 e non deve più essere usata.
ms.assetid: 78a63ef0-1b79-4b07-9121-a6fbd1116c4b
title: Metodo IItemPropertyBag::Read
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPropertyBag.Read
api_type:
- COM
api_location: ''
ms.openlocfilehash: c04cf34720871b1254f16822a090f48f8d68aaeb82398744d5139486fb6dd2f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118226606"
---
# <a name="iitempropertybagread-method"></a>Metodo IItemPropertyBag::Read

Fa in modo che una o più proprietà siano lette dal contenitore delle proprietà. [**L'interfaccia IItemPropertyBag**](iitempropertybag.md) è supportata solo in Windows XP e Windows Server 2003 e non deve più essere usata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Read(
  [in]  ULONG    cProperties,
  [in]  ITEMPROP *pPropBag,
  [out] VARIANT  *pvarValue,
  [out] HRESULT  *phrError
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*cProperties* \[ Pollici\]
</dt> <dd>

Numero di proprietà da leggere. Questo argomento specifica il numero di elementi nelle matrici in *pPropBag*, *pvarValue* e *phrError*.

</dd> <dt>

*pPropBag* \[ Pollici\]
</dt> <dd>

Puntatore a una matrice [**di strutture ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) che specifica le proprietà richieste.

</dd> <dt>

*pvarValue* \[ Cambio\]
</dt> <dd>

Riceve un puntatore che restituisce una matrice di **strutture VARIANT** che riceve i valori delle proprietà.

</dd> <dt>

*phrError* \[ Cambio\]
</dt> <dd>

Puntatore a una matrice **di valori HRESULT** che riceve il risultato di ogni lettura di proprietà. In questa matrice devono essere presenti *almeno elementi cProperties.*

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce S \_ OK. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

[**L'interfaccia IItemPropertyBag**](iitempropertybag.md) è supportata solo in Windows XP e Windows Server 2003 e non deve più essere usata.

Per visualizzare in anteprima gli allegati con un gestore di protocollo di terze parti nei computer che eseguono Windows XP o Windows Server 2003, potrebbe essere necessario usare l'interfaccia [**IItemPropertyBag**](iitempropertybag.md) e le API seguenti: le interfacce [**ISearchProtocolUI,**](-search-isearchprotocolui.md) [**IItemPreviewerExt**](-search-iitempreviewerext.md) e [**ISearchItem,**](-search-isearchitem.md) le strutture [**LINKINFO**](-search-linkinfo.md) e [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) e l'enumerazione [**LINKTYPE.**](-search-linktype.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP solo con app desktop SP2 \[\]<br/> |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/> |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 3.0<br/>          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IItemPropertyBag**](iitempropertybag.md)
</dt> </dl>

 

 




