---
title: IMsTscAx Domain - proprietà
description: Specifica il dominio a cui accede l'utente corrente.
ms.assetid: 5d9a2048-5f5d-43ca-a8b8-400dac7d7472
ms.tgt_platform: multiple
keywords:
- Proprietà di dominio Servizi Desktop remoto
- Proprietà di dominio Servizi Desktop remoto, interfaccia IMsTscAx
- Interfaccia IMsTscAx Servizi Desktop remoto , proprietà Domain
- Proprietà di dominio Servizi Desktop remoto, interfaccia IMsRdpClient
- Interfaccia IMsRdpClient Servizi Desktop remoto , proprietà Domain
- Proprietà di dominio Servizi Desktop remoto, interfaccia IMsRdpClient2
- Interfaccia IMsRdpClient2 Servizi Desktop remoto , proprietà Domain
- Proprietà di dominio Servizi Desktop remoto, interfaccia IMsRdpClient3
- Interfaccia IMsRdpClient3 Servizi Desktop remoto , proprietà Domain
- Proprietà di dominio Servizi Desktop remoto, interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto , proprietà Domain
- Proprietà di dominio Servizi Desktop remoto, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto , proprietà Domain
- Proprietà di dominio Servizi Desktop remoto, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto , proprietà Domain
- Proprietà di dominio Servizi Desktop remoto, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto , proprietà Domain
- Proprietà di dominio Servizi Desktop remoto, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto , proprietà Domain
- Proprietà di dominio Servizi Desktop remoto, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto , proprietà Domain
topic_type:
- apiref
api_name:
- IMsTscAx.Domain
- IMsTscAx.get_Domain
- IMsTscAx.put_Domain
- IMsRdpClient.Domain
- IMsRdpClient.get_Domain
- IMsRdpClient.put_Domain
- IMsRdpClient2.Domain
- IMsRdpClient2.get_Domain
- IMsRdpClient2.put_Domain
- IMsRdpClient3.Domain
- IMsRdpClient3.get_Domain
- IMsRdpClient3.put_Domain
- IMsRdpClient4.Domain
- IMsRdpClient4.get_Domain
- IMsRdpClient4.put_Domain
- IMsRdpClient5.Domain
- IMsRdpClient5.get_Domain
- IMsRdpClient5.put_Domain
- IMsRdpClient6.Domain
- IMsRdpClient6.get_Domain
- IMsRdpClient6.put_Domain
- IMsRdpClient7.Domain
- IMsRdpClient7.get_Domain
- IMsRdpClient7.put_Domain
- IMsRdpClient8.Domain
- IMsRdpClient8.get_Domain
- IMsRdpClient8.put_Domain
- IMsRdpClient9.Domain
- IMsRdpClient9.get_Domain
- IMsRdpClient9.put_Domain
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 498098b57ef5ecb19958f6ef0e082022a92f15bab7f1fbfc74bef62d928e8726
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125431"
---
# <a name="imstscaxdomain-property"></a>Proprietà IMsTscAx::D omain

Specifica il dominio a cui accede l'utente corrente.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_Domain(
  [in]  BSTR newVal
);

HRESULT get_Domain(
  [out] BSTR *pDomain
);
```



## <a name="property-value"></a>Valore proprietà

Nuovo nome di dominio.

## <a name="error-codes"></a>Codici di errore

Restituisce **S \_ OK in** caso di esito positivo.

## <a name="remarks"></a>Commenti

L'impostazione **della proprietà Domain** è facoltativa. Se non è impostato, l'utente può scegliere un dominio quando viene visualizzata la Windows di dialogo Accesso durante la connessione.

Il **metodo get \_ Domain** alloca la memoria necessaria per il buffer a cui punta il *parametro pDomain.* Le chiamate alle applicazioni C/C++ devono liberare la memoria con una chiamata alla [**funzione SysFreeString.**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) Questa operazione non è necessaria per i client Visual Basic e script.

Questa proprietà può essere impostata solo se il controllo non è nello stato connesso. Restituisce **E \_ FAIL** se viene chiamato quando il controllo è connesso. È possibile verificare se il controllo è connesso rispondendo agli eventi di connessione in [**IMsTscAxEvents**](imstscaxevents-interface.md) o esaminando la [**proprietà Connected.**](imstscax-connected.md)

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

[**Connesso**](imstscax-connected.md)
</dt> <dt>

[**IMsTscAx**](imstscax-interface.md)
</dt> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

