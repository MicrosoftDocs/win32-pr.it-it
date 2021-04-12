---
title: Messaggio WM_GESTURE (winuser. h)
description: Passa informazioni su un movimento.
ms.assetid: 4167aeb0-2c31-4b7b-ad1b-e6d37da09ef8
keywords:
- WM_GESTURE messaggio Windows Touch
topic_type:
- apiref
api_name:
- WM_GESTURE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d1184d1f54d110f84630a727decb91ad28e6c08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400764"
---
# <a name="wm_gesture-message"></a>\_Messaggio di movimento WM

Passa informazioni su un movimento.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Fornisce informazioni che identificano il comando movimento e i valori di argomento specifici del movimento. Queste informazioni sono le stesse informazioni passate nel membro **ullArguments** della struttura [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) .

</dd> <dt>

*lParam* 
</dt> <dd>

Fornisce un handle per le informazioni che identificano il comando movimento e i valori di argomento specifici del movimento. Queste informazioni vengono recuperate chiamando [**GetGestureInfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora il messaggio, deve restituire 0.

Se l'applicazione non elabora il messaggio, deve chiamare [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca). Questa operazione causerà la perdita di memoria da parte dell'applicazione perché l'handle di input tocco non verrà chiuso e la memoria del processo associata non verrà liberata.

## <a name="remarks"></a>Commenti

Nella tabella seguente sono elencati i comandi di movimento supportati.



| ID movimento            | Valore (*dwID*) | Descrizione                                                                                                                                                                                                                                                                          |
|-----------------------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_inizio GID**        | 1              | Indica l'inizio di un movimento generico.                                                                                                                                                                                                                                            |
| **\_fine GID**          | 2              | Indica un'entità finale di movimento generica.                                                                                                                                                                                                                                                     |
| **\_Zoom GID**         | 3              | Indica l'inizio dello zoom, lo spostamento dello zoom o l'arresto dello zoom. Il primo messaggio di comando **\_ Zoom GID** avvia uno zoom ma non provoca alcuno zoom. Il secondo comando di **\_ Zoom GID** attiva uno zoom rispetto allo stato contenuto nel primo **\_ Zoom GID**.                                    |
| **Pan di GID \_**          | 4              | Indica la panoramica dello spostamento o della panoramica. Il primo comando per la **\_ Panoramica di GID** indica una panoramica di avvio ma non esegue alcuna panoramica. Con il secondo messaggio del comando della **\_ Panoramica di GID** , l'applicazione inizierà la panoramica.                                                                            |
| **GID \_ ruotato**       | 5              | Indica l'avvio della rotazione o della rotazione. Il primo messaggio di comando per la **\_ rotazione GID** indica uno spostamento o una rotazione avviata, ma non viene ruotata. Il secondo messaggio di comando di rotazione **GID \_** attiverà un'operazione di rotazione relativa allo stato contenuto nella **prima \_ rotazione del GID**. |
| **GID \_ TWOFINGERTAP** | 6              | Indica il gesto di tocco a due dita.                                                                                                                                                                                                                                                    |
| **GID \_ PRESSANDTAP**  | 7              | Indica il gesto da premere e toccare.                                                                                                                                                                                                                                                 |



 

> [!Note]  
> Per abilitare il supporto legacy, è necessario che i messaggi con i comandi dei movimenti **\_ Begin** e **GID \_ end** si inoltrino usando [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).

 

La tabella seguente indica gli argomenti del movimento passati nei parametri *lParam* e *wParam* .



| ID movimento            | Movimento        | *ullArgument*                                                                                                                                                                                                                                                                                                                                                                                            | *ptsLocation* nella struttura [**GestureInfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo)                                                  |
|-----------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| **\_Zoom GID**         | Zoom avanti/indietro    | Indica la distanza tra i due punti.                                                                                                                                                                                                                                                                                                                                                           | Indica il centro dello zoom.                                                                                 |
| **Pan di GID \_**          | Dettaglio            | Indica la distanza tra i due punti.                                                                                                                                                                                                                                                                                                                                                           | Indica la posizione corrente del Pan.                                                                        |
| **GID \_ ruotato**       | Rotazione (pivot) | Indica l'angolo di rotazione se il **flag \_ Begin di GF** è impostato. In caso contrario, si tratta della modifica dell'angolo dall'avvio della rotazione. Questo oggetto è firmato per indicare la direzione della rotazione. Utilizzare l'angolo di [**\_ rotazione GID \_ \_ dall' \_ argomento**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_from_argument) e l' [**\_ \_ angolo di rotazione GID a macro \_ \_ argomento**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_to_argument) per ottenere e impostare il valore dell'angolo. | Indica il centro della rotazione che rappresenta il punto fisso in cui viene ruotato l'oggetto di destinazione. |
| **GID \_ TWOFINGERTAP** | Tocco con due dita | Indica la distanza tra le due dita.                                                                                                                                                                                                                                                                                                                                                          | Indica il centro delle due dita.                                                                          |
| **GID \_ PRESSANDTAP**  | Premere e toccare  | Indica il delta tra il primo dito e il secondo dito. Questo valore viene archiviato nei 32 bit inferiori di *ullArgument* in una struttura **Point** .                                                                                                                                                                                                                                             | Indica la posizione in cui si arresta il primo dito.                                                       |



 

> [!Note]  
> Tutte le distanze e le posizioni vengono fornite nelle coordinate dello schermo fisico.

 

> [!Note]  
> I parametri *dwID* e *ullArgument* devono essere considerati solo come allegati ai \_ \* comandi GID e non devono essere modificati dalle applicazioni.

 

## <a name="examples"></a>Esempio

Nel codice seguente viene illustrato come ottenere informazioni specifiche del movimento associate a questo messaggio.

> [!Note]  
> È necessario inviare sempre messaggi non gestiti a [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) e chiudere l'handle di input del movimento per i messaggi gestiti con una chiamata a [**CloseGestureInfoHandle**](/windows/desktop/api/winuser/nf-winuser-closegestureinfohandle). In questo esempio, il comportamento predefinito del gestore movimenti verrà eliminato perché l'handle TOUCHINPUT viene chiuso in ogni case di movimento. Se i case nel codice riportato in precedenza sono stati rimossi per i messaggi non gestiti, il gestore movimenti predefinito elaborerà i messaggi eseguendo l'invio a [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) nel caso predefinito.

 


```C++
  LRESULT DecodeGesture(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam){
    // Create a structure to populate and retrieve the extra message info.
    GESTUREINFO gi;  
    
    ZeroMemory(&gi, sizeof(GESTUREINFO));
    
    gi.cbSize = sizeof(GESTUREINFO);

    BOOL bResult  = GetGestureInfo((HGESTUREINFO)lParam, &gi);
    BOOL bHandled = FALSE;

    if (bResult){
        // now interpret the gesture
        switch (gi.dwID){
           case GID_ZOOM:
               // Code for zooming goes here     
               bHandled = TRUE;
               break;
           case GID_PAN:
               // Code for panning goes here
               bHandled = TRUE;
               break;
           case GID_ROTATE:
               // Code for rotation goes here
               bHandled = TRUE;
               break;
           case GID_TWOFINGERTAP:
               // Code for two-finger tap goes here
               bHandled = TRUE;
               break;
           case GID_PRESSANDTAP:
               // Code for roll over goes here
               bHandled = TRUE;
               break;
           default:
               // A gesture was not recognized
               break;
        }
    }else{
        DWORD dwErr = GetLastError();
        if (dwErr > 0){
            //MessageBoxW(hWnd, L"Error!", L"Could not retrieve a GESTUREINFO structure.", MB_OK);
        }
    }
    if (bHandled){
        return 0;
    }else{
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
  }
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                               |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                                  |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Notifications](notifications.md)
</dt> <dt>

[Guida alla programmazione di movimenti tocco di Windows](guide-multi-touch-gestures.md)
</dt> </dl>

 

