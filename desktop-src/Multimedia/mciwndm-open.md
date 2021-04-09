---
title: Messaggio di MCIWNDM_OPEN (VFW. h)
description: Il \_ messaggio aperto MCIWNDM apre un dispositivo MCI e lo associa a una finestra di MCIWnd.
ms.assetid: ad1dfe0f-015b-45a9-ab88-cc0bdf0aa057
keywords:
- MCIWNDM_OPEN messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_OPEN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2f232ea9076a1e0ff8c105d8c5cf94104e455c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119542"
---
# <a name="mciwndm_open-message"></a>MCIWNDM \_ messaggio aperto

Il **messaggio \_ aperto MCIWNDM** apre un dispositivo MCI e lo associa a una finestra di MCIWnd. Per i dispositivi MCI che usano file di dati, questa macro può anche aprire un file di dati specificato, denominare un nuovo file da creare o visualizzare una finestra di dialogo per consentire all'utente di selezionare un file da aprire. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) .


```C++
MCIWNDM_OPEN 
wParam = (WPARAM) (UINT) wFlags; 
lParam = (LPARAM) (LPVOID) szFile; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wFlags"></span><span id="wflags"></span><span id="WFLAGS"></span>*wFlags*
</dt> <dd>

Flag associati al dispositivo o al file da aprire. Il \_ nuovo flag MCIWNDOPENF specifica che è necessario creare un nuovo file con il nome specificato in **szFile**.

</dd> <dt>

<span id="szFile"></span><span id="szfile"></span><span id="SZFILE"></span>*szFile*
</dt> <dd>

Puntatore a una stringa con terminazione null che identifica il nome file o il nome del dispositivo MCI da aprire. Specificare 1 per questo parametro per visualizzare la finestra di dialogo Apri.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen)
</dt> </dl>

 

 





