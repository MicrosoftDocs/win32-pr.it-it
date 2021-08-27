---
title: LVN_GETDISPINFO codice di notifica (Commctrl.h)
description: Inviato da un controllo visualizzazione elenco alla relativa finestra padre. Si tratta di una richiesta per la finestra padre di fornire le informazioni necessarie per visualizzare o ordinare un elemento della visualizzazione elenco. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 04310e39-69bc-45d7-958c-00452279d7a9
keywords:
- LVN_GETDISPINFO codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- LVN_GETDISPINFO
- LVN_GETDISPINFOA
- LVN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f4f4fc6917b0de699d1ca561f46bc7789aa15eea7c40aa3681fe74991e3a122
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088821"
---
# <a name="lvn_getdispinfo-notification-code"></a>Codice di notifica \_ LVN GETDISPINFO

Inviato da un controllo visualizzazione elenco alla relativa finestra padre. Si tratta di una richiesta per la finestra padre di fornire le informazioni necessarie per visualizzare o ordinare un elemento della visualizzazione elenco. Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
LVN_GETDISPINFO
        
    pdi = (NMLVDISPINFO*) lParam
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMLVDISPINFO.**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) In input, la [**struttura LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) contenuta in questa struttura specifica il tipo di informazioni necessarie e identifica l'elemento o l'elemento secondario di interesse. Usare la **struttura LVITEM** per restituire le informazioni richieste al controllo. Se il gestore di messaggi imposta il flag LVIF DI SETITEM nel membro mask della struttura \_ \_ **LVITEM,**  il controllo visualizzazione elenco archivia le informazioni richieste e non le richiederà di nuovo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Il ricevitore della notifica esegue il cast *di lParam* per recuperare la [**struttura NMLVDISPINFO.**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) Il *parametro wParam* contiene il codice di notifica.

Un controllo visualizzazione elenco invia il codice di notifica **\_ LVN GETDISPINFO** per recuperare le informazioni sull'elemento archiviate dall'applicazione anziché dal controllo. Le informazioni possono essere informazioni di testo o icona per un elemento. Può anche essere informazioni sullo stato dell'elemento. Per altre informazioni sull'implementazione dello stato dell'elemento in base al callback, vedere il messaggio [**LVM \_ SETCALLBACKMASK.**](lvm-setcallbackmask.md)

Per altre informazioni sui callback di visualizzazione elenco, vedere [Elementi di callback e Maschera di callback](list-view-controls-overview.md).

## <a name="examples"></a>Esempio

L'esempio seguente illustra come questo codice di notifica può essere gestito per impostare il testo nelle colonne di una visualizzazione elenco. I dati per ogni elemento sono mantenuti nella struttura seguente.


```C++
 typedef struct tagPETINFO
{
    TCHAR szName[50];
    TCHAR szBreed[50];
    TCHAR szGender[7];
    TCHAR szPrice[20];
    GroupIds iGroup;
} PETINFO;
            
```



Di seguito è riportato il gestore WM \_ NOTIFY nella procedura della finestra di dialogo.


```C++
    case WM_NOTIFY:
        switch (((LPNMHDR) lParam)->code)
        {
        case LVN_GETDISPINFO:
            {
                NMLVDISPINFO* plvdi = (NMLVDISPINFO*)lParam;    
                switch (plvdi->item.iSubItem)
                {
                case 0:
                    // rgPetInfo is an array of PETINFO structures.
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szName;
                    break;

                case 1:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szBreed;
                    break;

                case 2:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szGender;
                    break;

                case 3:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szPrice;
                    break;

                default:
                    break;
                }
                return TRUE;
            }
      // More notifications...
      }
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **LVN \_ GETDISPINFOW** (Unicode) e **LVN \_ GETDISPINFOA** (ANSI)<br/>           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LVN \_ SETDISPINFO**](lvn-setdispinfo.md)
</dt> </dl>

 

 





