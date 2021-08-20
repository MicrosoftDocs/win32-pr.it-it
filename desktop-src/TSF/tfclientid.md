---
title: TfClientId (Msctf.h)
description: Il tipo di dati TfClientId viene usato per identificare il client.
ms.assetid: 984dc390-6e15-4491-8c06-77c27c5bdd6f
keywords:
- TfClientId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 347784de9014ee300bf6931e4d005c366a0cc9b67f57f82515010ece5b68551e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117950418"
---
# <a name="tfclientid"></a>TfClientId

Il **tipo di dati TfClientId** viene usato per identificare il client.


```C++
typedef DWORD TfClientId;
```



## <a name="remarks"></a>Commenti

All'interno di TSF, le applicazioni e i servizi di testo sono in genere definiti client. Ogni client riceve un identificatore univoco che usa per identificarsi quando chiama vari metodi di gestione di TSF. Questo identificatore è di tipo **TfClientId.**

Il **tipo di dati TfClientId** viene fornito dal gestore TSF. Un'applicazione ottiene un **valore TfClientId** quando chiama [ITfThreadMgr::Activate.](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate) Il valore TfClientId per un servizio di testo viene passato al [metodo ITfTextInputProcessor::Activate.](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) Qualsiasi oggetto che non rientra nelle categorie precedenti può ottenere un identificatore client chiamando [ITfClientId::GetClientId](/windows/desktop/api/Msctf/nf-msctf-itfclientid-getclientid).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[ app desktop \| UWP\]<br/>                    |
| Server minimo supportato<br/> | Windows app desktop di Windows 2000 Server \[ \| app UWP\]<br/>                          |
| Componente ridistribuibile<br/>          | TSF 1.0 in Windows 2000 Professional<br/>                                      |
| Intestazione<br/>                   | <dl> <dt>Msctf.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Msctf.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITfClientId::GetClientId**](/windows/desktop/api/Msctf/nf-msctf-itfclientid-getclientid)
</dt> <dt>

[**ITfTextInputProcessor::Activate**](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate)
</dt> <dt>

[**ITfThreadMgr::Activate**](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate)
</dt> </dl>

 

 





