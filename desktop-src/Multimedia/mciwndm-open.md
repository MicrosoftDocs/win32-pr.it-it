---
title: MCIWNDM_OPEN messaggio (Vfw.h)
description: Il messaggio MCIWNDM \_ OPEN apre un dispositivo MCI e lo associa a una finestra MCIWnd.
ms.assetid: ad1dfe0f-015b-45a9-ab88-cc0bdf0aa057
keywords:
- MCIWNDM_OPEN messaggio Windows Multimediali
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
ms.openlocfilehash: 03bebf9573303e3560b385425e7642106120c41456a21c1c4b80bc158328a864
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119428901"
---
# <a name="mciwndm_open-message"></a>Messaggio MCIWNDM \_ OPEN

Il **messaggio MCIWNDM \_ OPEN** apre un dispositivo MCI e lo associa a una finestra MCIWnd. Per i dispositivi MCI che usano file di dati, questa macro può anche aprire un file di dati specificato, assegnare un nome a un nuovo file da creare o visualizzare una finestra di dialogo per consentire all'utente di selezionare un file da aprire. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**MCIWndOpen.**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen)


```C++
MCIWNDM_OPEN 
wParam = (WPARAM) (UINT) wFlags; 
lParam = (LPARAM) (LPVOID) szFile; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wFlags"></span><span id="wflags"></span><span id="WFLAGS"></span>*Wflags*
</dt> <dd>

Flag associati al dispositivo o al file da aprire. Il flag MCIWNDOPENF NEW specifica che deve essere creato un nuovo file con il nome \_ specificato in **szFile**.

</dd> <dt>

<span id="szFile"></span><span id="szfile"></span><span id="SZFILE"></span>*szFile*
</dt> <dd>

Puntatore a una stringa con terminazione Null che identifica il nome del file o del dispositivo MCI da aprire. Specificare 1 per questo parametro per visualizzare la finestra di dialogo Apri.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen)
</dt> </dl>

 

 





