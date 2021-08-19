---
description: Funzione di callback definita dall'utente che consente al chiamante della funzione CryptUIDlgSelectCertificate di gestire la visualizzazione dei certificati che l'utente seleziona per la visualizzazione.
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
ms.openlocfilehash: a0d78569990874c87082d57045cf8075043c6edccc96b507d2d8dc72a58fb379
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117978977"
---
# <a name="pfnccertdisplayproc-callback-function"></a>Funzione di callback PFNCCERTDISPLAYPROC

La **funzione PFNCCERTDISPLAYPROC** è una funzione di callback definita dall'utente che consente al chiamante della funzione [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) di gestire la visualizzazione dei certificati selezionati dall'utente per la visualizzazione.

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

*pCertContext* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura CERT \_ CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) che rappresenta il certificato da visualizzare.

</dd> <dt>

*hWndSelCertDlg* \[ Pollici\]
</dt> <dd>

Handle per la finestra di dialogo da cui è stato selezionato il certificato per la visualizzazione.

</dd> <dt>

*pvCallbackData* \[ Pollici\]
</dt> <dd>

Dati aggiuntivi usati dalla funzione di callback.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione restituisce **TRUE** per indicare che gestisce la visualizzazione del certificato e che la finestra di dialogo non deve visualizzare il certificato. Se questa funzione restituisce **FALSE,** nella finestra di dialogo viene visualizzato il certificato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/> |



 

 




