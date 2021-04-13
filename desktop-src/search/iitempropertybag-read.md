---
description: Determina la lettura di una o più proprietà dall'elenco delle proprietà. L'interfaccia IItemPropertyBag è supportata solo in Windows XP e Windows Server 2003 e non deve più essere utilizzata.
ms.assetid: 78a63ef0-1b79-4b07-9121-a6fbd1116c4b
title: 'Metodo IItemPropertyBag:: Read'
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
ms.openlocfilehash: ef7af13dc42239a2823d7e7ca9b8def4748519fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342941"
---
# <a name="iitempropertybagread-method"></a>Metodo IItemPropertyBag:: Read

Determina la lettura di una o più proprietà dall'elenco delle proprietà. L'interfaccia [**IItemPropertyBag**](iitempropertybag.md) è supportata solo in Windows XP e windows Server 2003 e non deve più essere utilizzata.

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

*cProperties* \[ in\]
</dt> <dd>

Numero di proprietà da leggere. Questo argomento specifica il numero di elementi nelle matrici in *pPropBag*, *pvarValue* e *phrError*.

</dd> <dt>

*pPropBag* \[ in\]
</dt> <dd>

Puntatore a una matrice di strutture [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) che specifica le proprietà richieste.

</dd> <dt>

*pvarValue* \[ out\]
</dt> <dd>

Riceve un puntatore che restituisce una matrice di strutture **Variant** che riceve i valori della proprietà.

</dd> <dt>

*phrError* \[ out\]
</dt> <dd>

Puntatore a una matrice di valori **HRESULT** che riceve il risultato di ogni lettura della proprietà. In questa matrice devono essere presenti almeno gli elementi *cProperties* .

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

 

 




