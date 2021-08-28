---
title: Proprietà IMsTscAx DesktopHeight
description: Specifica l'altezza del controllo corrente, in pixel, sul desktop remoto iniziale.
ms.assetid: 7071053b-bdd1-408b-ab69-965c504fafb0
ms.tgt_platform: multiple
keywords:
- Proprietà DesktopHeight Servizi Desktop remoto
- Proprietà DesktopHeight Servizi Desktop remoto, interfaccia IMsTscAx
- Interfaccia IMsTscAx Servizi Desktop remoto proprietà DesktopHeight
- Proprietà DesktopHeight Servizi Desktop remoto, interfaccia IMsRdpClient
- Interfaccia IMsRdpClient Servizi Desktop remoto proprietà DesktopHeight
- Proprietà DesktopHeight Servizi Desktop remoto, interfaccia IMsRdpClient2
- Interfaccia IMsRdpClient2 Servizi Desktop remoto , proprietà DesktopHeight
- Proprietà DesktopHeight Servizi Desktop remoto, interfaccia IMsRdpClient3
- Interfaccia IMsRdpClient3 Servizi Desktop remoto proprietà DesktopHeight
- Proprietà DesktopHeight Servizi Desktop remoto, interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto , proprietà DesktopHeight
- Proprietà DesktopHeight Servizi Desktop remoto, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto proprietà DesktopHeight
- Proprietà DesktopHeight Servizi Desktop remoto, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto proprietà DesktopHeight
- Proprietà DesktopHeight Servizi Desktop remoto, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto , proprietà DesktopHeight
- Proprietà DesktopHeight Servizi Desktop remoto, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto , proprietà DesktopHeight
- Proprietà DesktopHeight Servizi Desktop remoto, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto , proprietà DesktopHeight
topic_type:
- apiref
api_name:
- IMsTscAx.DesktopHeight
- IMsTscAx.get_DesktopHeight
- IMsTscAx.put_DesktopHeight
- IMsRdpClient.DesktopHeight
- IMsRdpClient.get_DesktopHeight
- IMsRdpClient.put_DesktopHeight
- IMsRdpClient2.DesktopHeight
- IMsRdpClient2.get_DesktopHeight
- IMsRdpClient2.put_DesktopHeight
- IMsRdpClient3.DesktopHeight
- IMsRdpClient3.get_DesktopHeight
- IMsRdpClient3.put_DesktopHeight
- IMsRdpClient4.DesktopHeight
- IMsRdpClient4.get_DesktopHeight
- IMsRdpClient4.put_DesktopHeight
- IMsRdpClient5.DesktopHeight
- IMsRdpClient5.get_DesktopHeight
- IMsRdpClient5.put_DesktopHeight
- IMsRdpClient6.DesktopHeight
- IMsRdpClient6.get_DesktopHeight
- IMsRdpClient6.put_DesktopHeight
- IMsRdpClient7.DesktopHeight
- IMsRdpClient7.get_DesktopHeight
- IMsRdpClient7.put_DesktopHeight
- IMsRdpClient8.DesktopHeight
- IMsRdpClient8.get_DesktopHeight
- IMsRdpClient8.put_DesktopHeight
- IMsRdpClient9.DesktopHeight
- IMsRdpClient9.get_DesktopHeight
- IMsRdpClient9.put_DesktopHeight
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4e55d5a1f529435f0cdf6db3dcf801e7f24dda1a69e0bc1cad393942b672d4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513101"
---
# <a name="imstscaxdesktopheight-property"></a>Proprietà IMsTscAx::D esktopHeight

Specifica l'altezza del controllo corrente, in pixel, sul desktop remoto iniziale.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_DesktopHeight(
  [in]  LONG newVal
);

HRESULT get_DesktopHeight(
  [out] LONG *pVal
);
```



## <a name="property-value"></a>Valore proprietà

Nuova altezza, in pixel.

## <a name="error-codes"></a>Codici di errore

Restituisce **S \_ OK in** caso di esito positivo.

## <a name="remarks"></a>Commenti

**L'impostazione della proprietà DesktopHeight** è facoltativa, ma deve essere impostata prima di chiamare il [**Connessione**](imstscax-connect.md) metodo . Se non viene specificata un'altezza del desktop o è impostata su zero, l'altezza del desktop viene impostata sull'altezza del controllo . I valori minimo e massimo dipendono dalla versione del sistema operativo del client Desktop remoto client.

<dl> <dt>

<span id="_"></span>Windows 8/Windows Server 2012
</dt> <dd>

200 minimo, 8192 massimo

</dd> <dt>

<span id="_"></span>Windows 7/Windows Server 2008
</dt> <dd>

200 minimo, 2048 massimo

</dd> <dt>

Windows Vista
</dt> <dd>

200 minimo, 1200 massimo

</dd> </dl>

Dopo aver stabilito una connessione, qualsiasi modifica all'altezza del controllo non modifica l'altezza del desktop remoto. Al contrario, il controllo apre le barre di scorrimento o centra il desktop remoto, in base alle esigenze. Per modificare le dimensioni del desktop di una connessione attiva, usare il [**metodo IMsRdpClient8::Reconnect.**](imsrdpclient8-reconnect.md)

Per altre informazioni sui Connessione Web Desktop remoto, vedere [Requisiti per Connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAx IID è definito come \_ 8C11EFAE-92C3-11D1-BC1E-00C04FA31489<br/>            |



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

[**IMsTscAx**](imstscax-interface.md)
</dt> </dl>

 

 





