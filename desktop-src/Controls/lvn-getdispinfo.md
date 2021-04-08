---
title: Codice di notifica LVN_GETDISPINFO (COMmctrl. h)
description: Inviato da un controllo di visualizzazione elenco alla relativa finestra padre. Si tratta di una richiesta per la finestra padre per fornire le informazioni necessarie per visualizzare o ordinare un elemento della visualizzazione elenco. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 04310e39-69bc-45d7-958c-00452279d7a9
keywords:
- Controlli di Windows per il codice di notifica LVN_GETDISPINFO
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
ms.openlocfilehash: f1585524dd447c4a1324dc5c7a235490de776fb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103744002"
---
# <a name="lvn_getdispinfo-notification-code"></a>\_Codice di notifica GETDISPINFO di LVN

Inviato da un controllo di visualizzazione elenco alla relativa finestra padre. Si tratta di una richiesta per la finestra padre per fornire le informazioni necessarie per visualizzare o ordinare un elemento della visualizzazione elenco. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
LVN_GETDISPINFO
        
    pdi = (NMLVDISPINFO*) lParam
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) . In input la struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) contenuta in questa struttura specifica il tipo di informazioni richieste e identifica l'elemento o l'elemento secondario di interesse. Utilizzare la struttura **LVITEM** per restituire al controllo le informazioni richieste. Se il gestore di messaggi imposta il \_ flag LVIF di \_ SetItem nel membro **mask** della struttura **LVITEM** , il controllo List-View archivia le informazioni richieste e non le richiede di nuovo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Il ricevitore di notifiche esegue il cast di *lParam* per recuperare la struttura [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) . Il parametro *wParam* contiene il codice di notifica.

Un controllo di visualizzazione elenco Invia il codice di notifica **\_ GETDISPINFO LVN** per recuperare le informazioni sull'elemento archiviate dall'applicazione anziché dal controllo. Le informazioni possono essere informazioni sul testo o sull'icona per un elemento. Può anche essere informazioni sullo stato dell'elemento. Per ulteriori informazioni sull'implementazione dello stato dell'elemento in base a un callback, vedere il messaggio [**LVM \_ SETCALLBACKMASK**](lvm-setcallbackmask.md) .

Per altre informazioni sui callback di visualizzazione elenco, vedere [elementi di callback e maschera di callback](list-view-controls-overview.md).

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato il modo in cui questo codice di notifica può essere gestito per impostare il testo nelle colonne di una visualizzazione elenco. I dati per ogni elemento sono contenuti nella struttura seguente.


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



Il codice seguente è riportato dal \_ gestore di notifiche WM nella procedura della finestra di dialogo.


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
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **LVN \_ GETDISPINFOW** (Unicode) e **LVN \_ GETDISPINFOA** (ANSI)<br/>           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SETDISPINFO LVN**](lvn-setdispinfo.md)
</dt> </dl>

 

 





