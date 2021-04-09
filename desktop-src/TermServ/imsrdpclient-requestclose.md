---
title: Metodo IMsRdpClient RequestClose
description: Richiede un arresto normale del controllo ActiveX Desktop remoto.
ms.assetid: 0b930a00-f134-4da2-a752-8fd131a22043
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del Metodo RequestClose
- Metodo RequestClose Servizi Desktop remoto, interfaccia IMsRdpClient
- Interfaccia IMsRdpClient Servizi Desktop remoto, Metodo RequestClose
- Metodo RequestClose Servizi Desktop remoto, interfaccia IMsRdpClient2
- Interfaccia IMsRdpClient2 Servizi Desktop remoto, Metodo RequestClose
- Metodo RequestClose Servizi Desktop remoto, interfaccia IMsRdpClient3
- Interfaccia IMsRdpClient3 Servizi Desktop remoto, Metodo RequestClose
- Metodo RequestClose Servizi Desktop remoto, interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto, Metodo RequestClose
- Metodo RequestClose Servizi Desktop remoto, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto, Metodo RequestClose
- Metodo RequestClose Servizi Desktop remoto, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto, Metodo RequestClose
- Metodo RequestClose Servizi Desktop remoto, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, Metodo RequestClose
- Metodo RequestClose Servizi Desktop remoto, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, Metodo RequestClose
- Metodo RequestClose Servizi Desktop remoto, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, Metodo RequestClose
- Metodo RequestClose Servizi Desktop remoto, interfaccia IMsRdpClient10
- Interfaccia IMsRdpClient10 Servizi Desktop remoto, Metodo RequestClose
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
ms.openlocfilehash: 1679b08680b962cdbff57e9bbbd1c392607d8709
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740575"
---
# <a name="imsrdpclientrequestclose-method"></a>Metodo IMsRdpClient:: RequestClose

Richiede un arresto normale del controllo ActiveX Desktop remoto. Un arresto normale può includere la chiusura della sessione di Servizi Desktop remoto dell'utente, ma non l'arresto del server di host sessione Desktop remoto (host sessione Desktop remoto).

## <a name="syntax"></a>Sintassi


```C++
HRESULT RequestClose(
  [out] ControlCloseStatus *pCloseStatus
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pCloseStatus* \[ out\]
</dt> <dd>

Valore dell'enumerazione [**ControlCloseStatus**](controlclosestatus.md) che indica se l'applicazione può chiudere immediatamente il controllo. Di seguito è riportato un elenco di valori possibili.

<dt>

<span id="controlCloseCanProceed"></span><span id="controlclosecanproceed"></span><span id="CONTROLCLOSECANPROCEED"></span>

<span id="controlCloseCanProceed"></span><span id="controlclosecanproceed"></span><span id="CONTROLCLOSECANPROCEED"></span>**controlCloseCanProceed** (0x0000)


</dt> <dd>

L'applicazione contenitore può procedere immediatamente alla chiusura del controllo. Questo valore può anche indicare che la connessione è già stata terminata.

</dd> <dt>

<span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>

<span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>**controlCloseWaitForEvents** (0x0001)


</dt> <dd>

Il controllo non deve essere chiuso immediatamente dall'applicazione contenitore; l'applicazione deve attendere che uno degli eventi descritti nella sezione Osservazioni seguente venga eseguito prima della chiusura.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione ha esito positivo, restituire **S \_ OK** .

## <a name="remarks"></a>Commenti

Se il parametro *pCloseStatus* è uguale a **controlCloseWaitForEvents**, l'applicazione deve attendere che si verifichi uno degli eventi seguenti prima che l'applicazione chiuda il controllo:

-   [**IMsTscAxEvents:: disconnected**](imstscaxevents-ondisconnected.md). Se l'utente non è connesso alla sessione di Servizi Desktop remoto, l'applicazione può chiamare la funzione [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) per eliminare definitivamente tutte le finestre e quindi chiudere il controllo.
-   [**IMsTscAxEvents:: OnConfirmClose**](imstscaxevents-onconfirmclose.md). Se l'utente è connesso alla sessione di Servizi Desktop remoto, il controllo genera un evento **OnConfirmClose** . Questo evento consente all'applicazione di richiedere all'utente se chiudere la connessione. Se l'utente risponde Sì al prompt, l'applicazione contenitore può chiamare [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) per eliminare tutte le finestre e chiudere il controllo.

**RequestClose** consente a un'applicazione contenitore di richiedere all'utente se chiudere una connessione. Per ulteriori informazioni, vedere [**IMsTscAxEvents:: OnConfirmClose**](imstscaxevents-onconfirmclose.md).

Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClient è definito come 92b4a539-7115-4B7C-a5a9-e5d9efc2780a<br/>        |



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

[**IMsTscAxEvents:: disconnected**](imstscaxevents-ondisconnected.md)
</dt> </dl>

 

