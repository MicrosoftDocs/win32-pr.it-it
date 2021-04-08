---
title: TfEditCookie (msctf. h)
description: Il tipo di dati TfEditCookie identifica una sessione di modifica con un blocco.
ms.assetid: 1de17286-5d56-4302-a144-5fe6ca7d5557
keywords:
- TfEditCookie
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69281bc38b5df6c22dd5306877aecdb8025af84a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047816"
---
# <a name="tfeditcookie"></a>TfEditCookie

Il tipo di dati **TfEditCookie** identifica una sessione di modifica con un blocco.


```C++
typedef DWORD TfEditCookie;
```



## <a name="remarks"></a>Commenti

Il tipo di dati **TfEditCookie** viene fornito dal gestore TSF e viene usato da un client (servizio applicazione o testo) per identificare una sessione di modifica con un blocco di sola lettura o di lettura/scrittura in diversi metodi.

Viene ottenuto un valore **TfEditCookie** in uno dei modi seguenti.

-   Il client chiama [ITfDocumentMgr:: CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext).
-   Il gestore TSF chiama il metodo client [ITfEditSession::D oeditsession](/windows/desktop/api/Msctf/nf-msctf-itfeditsession-doeditsession) .
-   Il gestore TSF chiama il metodo client [ITfCompositionSink:: OnCompositionTerminated](/windows/desktop/api/Msctf/nf-msctf-itfcompositionsink-oncompositionterminated) .
-   Il gestore TSF chiama il metodo client [ITfCleanupContextSink:: OnCleanupContext](/windows/desktop/api/Msctf/nf-msctf-itfcleanupcontextsink-oncleanupcontext) .
-   Il gestore TSF chiama il metodo client [ITfTextEditSink:: OnEndEdit](/windows/desktop/api/Msctf/nf-msctf-itftexteditsink-onendedit) .

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

[**ITfCleanupContextSink::OnCleanupContext**](/windows/desktop/api/Msctf/nf-msctf-itfcleanupcontextsink-oncleanupcontext)
</dt> <dt>

[**ITfCompositionSink::OnCompositionTerminated**](/windows/desktop/api/Msctf/nf-msctf-itfcompositionsink-oncompositionterminated)
</dt> <dt>

[**ITfDocumentMgr:: CreateContext**](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext)
</dt> <dt>

[**ITfEditSession::D oEditSession**](/windows/desktop/api/Msctf/nf-msctf-itfeditsession-doeditsession)
</dt> <dt>

[**ITfTextEditSink::OnEndEdit**](/windows/desktop/api/Msctf/nf-msctf-itftexteditsink-onendedit)
</dt> </dl>

 

 





