---
title: Proprietà VerticalScrollBarVisible di IMsTscAx
description: Indica se il controllo Visualizza una barra di scorrimento verticale.
ms.assetid: b31e2db3-b367-4900-a2c6-51fd794341c2
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà VerticalScrollBarVisible
- Servizi Desktop remoto proprietà VerticalScrollBarVisible, interfaccia IMsTscAx
- Interfaccia IMsTscAx Servizi Desktop remoto, proprietà VerticalScrollBarVisible
- Servizi Desktop remoto proprietà VerticalScrollBarVisible, interfaccia IMsRdpClient
- Interfaccia IMsRdpClient Servizi Desktop remoto, proprietà VerticalScrollBarVisible
- Servizi Desktop remoto proprietà VerticalScrollBarVisible, interfaccia IMsRdpClient2
- Interfaccia IMsRdpClient2 Servizi Desktop remoto, proprietà VerticalScrollBarVisible
- Servizi Desktop remoto proprietà VerticalScrollBarVisible, interfaccia IMsRdpClient3
- Interfaccia IMsRdpClient3 Servizi Desktop remoto, proprietà VerticalScrollBarVisible
- Servizi Desktop remoto proprietà VerticalScrollBarVisible, interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto, proprietà VerticalScrollBarVisible
- Servizi Desktop remoto proprietà VerticalScrollBarVisible, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto, proprietà VerticalScrollBarVisible
- Servizi Desktop remoto proprietà VerticalScrollBarVisible, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto, proprietà VerticalScrollBarVisible
- Servizi Desktop remoto proprietà VerticalScrollBarVisible, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, proprietà VerticalScrollBarVisible
- Servizi Desktop remoto proprietà VerticalScrollBarVisible, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, proprietà VerticalScrollBarVisible
- Servizi Desktop remoto proprietà VerticalScrollBarVisible, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, proprietà VerticalScrollBarVisible
topic_type:
- apiref
api_name:
- IMsTscAx.VerticalScrollBarVisible
- IMsTscAx.get_VerticalScrollBarVisible
- IMsRdpClient.VerticalScrollBarVisible
- IMsRdpClient.get_VerticalScrollBarVisible
- IMsRdpClient2.VerticalScrollBarVisible
- IMsRdpClient2.get_VerticalScrollBarVisible
- IMsRdpClient3.VerticalScrollBarVisible
- IMsRdpClient3.get_VerticalScrollBarVisible
- IMsRdpClient4.VerticalScrollBarVisible
- IMsRdpClient4.get_VerticalScrollBarVisible
- IMsRdpClient5.VerticalScrollBarVisible
- IMsRdpClient5.get_VerticalScrollBarVisible
- IMsRdpClient6.VerticalScrollBarVisible
- IMsRdpClient6.get_VerticalScrollBarVisible
- IMsRdpClient7.VerticalScrollBarVisible
- IMsRdpClient7.get_VerticalScrollBarVisible
- IMsRdpClient8.VerticalScrollBarVisible
- IMsRdpClient8.get_VerticalScrollBarVisible
- IMsRdpClient9.VerticalScrollBarVisible
- IMsRdpClient9.get_VerticalScrollBarVisible
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1365a0ab6d4a1411d78496cf157f3bc49fe5db15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475778"
---
# <a name="imstscaxverticalscrollbarvisible-property"></a>Proprietà IMsTscAx:: VerticalScrollBarVisible

Indica se il controllo Visualizza una barra di scorrimento verticale.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_VerticalScrollBarVisible(
  [out] BOOL *pfVScrollVisible
);
```



## <a name="property-value"></a>Valore proprietà

Il valore di questo parametro è **true** se la barra di scorrimento verticale è visibile e **false** in caso contrario.

## <a name="error-codes"></a>Codici di errore

Se l'operazione ha esito positivo, restituire **S \_ OK** .

## <a name="remarks"></a>Commenti

Il controllo Visualizza automaticamente una barra di scorrimento verticale se l'altezza del controllo corrente è minore dell'altezza del desktop.

Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsTscAx è definito come 8C11EFAE-92C3-11D1-BC1E-00C04FA31489<br/>            |



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

[**HorizontalScrollBarVisible**](imstscax-horizontalscrollbarvisible.md)
</dt> <dt>

[**IMsTscAx**](imstscax-interface.md)
</dt> </dl>

 

 





