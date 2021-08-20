---
title: Proprietà IMsTscAx ConnectingText
description: Specifica il testo visualizzato al centro nel controllo mentre il controllo è connesso.
ms.assetid: 9bc82074-988f-491b-80e3-00c3f7ba437a
ms.tgt_platform: multiple
keywords:
- Proprietà ConnectingText Servizi Desktop remoto
- Proprietà ConnectingText Servizi Desktop remoto , interfaccia IMsTscAx
- Interfaccia IMsTscAx Servizi Desktop remoto , proprietà ConnectingText
- Proprietà ConnectingText Servizi Desktop remoto , interfaccia IMsRdpClient
- Interfaccia IMsRdpClient Servizi Desktop remoto proprietà ConnectingText
- Proprietà ConnectingText Servizi Desktop remoto , interfaccia IMsRdpClient2
- Interfaccia IMsRdpClient2 Servizi Desktop remoto , proprietà ConnectingText
- Proprietà ConnectingText Servizi Desktop remoto , interfaccia IMsRdpClient3
- Interfaccia IMsRdpClient3 Servizi Desktop remoto , proprietà ConnectingText
- Proprietà ConnectingText Servizi Desktop remoto , interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto , proprietà ConnectingText
- Proprietà ConnectingText Servizi Desktop remoto , interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto , proprietà ConnectingText
- Proprietà ConnectingText Servizi Desktop remoto , interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto , proprietà ConnectingText
- Proprietà ConnectingText Servizi Desktop remoto , interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto , proprietà ConnectingText
- Proprietà ConnectingText Servizi Desktop remoto , interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto , proprietà ConnectingText
- Proprietà ConnectingText Servizi Desktop remoto , interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto , proprietà ConnectingText
topic_type:
- apiref
api_name:
- IMsTscAx.ConnectingText
- IMsTscAx.get_ConnectingText
- IMsTscAx.put_ConnectingText
- IMsRdpClient.ConnectingText
- IMsRdpClient.get_ConnectingText
- IMsRdpClient.put_ConnectingText
- IMsRdpClient2.ConnectingText
- IMsRdpClient2.get_ConnectingText
- IMsRdpClient2.put_ConnectingText
- IMsRdpClient3.ConnectingText
- IMsRdpClient3.get_ConnectingText
- IMsRdpClient3.put_ConnectingText
- IMsRdpClient4.ConnectingText
- IMsRdpClient4.get_ConnectingText
- IMsRdpClient4.put_ConnectingText
- IMsRdpClient5.ConnectingText
- IMsRdpClient5.get_ConnectingText
- IMsRdpClient5.put_ConnectingText
- IMsRdpClient6.ConnectingText
- IMsRdpClient6.get_ConnectingText
- IMsRdpClient6.put_ConnectingText
- IMsRdpClient7.ConnectingText
- IMsRdpClient7.get_ConnectingText
- IMsRdpClient7.put_ConnectingText
- IMsRdpClient8.ConnectingText
- IMsRdpClient8.get_ConnectingText
- IMsRdpClient8.put_ConnectingText
- IMsRdpClient9.ConnectingText
- IMsRdpClient9.get_ConnectingText
- IMsRdpClient9.put_ConnectingText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7342e47658e77d9fb29ef03ab1995e5263c78a8e31d2f020852e5fa10864a031
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129673"
---
# <a name="imstscaxconnectingtext-property"></a>Proprietà IMsTscAx::ConnectingText

Specifica il testo visualizzato al centro nel controllo mentre il controllo è connesso.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_ConnectingText(
  [in]  BSTR newVal
);

HRESULT get_ConnectingText(
  [out] BSTR *pConnectingText
);
```



## <a name="property-value"></a>Valore proprietà

Nuovo testo visualizzato.

## <a name="error-codes"></a>Codici di errore

Restituisce **S \_ OK in** caso di esito positivo.

Restituisce un **HRESULT** diverso da zero se si verifica un errore.

## <a name="remarks"></a>Commenti

Un esempio di testo di connessione è "Connessione al server ...".

L'impostazione **della proprietà ConnectingText** è facoltativa. Se non è impostato, il controllo viene visualizzato vuoto prima che venga stabilita una connessione.

Questa proprietà può essere impostata solo se il controllo non è nello stato connesso. Restituisce **E \_ FAIL** se viene chiamato quando il controllo è connesso. È possibile verificare se il controllo è connesso rispondendo agli eventi di connessione in [**IMsTscAxEvents**](imstscaxevents-interface.md) o esaminando la [**proprietà Connected.**](imstscax-connected.md)

Il **metodo della proprietà get \_ ConnectingText** alloca la memoria necessaria per il buffer a cui punta il *parametro pConnectingText.* Le chiamate alle applicazioni C/C++ devono liberare la memoria con una chiamata alla [**funzione SysFreeString.**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) Questa operazione non è necessaria per i client Visual Basic e script.

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

 

