---
title: Proprietà IMsRdpClient ColorDepth
description: Profondità del colore (in bit per pixel) per la connessione del controllo.
ms.assetid: 9ba4d8fe-20cd-40e9-a71a-0dce0ddd29fc
ms.tgt_platform: multiple
keywords:
- Proprietà ColorDepth Servizi Desktop remoto
- Proprietà ColorDepth Servizi Desktop remoto, interfaccia IMsRdpClient
- Interfaccia IMsRdpClient Servizi Desktop remoto , proprietà ColorDepth
- Proprietà ColorDepth Servizi Desktop remoto, interfaccia IMsRdpClient2
- Interfaccia IMsRdpClient2 Servizi Desktop remoto , proprietà ColorDepth
- Proprietà ColorDepth Servizi Desktop remoto, interfaccia IMsRdpClient3
- Interfaccia IMsRdpClient3 Servizi Desktop remoto , proprietà ColorDepth
- Proprietà ColorDepth Servizi Desktop remoto, interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto , proprietà ColorDepth
- Proprietà ColorDepth Servizi Desktop remoto, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto , proprietà ColorDepth
- Proprietà ColorDepth Servizi Desktop remoto, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto , proprietà ColorDepth
- Proprietà ColorDepth Servizi Desktop remoto, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto , proprietà ColorDepth
- Proprietà ColorDepth Servizi Desktop remoto, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto , proprietà ColorDepth
- Proprietà ColorDepth Servizi Desktop remoto, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto , proprietà ColorDepth
- Proprietà ColorDepth Servizi Desktop remoto , interfaccia IMsRdpClient10
- Interfaccia IMsRdpClient10 Servizi Desktop remoto , proprietà ColorDepth
topic_type:
- apiref
api_name:
- IMsRdpClient.ColorDepth
- IMsRdpClient.get_ColorDepth
- IMsRdpClient.put_ColorDepth
- IMsRdpClient2.ColorDepth
- IMsRdpClient2.get_ColorDepth
- IMsRdpClient2.put_ColorDepth
- IMsRdpClient3.ColorDepth
- IMsRdpClient3.get_ColorDepth
- IMsRdpClient3.put_ColorDepth
- IMsRdpClient4.ColorDepth
- IMsRdpClient4.get_ColorDepth
- IMsRdpClient4.put_ColorDepth
- IMsRdpClient5.ColorDepth
- IMsRdpClient5.get_ColorDepth
- IMsRdpClient5.put_ColorDepth
- IMsRdpClient6.ColorDepth
- IMsRdpClient6.get_ColorDepth
- IMsRdpClient6.put_ColorDepth
- IMsRdpClient7.ColorDepth
- IMsRdpClient7.get_ColorDepth
- IMsRdpClient7.put_ColorDepth
- IMsRdpClient8.ColorDepth
- IMsRdpClient8.get_ColorDepth
- IMsRdpClient8.put_ColorDepth
- IMsRdpClient9.ColorDepth
- IMsRdpClient9.get_ColorDepth
- IMsRdpClient9.put_ColorDepth
- IMsRdpClient10.ColorDepth
- IMsRdpClient10.get_ColorDepth
- IMsRdpClient10.put_ColorDepth
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 995509385cabc18a7768300e29482b00f674ce347463b0b8aeb2c3af7e6a209b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119475751"
---
# <a name="imsrdpclientcolordepth-property"></a>Proprietà IMsRdpClient::ColorDepth

Profondità del colore (in bit per pixel) per la connessione del controllo.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_ColorDepth(
  [in]  LONG colorDepth
);

HRESULT get_ColorDepth(
  [out] LONG pcolorDepth
);
```



## <a name="property-value"></a>Valore proprietà

Profondità del colore. I valori includono 8, 15, 16, 24 e 32 bit per pixel.

## <a name="error-codes"></a>Codici di errore

Se i metodi hanno esito positivo, **viene restituito S \_ OK.** Qualsiasi altro **valore HRESULT** indica che la chiamata non è riuscita.

## <a name="remarks"></a>Commenti

Questa proprietà non può essere impostata quando il controllo è connesso.

Per altre informazioni sui Connessione Web Desktop remoto, vedere [Requisiti per Connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsRdpClient IID è definito come \_ 92b4a539-7115-4b7c-a5a9-e5d9efc2780a<br/>        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClient**](imsrdpclient-interface.md)
</dt> <dt>

[**IMsRdpClient2**](imsrdpclient2.md)
</dt> <dt>

[**IMsRdpClient3**](imsrdpclient3.md)
</dt> <dt>

[**IMsRdpClient4**](imsrdpclient4.md)
</dt> <dt>

[**IMsRdpClient5**](imsrdpclient5.md)
</dt> <dt>

[**IMsRdpClient6**](imsrdpclient6.md)
</dt> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> </dl>

 

 





