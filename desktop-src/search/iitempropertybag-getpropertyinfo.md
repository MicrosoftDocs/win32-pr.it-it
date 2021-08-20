---
description: Ottiene le informazioni necessarie per leggere o salvare le proprietà nell'elenco delle proprietà. L'interfaccia IItemPropertyBag è supportata solo in Windows XP e Windows Server 2003 e non deve più essere usata.
ms.assetid: 1667b67d-9dd2-48a6-81dd-c8b06834cef0
title: Metodo IItemPropertyBag::GetPropertyInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPropertyBag.GetPropertyInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: 7a69ceff2236a101f18ee06b4a87dd60e35ca69e73fdeb085232f102f8450d7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863090"
---
# <a name="iitempropertybaggetpropertyinfo-method"></a>Metodo IItemPropertyBag::GetPropertyInfo

Ottiene le informazioni necessarie per leggere o salvare le proprietà nell'elenco delle proprietà. [**L'interfaccia IItemPropertyBag**](iitempropertybag.md) è supportata solo in Windows XP e Windows Server 2003 e non deve più essere usata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetPropertyInfo(
  [in]  ULONG    iProperty,
  [in]  ULONG    cProperties,
  [out] ITEMPROP *pPropBag,
  [out] ULONG    *pcProperties
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*iProperty* \[ Pollici\]
</dt> <dd>

Indice in base zero della prima proprietà per la quale vengono richieste informazioni.

</dd> <dt>

*cProperties* \[ Pollici\]
</dt> <dd>

Numero di proprietà per cui ottenere informazioni. Questo argomento specifica il numero di elementi di matrice in *pPropBag.*

</dd> <dt>

*pPropBag* \[ Cambio\]
</dt> <dd>

Puntatore a una matrice [**di strutture ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) che riceve le informazioni per le proprietà.

</dd> <dt>

*proprietà pcProperties* \[ Cambio\]
</dt> <dd>

Riceve un puntatore a una **variabile ULONG** che riceve il numero di proprietà per le quali sono stati recuperati dati.

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

 

 




