---
title: Metodo IMsRdpClient RequestClose
description: Richiede un arresto normale del controllo Desktop remoto ActiveX normale.
ms.assetid: 0b930a00-f134-4da2-a752-8fd131a22043
ms.tgt_platform: multiple
keywords:
- Metodo RequestClose Servizi Desktop remoto
- Metodo RequestClose Servizi Desktop remoto, interfaccia IMsRdpClient
- Interfaccia IMsRdpClient Servizi Desktop remoto , metodo RequestClose
- Metodo RequestClose Servizi Desktop remoto, interfaccia IMsRdpClient2
- Interfaccia IMsRdpClient2 Servizi Desktop remoto , metodo RequestClose
- Metodo RequestClose Servizi Desktop remoto, interfaccia IMsRdpClient3
- Interfaccia IMsRdpClient3 Servizi Desktop remoto , metodo RequestClose
- Metodo RequestClose Servizi Desktop remoto, interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto , metodo RequestClose
- Metodo RequestClose Servizi Desktop remoto, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto , metodo RequestClose
- Metodo RequestClose Servizi Desktop remoto, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto , metodo RequestClose
- Metodo RequestClose Servizi Desktop remoto, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto , metodo RequestClose
- Metodo RequestClose Servizi Desktop remoto, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto , metodo RequestClose
- Metodo RequestClose Servizi Desktop remoto, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto , metodo RequestClose
- Metodo RequestClose Servizi Desktop remoto, interfaccia IMsRdpClient10
- Interfaccia IMsRdpClient10 Servizi Desktop remoto , metodo RequestClose
topic_type:
- apiref
api_name:
- IMsRdpClient.RequestClose
- IMsRdpClient2.RequestClose
- IMsRdpClient3.RequestClose
- IMsRdpClient4.RequestClose
- IMsRdpClient5.RequestClose
- IMsRdpClient6.RequestClose
- IMsRdpClient7.RequestClose
- IMsRdpClient8.RequestClose
- IMsRdpClient9.RequestClose
- IMsRdpClient10.RequestClose
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae812c27b0c280ca3a6cd879d5af86181de85793ec6092441fb83b45c74d8656
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010181"
---
# <a name="imsrdpclientrequestclose-method"></a>Metodo IMsRdpClient::RequestClose

Richiede un arresto normale del controllo Desktop remoto ActiveX normale. Un arresto normale può includere l'arresto della sessione Servizi Desktop remoto dell'utente, ma non arresta il server host sessione Desktop remoto (Host sessione Desktop remoto).

## <a name="syntax"></a>Sintassi


```C++
HRESULT RequestClose(
  [out] ControlCloseStatus *pCloseStatus
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pCloseStatus* \[ Cambio\]
</dt> <dd>

Valore [**dell'enumerazione ControlCloseStatus**](controlclosestatus.md) che indica se l'applicazione può chiudere immediatamente il controllo. Di seguito è riportato un elenco di valori possibili.

<dt>

<span id="controlCloseCanProceed"></span><span id="controlclosecanproceed"></span><span id="CONTROLCLOSECANPROCEED"></span>

<span id="controlCloseCanProceed"></span><span id="controlclosecanproceed"></span><span id="CONTROLCLOSECANPROCEED"></span>**controlCloseCanProceed** (0x0000)


</dt> <dd>

L'applicazione contenitore può procedere alla chiusura immediata del controllo. Questo valore può anche indicare che la connessione è già terminata.

</dd> <dt>

<span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>

<span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>**controlCloseWaitForEvents** (0x0001)


</dt> <dd>

L'applicazione contenitore non deve chiudere immediatamente il controllo. l'applicazione deve attendere che uno degli eventi descritti nella sezione Osservazioni seguente si verifichi prima della chiusura.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **S \_ OK in** caso di esito positivo.

## <a name="remarks"></a>Commenti

Se il *parametro pCloseStatus* è uguale a **controlCloseWaitForEvents**, l'applicazione deve attendere che si verifichi uno degli eventi seguenti prima che l'applicazione chiuda il controllo:

-   [**IMsTscAxEvents::OnDisconnected**](imstscaxevents-ondisconnected.md). Se l'utente non è connesso alla sessione Servizi Desktop remoto, l'applicazione può chiamare la funzione [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) per eliminare tutte le finestre e quindi chiudere il controllo.
-   [**IMsTscAxEvents::OnConfirmClose**](imstscaxevents-onconfirmclose.md). Se l'utente è connesso alla sessione Servizi Desktop remoto, il controllo genera un **evento OnConfirmClose.** Questo evento consente all'applicazione di richiedere all'utente se chiudere la connessione. Se l'utente risponde sì al prompt, l'applicazione contenitore può chiamare [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) per eliminare tutte le finestre e chiudere il controllo.

**RequestClose** consente a un'applicazione contenitore di richiedere all'utente se chiudere una connessione. Per altre informazioni, vedere [**IMsTscAxEvents::OnConfirmClose**](imstscaxevents-onconfirmclose.md).

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
</dt> <dt>

[**IMsTscAxEvents::OnConfirmClose**](imstscaxevents-onconfirmclose.md)
</dt> <dt>

[**IMsTscAxEvents::OnDisconnected**](imstscaxevents-ondisconnected.md)
</dt> </dl>

 

