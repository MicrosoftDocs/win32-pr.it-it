---
title: Proprietà FullScreenTitle di IMsTscAx
description: Specifica il titolo della finestra visualizzata quando il controllo è in modalità schermo intero.
ms.assetid: 441aea43-2d1c-44b7-a74f-e375e711fb4f
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà FullScreenTitle
- Servizi Desktop remoto proprietà FullScreenTitle, interfaccia IMsTscAx
- Interfaccia IMsTscAx Servizi Desktop remoto, proprietà FullScreenTitle
- Servizi Desktop remoto proprietà FullScreenTitle, interfaccia IMsRdpClient
- Interfaccia IMsRdpClient Servizi Desktop remoto, proprietà FullScreenTitle
- Servizi Desktop remoto proprietà FullScreenTitle, interfaccia IMsRdpClient2
- Interfaccia IMsRdpClient2 Servizi Desktop remoto, proprietà FullScreenTitle
- Servizi Desktop remoto proprietà FullScreenTitle, interfaccia IMsRdpClient3
- Interfaccia IMsRdpClient3 Servizi Desktop remoto, proprietà FullScreenTitle
- Servizi Desktop remoto proprietà FullScreenTitle, interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto, proprietà FullScreenTitle
- Servizi Desktop remoto proprietà FullScreenTitle, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto, proprietà FullScreenTitle
- Servizi Desktop remoto proprietà FullScreenTitle, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto, proprietà FullScreenTitle
- Servizi Desktop remoto proprietà FullScreenTitle, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, proprietà FullScreenTitle
- Servizi Desktop remoto proprietà FullScreenTitle, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, proprietà FullScreenTitle
- Servizi Desktop remoto proprietà FullScreenTitle, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, proprietà FullScreenTitle
topic_type:
- apiref
api_name:
- IMsTscAx.FullScreenTitle
- IMsTscAx.put_FullScreenTitle
- IMsRdpClient.FullScreenTitle
- IMsRdpClient.put_FullScreenTitle
- IMsRdpClient2.FullScreenTitle
- IMsRdpClient2.put_FullScreenTitle
- IMsRdpClient3.FullScreenTitle
- IMsRdpClient3.put_FullScreenTitle
- IMsRdpClient4.FullScreenTitle
- IMsRdpClient4.put_FullScreenTitle
- IMsRdpClient5.FullScreenTitle
- IMsRdpClient5.put_FullScreenTitle
- IMsRdpClient6.FullScreenTitle
- IMsRdpClient6.put_FullScreenTitle
- IMsRdpClient7.FullScreenTitle
- IMsRdpClient7.put_FullScreenTitle
- IMsRdpClient8.FullScreenTitle
- IMsRdpClient8.put_FullScreenTitle
- IMsRdpClient9.FullScreenTitle
- IMsRdpClient9.put_FullScreenTitle
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1384d1582f4f0089df55030c22471438575bd072
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120202"
---
# <a name="imstscaxfullscreentitle-property"></a>Proprietà IMsTscAx:: FullScreenTitle

Specifica il titolo della finestra visualizzata quando il controllo è in modalità schermo intero.

Questa proprietà è di sola scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_FullScreenTitle(
  [in] BSTR fullScreenTitle
);
```



## <a name="property-value"></a>Valore proprietà

Titolo della finestra. La lunghezza massima di questa stringa è MAX \_ Path-1 caratteri.

## <a name="error-codes"></a>Codici di errore

Se l'operazione ha esito positivo, restituire **S \_ OK** .

## <a name="remarks"></a>Commenti

Questa proprietà viene utilizzata per impostare il titolo della finestra del controllo quando la connessione viene aperta in modalità schermo intero. Non usare questa proprietà per la modalità a schermo intero gestita dal contenitore. Quando viene chiamato il metodo [**IMsTscAdvancedSettings::p UT \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) , nella finestra del contenitore viene visualizzato il titolo della finestra.

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

[**IMsTscAx**](imstscax-interface.md)
</dt> </dl>

 

 





