---
title: Proprietà IMsRdpClientAdvancedSettings5 BitmapVirtualCache32BppSize
description: Imposta o recupera le dimensioni del file della cache virtuale per bitmap bpp (32 bit per pixel).
ms.assetid: 7084293a-ae75-4711-a8d8-f813117333e7
ms.tgt_platform: multiple
keywords:
- Proprietà BitmapVirtualCache32BppSize Servizi Desktop remoto
- Proprietà BitmapVirtualCache32BppSize Servizi Desktop remoto , interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto , proprietà BitmapVirtualCache32BppSize
- Proprietà BitmapVirtualCache32BppSize Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto , proprietà BitmapVirtualCache32BppSize
- Proprietà BitmapVirtualCache32BppSize Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto , proprietà BitmapVirtualCache32BppSize
- Proprietà BitmapVirtualCache32BppSize Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto , proprietà BitmapVirtualCache32BppSize
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings5.get_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings5.put_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings6.BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings6.get_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings6.put_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings7.BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings7.get_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings7.put_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings8.BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings8.get_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings8.put_BitmapVirtualCache32BppSize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb33ee817a9410beb95e91be674de1a96cdbf78f92f5aaa7e3298447804cc1d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118608410"
---
# <a name="imsrdpclientadvancedsettings5bitmapvirtualcache32bppsize-property"></a>Proprietà IMsRdpClientAdvancedSettings5::BitmapVirtualCache32BppSize

Imposta o recupera le dimensioni del file della cache virtuale per bitmap bpp (32 bit per pixel).

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_BitmapVirtualCache32BppSize(
  [in]  LONG bitmapVirtualCache32BppSize
);

HRESULT get_BitmapVirtualCache32BppSize(
  [out] LONG *pbitmapVirtualCache32BppSize
);
```



## <a name="property-value"></a>Valore proprietà

Imposta le dimensioni del file di cache virtuale per 32 bitmap bpp, in megabyte (MB). Il valore massimo è 48 MB.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                         |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                   |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings5 è definito come FBA7F64E-6783-4405-DA45-FA4A763DABD0<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 





