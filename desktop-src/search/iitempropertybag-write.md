---
description: Fa in modo che una o più proprietà siano salvate nel contenitore delle proprietà. L'interfaccia IItemPropertyBag è supportata solo in Windows XP e Windows Server 2003 e non deve più essere usata.
ms.assetid: 35491fbc-fb1c-4bad-86e8-9f19856ed7cb
title: Metodo IItemPropertyBag::Write
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPropertyBag.Write
api_type:
- COM
api_location: ''
ms.openlocfilehash: e8860653244cef53739c7d104405a176c1ec63d2de1d3434b1d25e3206c431aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863110"
---
# <a name="iitempropertybagwrite-method"></a>Metodo IItemPropertyBag::Write

Fa in modo che una o più proprietà siano salvate nel contenitore delle proprietà. [**L'interfaccia IItemPropertyBag**](iitempropertybag.md) è supportata solo in Windows XP e Windows Server 2003 e non deve più essere usata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Write(
  [in] ULONG    cProperties,
  [in] ITEMPROP *pPropBag,
  [in] VARIANT  *pvarValue
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*cProperties* \[ Pollici\]
</dt> <dd>

Numero di proprietà da salvare. Questo argomento specifica il numero di elementi nelle matrici in *pPropBag* e *pvarValue*.

</dd> <dt>

*pPropBag* \[ Pollici\]
</dt> <dd>

Puntatore a una matrice [**di strutture ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) che specifica le proprietà da salvare.

</dd> <dt>

*pvarValue* \[ Pollici\]
</dt> <dd>

Puntatore a **un variant** il cui tipo dipende dal tipo di dati delle informazioni sulle proprietà in esso contenute.

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

 

 




