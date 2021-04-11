---
description: Determina il salvataggio di una o più proprietà nel contenitore delle proprietà. L'interfaccia IItemPropertyBag è supportata solo in Windows XP e Windows Server 2003 e non deve più essere utilizzata.
ms.assetid: 35491fbc-fb1c-4bad-86e8-9f19856ed7cb
title: 'Metodo IItemPropertyBag:: Write'
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
ms.openlocfilehash: 7df66487bba0c2bbef40cf3642754dff56f65835
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128507"
---
# <a name="iitempropertybagwrite-method"></a>Metodo IItemPropertyBag:: Write

Determina il salvataggio di una o più proprietà nel contenitore delle proprietà. L'interfaccia [**IItemPropertyBag**](iitempropertybag.md) è supportata solo in Windows XP e windows Server 2003 e non deve più essere utilizzata.

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

*cProperties* \[ in\]
</dt> <dd>

Numero di proprietà da salvare. Questo argomento specifica il numero di elementi nelle matrici in *pPropBag* e *pvarValue*.

</dd> <dt>

*pPropBag* \[ in\]
</dt> <dd>

Puntatore a una matrice di strutture [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) che specifica le proprietà da salvare.

</dd> <dt>

*pvarValue* \[ in\]
</dt> <dd>

Puntatore a una **variante** il cui tipo dipende dal tipo di dati delle informazioni sulla proprietà in esso contenute.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce S \_ OK. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

L'interfaccia [**IItemPropertyBag**](iitempropertybag.md) è supportata solo in Windows XP e windows Server 2003 e non deve più essere utilizzata.

Per visualizzare in anteprima gli allegati con un gestore di protocollo di terze parti in computer che eseguono Windows XP o Windows Server 2003, potrebbe essere necessario usare l'interfaccia [**IItemPropertyBag**](iitempropertybag.md) e le API seguenti: le interfacce [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPreviewerExt**](-search-iitempreviewerext.md) e [**ISearchItem**](-search-isearchitem.md) , le strutture [**LINKINFO**](-search-linkinfo.md) e [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) e l'enumerazione [**LinkType**](-search-linktype.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP con SP2 \[\]<br/> |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/> |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 3,0<br/>          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IItemPropertyBag**](iitempropertybag.md)
</dt> </dl>

 

 




