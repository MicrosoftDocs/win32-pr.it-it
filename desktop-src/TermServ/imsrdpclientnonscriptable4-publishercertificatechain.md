---
title: Proprietà PublisherCertificateChain di IMsRdpClientNonScriptable4
description: Controlla la catena di certificati del server di pubblicazione. La catena è archiviata in una variante di tipo VT \_ ByRef che contiene un puntatore a una \_ struttura del contesto della catena di certificati \_ . Per informazioni sulle \_ strutture ByRef VT, vedere VARIANT e VARIANTARG.
ms.assetid: 27ab0aff-1aef-4701-abe0-849bf32c9773
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà PublisherCertificateChain
- Servizi Desktop remoto proprietà PublisherCertificateChain, interfaccia IMsRdpClientNonScriptable4
- Interfaccia IMsRdpClientNonScriptable4 Servizi Desktop remoto, proprietà PublisherCertificateChain
- Servizi Desktop remoto proprietà PublisherCertificateChain, interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto, proprietà PublisherCertificateChain
- Servizi Desktop remoto proprietà PublisherCertificateChain, oggetto MsRdpClient6
- Oggetto MsRdpClient6 Servizi Desktop remoto, proprietà PublisherCertificateChain
- Servizi Desktop remoto proprietà PublisherCertificateChain, oggetto MsRdpClient7
- Oggetto MsRdpClient7 Servizi Desktop remoto, proprietà PublisherCertificateChain
- Servizi Desktop remoto proprietà PublisherCertificateChain, oggetto MsRdpClient8
- Oggetto MsRdpClient8 Servizi Desktop remoto, proprietà PublisherCertificateChain
- Servizi Desktop remoto proprietà PublisherCertificateChain, oggetto MsRdpClient9
- Oggetto MsRdpClient9 Servizi Desktop remoto, proprietà PublisherCertificateChain
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.PublisherCertificateChain
- IMsRdpClientNonScriptable4.get_PublisherCertificateChain
- IMsRdpClientNonScriptable4.put_PublisherCertificateChain
- IMsRdpClientNonScriptable5.PublisherCertificateChain
- IMsRdpClientNonScriptable5.get_PublisherCertificateChain
- IMsRdpClientNonScriptable5.put_PublisherCertificateChain
- MsRdpClient6.PublisherCertificateChain
- MsRdpClient7.PublisherCertificateChain
- MsRdpClient8.PublisherCertificateChain
- MsRdpClient9.PublisherCertificateChain
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7552483c2fc651ace1a9401e0555f90fb2584423
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874081"
---
# <a name="imsrdpclientnonscriptable4publishercertificatechain-property"></a>IMsRdpClientNonScriptable4::P proprietà ublisherCertificateChain

Controlla la catena di certificati del server di pubblicazione. La catena è archiviata in una variante di tipo **VT \_ ByRef** che contiene un puntatore a una struttura del [**\_ \_ contesto della catena di certificati**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context) . Per informazioni sulle **strutture \_ ByRef VT** , vedere [Variant e VARIANTARG](/windows/win32/api/oaidl/ns-oaidl-variant).

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_PublisherCertificateChain(
  [in]  VARIANT *pVarCert
);

HRESULT get_PublisherCertificateChain(
  [out] VARIANT *pVarCert
);
```



## <a name="property-value"></a>Valore proprietà

Imposta la catena di certificati del server di pubblicazione. La catena è archiviata in una variante di tipo **VT \_ ByRef** che contiene un puntatore a una struttura del [**\_ \_ contesto della catena di certificati**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context) .

## <a name="error-codes"></a>Codici di errore

Restituisce **\_ OK** se ha esito positivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                           |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IMsRdpClientNonScriptable4 è definito come f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

