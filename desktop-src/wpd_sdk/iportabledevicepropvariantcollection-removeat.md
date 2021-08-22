---
description: "Metodo IPortableDevicePropVariantCollection::RemoveAt: il metodo RemoveAt rimuove l'elemento archiviato nella posizione specificata dall'indice specificato."
ms.assetid: cfee2454-5103-48ce-b9f7-1f76f5c18b6d
title: Metodo IPortableDevicePropVariantCollection::RemoveAt (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.RemoveAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 311b3511329ed15f5afd83d5a84c0c5abd62fe3f44000962fbdcd2f8ddd67c9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026899"
---
# <a name="iportabledevicepropvariantcollectionremoveat-method"></a>Metodo IPortableDevicePropVariantCollection::RemoveAt

Il **metodo RemoveAt** rimuove l'elemento archiviato nella posizione specificata dall'indice specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RemoveAt(
  [in] const DWORD dwIndex
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwIndex* \[ Pollici\]
</dt> <dd>

Specifica l'indice dell'elemento da rimuovere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **valore HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                  | Descrizione                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Il metodo è riuscito.<br/>                 |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | L'indice specificato non è compreso nell'intervallo.<br/> |



 

## <a name="remarks"></a>Commenti

È necessario specificare un indice in base zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




