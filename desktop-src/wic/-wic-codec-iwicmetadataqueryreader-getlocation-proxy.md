---
description: Funzione proxy per il metodo getLocation.
ms.assetid: 2dc4767b-9992-4e5a-a171-2de19178d912
title: Funzione IWICMetadataQueryReader_GetLocation_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryReader_GetLocation_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 40dd23df0e1004687a945889d2598d41ca0e2e72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319118"
---
# <a name="iwicmetadataqueryreader_getlocation_proxy-function"></a>\_Funzione proxy getLocation IWICMetadataQueryReader \_

Funzione proxy per il metodo [**getLocation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getlocation) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT IWICMetadataQueryReader_GetLocation_Proxy(
  _In_    IWICMetadataQueryReader *THIS_PTR,
  _In_    UINT                    cchMaxLength,
  _Inout_ WCHAR                   *wzNamespace,
  _Out_   UINT                    *pcchActualLength
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Questa \_ PTR* \[ in\]
</dt> <dd>

Tipo: **[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) \** _

Puntatore a questo oggetto [_ *IWICMetadataQueryReader* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) .

</dd> <dt>

*cchMaxLength* \[ in\]
</dt> <dd>

Tipo: **uint**

Lunghezza del buffer *wzNamespace* .

</dd> <dt>

*wzNamespace* \[ in uscita\]
</dt> <dd>

Tipo: **WCHAR \** _

Puntatore che riceve il percorso dello spazio dei nomi corrente.

</dd> <dt>

_pcchActualLength * \[ out\]
</dt> <dd>

Tipo: **uint \** _

Lunghezza effettiva del buffer necessaria per recuperare il percorso dello spazio dei nomi corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: _ *HRESULT**

Se questa funzione ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Osservazioni

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP con SP2, \[ solo app desktop di Windows Vista\]<br/>                                                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt> </dl> |



 

 




