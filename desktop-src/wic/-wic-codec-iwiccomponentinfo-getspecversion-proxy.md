---
description: Funzione proxy per il metodo GetSpecVersion.
ms.assetid: 363e55c2-d6e8-4ddc-a063-c5be08232a67
title: Funzione IWICComponentInfo_GetSpecVersion_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetSpecVersion_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: a7b9b0a44eb5fd8404eecc3ad355ec280583d690
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319559"
---
# <a name="iwiccomponentinfo_getspecversion_proxy-function"></a>IWICComponentInfo \_ GetSpecVersion- \_ funzione proxy

Funzione proxy per il metodo [**GetSpecVersion**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getspecversion) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT IWICComponentInfo_GetSpecVersion_Proxy(
  _In_    IWICComponentInfo *THIS_PTR,
  _In_    UINT              cchSpecVersion,
  _Inout_ WCHAR             *wzSpecVersion,
  _Out_   UINT              *pcchActual
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Questa \_ PTR* \[ in\]
</dt> <dd>

Tipo: **[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) \** _

Puntatore a questo oggetto [_ *IWICComponentInfo* *](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) .

</dd> <dt>

*cchSpecVersion* \[ in\]
</dt> <dd>

Tipo: **uint**

Dimensioni del buffer *wzSpecVersion* .

</dd> <dt>

*wzSpecVersion* \[ in uscita\]
</dt> <dd>

Tipo: **WCHAR \** _

Quando termina, questo metodo contiene una stringa invarient delle impostazioni cultura della versione specifica del componente. Il formato della versione è NN. NN. nn. NN.

</dd> <dt>

_pcchActual * \[ out\]
</dt> <dd>

Tipo: **uint \** _

Puntatore che riceve la lunghezza effettiva della versione della specifica del componente.

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



 

 




