---
description: Funzione proxy per il metodo Lock.
ms.assetid: c9d67b35-092b-4f0b-a292-879576a046bf
title: IWICBitmap_Lock_Proxy funzione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmap_Lock_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 98415428a020129d884a036fab121511e489ec96af3a5606e25283dfec69c21d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118207232"
---
# <a name="iwicbitmap_lock_proxy-function"></a>Funzione proxy di blocco IWICBitmap \_ \_

Funzione proxy per il [**metodo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-lock) Lock.

## <a name="syntax"></a>Sintassi


```C++
HRESULT IWICBitmap_Lock_Proxy(
  _In_        IWICBitmap     *THIS_PTR,
  _In_  const WICRect        *prcLock,
  _In_        DWORD          flags,
  _Out_       IWICBitmapLock **ppILock
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*QUESTO \_ PTR* \[ in\]
</dt> <dd>

Tipo: **[ **IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\***

Puntatore a [**questo oggetto IWICBitmap.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)

</dd> <dt>

*prcLock* \[ Pollici\]
</dt> <dd>

Tipo: **const [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect) \***

Rettangolo a cui accedere.

</dd> <dt>

*flag* \[ Pollici\]
</dt> <dd>

Tipo: **DWORD**

Modalità di accesso che si desidera ottenere per il blocco.

</dd> <dt>

*ppILock* \[ Cambio\]
</dt> <dd>

Tipo: **[ **IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock)\*\***

Puntatore che riceve la posizione di memoria bloccata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questa funzione ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Osservazioni

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP con SP2, Windows solo \[ app desktop vista\]<br/>                                                                                              |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



 

 




