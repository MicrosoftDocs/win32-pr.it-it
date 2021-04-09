---
title: TfClientId (msctf. h)
description: Il tipo di dati TfClientId viene utilizzato per identificare il client.
ms.assetid: 984dc390-6e15-4491-8c06-77c27c5bdd6f
keywords:
- TfClientId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ffba8e1d5ea3c8114d9f567c3829141dd8902dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740874"
---
# <a name="tfclientid"></a>TfClientId

Il tipo di dati **TfClientId** viene utilizzato per identificare il client.


```C++
typedef DWORD TfClientId;
```



## <a name="remarks"></a>Commenti

In TSF, le applicazioni e i servizi di testo vengono in genere definiti client. Ogni client riceve un identificatore univoco usato per identificare se stesso quando chiama diversi metodi di gestione TSF. Questo identificatore è del tipo **TfClientId** .

Il tipo di dati **TfClientId** viene fornito dal gestore TSF. Un'applicazione ottiene un valore **TfClientId** quando chiama [ITfThreadMgr:: Activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate). Il valore TfClientId per un servizio di testo viene passato al metodo [ITfTextInputProcessor:: Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) . Qualsiasi oggetto che non soddisfa le categorie precedenti può ottenere un identificatore client chiamando [ITfClientId:: getClientID](/windows/desktop/api/Msctf/nf-msctf-itfclientid-getclientid).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App UWP di Windows 2000 Professional \[ desktop apps \|\]<br/>                    |
| Server minimo supportato<br/> | App desktop di Windows 2000 Server \[ \| UWP\]<br/>                          |
| Componente ridistribuibile<br/>          | TSF 1,0 su Windows 2000 Professional<br/>                                      |
| Intestazione<br/>                   | <dl> <dt>Msctf. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Msctf. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITfClientId:: getClientID**](/windows/desktop/api/Msctf/nf-msctf-itfclientid-getclientid)
</dt> <dt>

[**ITfTextInputProcessor:: Activate**](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate)
</dt> <dt>

[**ITfThreadMgr:: Activate**](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate)
</dt> </dl>

 

 





