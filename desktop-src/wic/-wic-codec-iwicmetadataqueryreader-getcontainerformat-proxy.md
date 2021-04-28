---
description: IWICMetadataQueryReader_GetContainerFormat_Proxy funzione proxy per il metodo GetContainerFormat.
ms.assetid: 3a909151-53c2-4f82-9ead-f689b73f5faf
title: IWICMetadataQueryReader_GetContainerFormat_Proxy funzione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryReader_GetContainerFormat_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 1fa2e34aa0e4cff05f6cdacc9cd1f340ff41af28
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097139"
---
# <a name="iwicmetadataqueryreader_getcontainerformat_proxy-function"></a>Funzione proxy IWICMetadataQueryReader \_ GetContainerFormat \_

Funzione proxy per il [**metodo GetContainerFormat.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getcontainerformat)

## <a name="syntax"></a>Sintassi


```C++
HRESULT IWICMetadataQueryReader_GetContainerFormat_Proxy(
  _In_  IWICMetadataQueryReader *THIS_PTR,
  _Out_ GUID                    *pguidContainerFormat
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*QUESTO \_ PTR* \[ in\]
</dt> <dd>

Tipo: **[ **IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\***

Puntatore a [**questo oggetto IWICMetadataQueryReader.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)

</dd> <dt>

*pguidContainerFormat* \[ Cambio\]
</dt> <dd>

Tipo: **\* GUID**

Puntatore che riceve il GUID del formato cointainer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questa funzione ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Osservazioni

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP con SP2, solo app desktop di Windows Vista \[\]<br/>                                                                                              |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2008 \[\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



 

 




