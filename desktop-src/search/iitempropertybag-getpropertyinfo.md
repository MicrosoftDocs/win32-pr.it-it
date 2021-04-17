---
description: Ottiene le informazioni necessarie per leggere o salvare le proprietà nell'elenco delle proprietà. L'interfaccia IItemPropertyBag è supportata solo in Windows XP e Windows Server 2003 e non deve più essere utilizzata.
ms.assetid: 1667b67d-9dd2-48a6-81dd-c8b06834cef0
title: 'Metodo IItemPropertyBag:: GetPropertyInfo'
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
ms.openlocfilehash: a64b064c6c6d3708edc353db136fcad599d14adb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306102"
---
# <a name="iitempropertybaggetpropertyinfo-method"></a>Metodo IItemPropertyBag:: GetPropertyInfo

Ottiene le informazioni necessarie per leggere o salvare le proprietà nell'elenco delle proprietà. L'interfaccia [**IItemPropertyBag**](iitempropertybag.md) è supportata solo in Windows XP e windows Server 2003 e non deve più essere utilizzata.

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

*IProperty* \[ in\]
</dt> <dd>

Indice in base zero della prima proprietà per la quale vengono richieste informazioni.

</dd> <dt>

*cProperties* \[ in\]
</dt> <dd>

Numero di proprietà per cui ottenere informazioni. Questo argomento specifica il numero di elementi di matrice in *pPropBag*.

</dd> <dt>

*pPropBag* \[ out\]
</dt> <dd>

Puntatore a una matrice di strutture [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) che riceve le informazioni per le proprietà.

</dd> <dt>

*pcProperties* \[ out\]
</dt> <dd>

Riceve un puntatore a una variabile **ULONG** che riceve il numero di proprietà per le quali sono state recuperate le informazioni.

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

 

 




