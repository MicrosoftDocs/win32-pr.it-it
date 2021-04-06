---
title: Proprietà DisconnectedText di IMsTscAx
description: Specifica il testo visualizzato al centro del controllo prima che venga terminata una connessione.
ms.assetid: ec7efe7a-8fb9-4c45-8e16-78951365de13
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà DisconnectedText
- Servizi Desktop remoto proprietà DisconnectedText, interfaccia IMsTscAx
- Interfaccia IMsTscAx Servizi Desktop remoto, proprietà DisconnectedText
- Servizi Desktop remoto proprietà DisconnectedText, interfaccia IMsRdpClient
- Interfaccia IMsRdpClient Servizi Desktop remoto, proprietà DisconnectedText
- Servizi Desktop remoto proprietà DisconnectedText, interfaccia IMsRdpClient2
- Interfaccia IMsRdpClient2 Servizi Desktop remoto, proprietà DisconnectedText
- Servizi Desktop remoto proprietà DisconnectedText, interfaccia IMsRdpClient3
- Interfaccia IMsRdpClient3 Servizi Desktop remoto, proprietà DisconnectedText
- Servizi Desktop remoto proprietà DisconnectedText, interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto, proprietà DisconnectedText
- Servizi Desktop remoto proprietà DisconnectedText, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto, proprietà DisconnectedText
- Servizi Desktop remoto proprietà DisconnectedText, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto, proprietà DisconnectedText
- Servizi Desktop remoto proprietà DisconnectedText, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, proprietà DisconnectedText
- Servizi Desktop remoto proprietà DisconnectedText, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, proprietà DisconnectedText
- Servizi Desktop remoto proprietà DisconnectedText, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, proprietà DisconnectedText
topic_type:
- apiref
api_name:
- IMsTscAx.DisconnectedText
- IMsTscAx.get_DisconnectedText
- IMsTscAx.put_DisconnectedText
- IMsRdpClient.DisconnectedText
- IMsRdpClient.get_DisconnectedText
- IMsRdpClient.put_DisconnectedText
- IMsRdpClient2.DisconnectedText
- IMsRdpClient2.get_DisconnectedText
- IMsRdpClient2.put_DisconnectedText
- IMsRdpClient3.DisconnectedText
- IMsRdpClient3.get_DisconnectedText
- IMsRdpClient3.put_DisconnectedText
- IMsRdpClient4.DisconnectedText
- IMsRdpClient4.get_DisconnectedText
- IMsRdpClient4.put_DisconnectedText
- IMsRdpClient5.DisconnectedText
- IMsRdpClient5.get_DisconnectedText
- IMsRdpClient5.put_DisconnectedText
- IMsRdpClient6.DisconnectedText
- IMsRdpClient6.get_DisconnectedText
- IMsRdpClient6.put_DisconnectedText
- IMsRdpClient7.DisconnectedText
- IMsRdpClient7.get_DisconnectedText
- IMsRdpClient7.put_DisconnectedText
- IMsRdpClient8.DisconnectedText
- IMsRdpClient8.get_DisconnectedText
- IMsRdpClient8.put_DisconnectedText
- IMsRdpClient9.DisconnectedText
- IMsRdpClient9.get_DisconnectedText
- IMsRdpClient9.put_DisconnectedText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4768e639cbfb1543e06c03f2d9e6566d0adb147e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742127"
---
# <a name="imstscaxdisconnectedtext-property"></a>IMsTscAx::D Proprietà isconnectedText

Specifica il testo visualizzato al centro del controllo prima che venga terminata una connessione.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_DisconnectedText(
  [in]  BSTR newVal
);

HRESULT get_DisconnectedText(
  [out] BSTR *pDisconnectedText
);
```



## <a name="property-value"></a>Valore proprietà

Nuovo testo visualizzato.

## <a name="error-codes"></a>Codici di errore

Se l'operazione ha esito positivo, restituire **S \_ OK** .

## <a name="remarks"></a>Commenti

L'impostazione della proprietà **DisconnectedText** è facoltativa. Se non viene specificato, il controllo appare vuoto prima che venga stabilita una connessione.

Questa proprietà può essere impostata solo se il controllo non è nello stato connesso. Il metodo restituisce **E ha \_ esito negativo** se viene chiamato dopo la connessione del controllo. È possibile verificare se il controllo è connesso rispondendo agli eventi di connessione in [**IMsTscAxEvents**](imstscaxevents-interface.md) o esaminando la proprietà [**connessa**](imstscax-connected.md) .

Questo metodo alloca la memoria necessaria per il buffer a cui punta il parametro *pDisconnectedText* . La chiamata di applicazioni C/C++ deve liberare la memoria con una chiamata alla funzione [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) . Questa operazione non è necessaria per Visual Basic e client di scripting.

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

 

