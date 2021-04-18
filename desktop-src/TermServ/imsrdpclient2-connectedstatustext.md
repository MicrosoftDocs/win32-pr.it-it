---
title: Proprietà ConnectedStatusText di IMsRdpClient2
description: Contiene il testo visualizzato nell'area client del controllo mentre il controllo è nello stato connesso.
ms.assetid: c3d8433b-2fb0-413d-88a3-667149f858ba
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà ConnectedStatusText
- Servizi Desktop remoto proprietà ConnectedStatusText, interfaccia IMsRdpClient2
- Interfaccia IMsRdpClient2 Servizi Desktop remoto, proprietà ConnectedStatusText
- Servizi Desktop remoto proprietà ConnectedStatusText, interfaccia IMsRdpClient3
- Interfaccia IMsRdpClient3 Servizi Desktop remoto, proprietà ConnectedStatusText
- Servizi Desktop remoto proprietà ConnectedStatusText, interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto, proprietà ConnectedStatusText
- Servizi Desktop remoto proprietà ConnectedStatusText, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto, proprietà ConnectedStatusText
- Servizi Desktop remoto proprietà ConnectedStatusText, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto, proprietà ConnectedStatusText
- Servizi Desktop remoto proprietà ConnectedStatusText, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, proprietà ConnectedStatusText
- Servizi Desktop remoto proprietà ConnectedStatusText, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, proprietà ConnectedStatusText
- Servizi Desktop remoto proprietà ConnectedStatusText, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, proprietà ConnectedStatusText
- Servizi Desktop remoto proprietà ConnectedStatusText, interfaccia IMsRdpClient10
- Interfaccia IMsRdpClient10 Servizi Desktop remoto, proprietà ConnectedStatusText
topic_type:
- apiref
api_name:
- IMsRdpClient2.ConnectedStatusText
- IMsRdpClient2.get_ConnectedStatusText
- IMsRdpClient2.put_ConnectedStatusText
- IMsRdpClient3.ConnectedStatusText
- IMsRdpClient3.get_ConnectedStatusText
- IMsRdpClient3.put_ConnectedStatusText
- IMsRdpClient4.ConnectedStatusText
- IMsRdpClient4.get_ConnectedStatusText
- IMsRdpClient4.put_ConnectedStatusText
- IMsRdpClient5.ConnectedStatusText
- IMsRdpClient5.get_ConnectedStatusText
- IMsRdpClient5.put_ConnectedStatusText
- IMsRdpClient6.ConnectedStatusText
- IMsRdpClient6.get_ConnectedStatusText
- IMsRdpClient6.put_ConnectedStatusText
- IMsRdpClient7.ConnectedStatusText
- IMsRdpClient7.get_ConnectedStatusText
- IMsRdpClient7.put_ConnectedStatusText
- IMsRdpClient8.ConnectedStatusText
- IMsRdpClient8.get_ConnectedStatusText
- IMsRdpClient8.put_ConnectedStatusText
- IMsRdpClient9.ConnectedStatusText
- IMsRdpClient9.get_ConnectedStatusText
- IMsRdpClient9.put_ConnectedStatusText
- IMsRdpClient10.ConnectedStatusText
- IMsRdpClient10.get_ConnectedStatusText
- IMsRdpClient10.put_ConnectedStatusText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fd6ee2ac155aa3fc4873ee1a5eb890774b50978
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301227"
---
# <a name="imsrdpclient2connectedstatustext-property"></a>Proprietà IMsRdpClient2:: ConnectedStatusText

Contiene il testo visualizzato nell'area client del controllo mentre il controllo è nello stato connesso.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_ConnectedStatusText(
  [in]  BSTR newVal
);

HRESULT get_ConnectedStatusText(
  [out] BSTR *pConnectedStatusText
);
```



## <a name="property-value"></a>Valore proprietà

La proprietà **ConnectedStatusText** contiene il testo visualizzato nell'area client del controllo mentre il controllo è nello stato connesso.

## <a name="error-codes"></a>Codici di errore

Se l'operazione ha esito positivo, restituire **S \_ OK** .

## <a name="remarks"></a>Commenti

Testo da visualizzare nell'area client del controllo mentre il controllo è nello stato connesso. Si tratta del testo visibile, ad esempio quando l'utente passa il controllo alla modalità schermo intero in un Web browser, uno scenario che lascia una parte del controllo ospitata nel browser.

Il metodo **get \_ ConnectedStatusText** alloca la memoria necessaria per il buffer a cui punta il parametro *pConnectedStatusText* . La chiamata di applicazioni C/C++ deve liberare la memoria con una chiamata alla funzione [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) . Questa operazione non è necessaria per Visual Basic e client di scripting.

Impossibile impostare questa proprietà quando il controllo è connesso. È possibile verificare se il controllo è connesso chiamando il metodo [**IMsTscAx:: Get \_ Connected**](imstscax-connected.md) .

Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClient2 è definito come e7e17dc4-3b71-4ba7-A8E6-281ffadca28f<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

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

 

