---
title: Proprietà della versione IMsTscAx
description: Specifica il numero di versione del controllo corrente.
ms.assetid: 91ddeb4c-9d61-41e7-af96-95b0c4884682
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto della proprietà Version
- Servizi Desktop remoto della proprietà Version, interfaccia IMsTscAx
- Interfaccia IMsTscAx Servizi Desktop remoto, proprietà Version
- Servizi Desktop remoto della proprietà Version, interfaccia IMsRdpClient
- Interfaccia IMsRdpClient Servizi Desktop remoto, proprietà Version
- Servizi Desktop remoto della proprietà Version, interfaccia IMsRdpClient2
- Interfaccia IMsRdpClient2 Servizi Desktop remoto, proprietà Version
- Servizi Desktop remoto della proprietà Version, interfaccia IMsRdpClient3
- Interfaccia IMsRdpClient3 Servizi Desktop remoto, proprietà Version
- Servizi Desktop remoto della proprietà Version, interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto, proprietà Version
- Servizi Desktop remoto della proprietà Version, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto, proprietà Version
- Servizi Desktop remoto della proprietà Version, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto, proprietà Version
- Servizi Desktop remoto della proprietà Version, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, proprietà Version
- Servizi Desktop remoto della proprietà Version, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, proprietà Version
- Servizi Desktop remoto della proprietà Version, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, proprietà Version
topic_type:
- apiref
api_name:
- IMsTscAx.Version
- IMsTscAx.get_Version
- IMsRdpClient.Version
- IMsRdpClient.get_Version
- IMsRdpClient2.Version
- IMsRdpClient2.get_Version
- IMsRdpClient3.Version
- IMsRdpClient3.get_Version
- IMsRdpClient4.Version
- IMsRdpClient4.get_Version
- IMsRdpClient5.Version
- IMsRdpClient5.get_Version
- IMsRdpClient6.Version
- IMsRdpClient6.get_Version
- IMsRdpClient7.Version
- IMsRdpClient7.get_Version
- IMsRdpClient8.Version
- IMsRdpClient8.get_Version
- IMsRdpClient9.Version
- IMsRdpClient9.get_Version
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff25f274d1f076c9c4119648ccb9cc6d82f43b33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476738"
---
# <a name="imstscaxversion-property"></a>Proprietà IMsTscAx:: Version

Specifica il numero di versione del controllo corrente.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Version(
  [out] BSTR *pVersion
);
```



## <a name="property-value"></a>Valore proprietà

Numero di versione.

## <a name="error-codes"></a>Codici di errore

Se l'operazione ha esito positivo, restituire **S \_ OK** .

## <a name="remarks"></a>Commenti

Questo metodo alloca la memoria necessaria per il buffer a cui punta il parametro *pVersion* . La chiamata di applicazioni C/C++ deve liberare la memoria con una chiamata alla funzione [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) . Questa operazione non è necessaria per Visual Basic e client di scripting.

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

 

