---
description: Funzione di callback definita dall'utente che consente al chiamante della funzione CryptUIDlgSelectCertificate di gestire la visualizzazione dei certificati selezionati dall'utente per la visualizzazione.
ms.assetid: fdb9e9e0-02f1-42e0-9a11-204d916a1a88
title: Funzione di callback PFNCCERTDISPLAYPROC
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PFNCCERTDISPLAYPROC
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 7371e983b339ff8bfa9edb1b7fb795ab64596a98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050075"
---
# <a name="pfnccertdisplayproc-callback-function"></a>Funzione di callback PFNCCERTDISPLAYPROC

La funzione **PFNCCERTDISPLAYPROC** è una funzione di callback definita dall'utente che consente al chiamante della funzione [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) di gestire la visualizzazione dei certificati selezionati dall'utente per la visualizzazione.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI * PFNCCERTDISPLAYPROC(
  _In_ PCCERT_CONTEXT pCertContext,
  _In_ HWND           hWndSelCertDlg,
  _In_ void           *pvCallbackData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pCertContext* \[ in\]
</dt> <dd>

Puntatore a una struttura [**del \_ contesto**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) del certificato che rappresenta il certificato da visualizzare.

</dd> <dt>

*hWndSelCertDlg* \[ in\]
</dt> <dd>

Handle per la finestra di dialogo da cui è stato selezionato il certificato per la visualizzazione.

</dd> <dt>

*pvCallbackData* \[ in\]
</dt> <dd>

Dati aggiuntivi utilizzati dalla funzione di callback.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione restituisce **true** per indicare che gestisce la visualizzazione del certificato e che la finestra di dialogo non deve visualizzare il certificato. Se questa funzione restituisce **false**, nella finestra di dialogo verrà visualizzato il certificato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/> |



 

 




