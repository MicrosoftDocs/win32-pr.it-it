---
title: Identificatori di oggetto (Winuser.h)
description: Questo argomento descrive gli identificatori di Microsoft Active Accessibility, i valori a 32 bit che identificano le categorie di oggetti accessibili all'interno di una finestra.
ms.assetid: dc1603f8-29e5-4acd-817a-c6957feaff6c
topic_type:
- apiref
api_name:
- OBJID_ALERT
- OBJID_CARET
- OBJID_CLIENT
- OBJID_CURSOR
- OBJID_HSCROLL
- OBJID_NATIVEOM
- OBJID_MENU
- OBJID_QUERYCLASSNAMEIDX
- OBJID_SIZEGRIP
- OBJID_SOUND
- OBJID_SYSMENU
- OBJID_TITLEBAR
- OBJID_VSCROLL
- OBJID_WINDOW
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b91bf70333d4ba7d607e465851f7f217aec43b0a081ec020017321fe30a7ede
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118565066"
---
# <a name="object-identifiers-winuserh"></a>Identificatori di oggetto (Winuser.h)

Questo argomento descrive gli identificatori Microsoft Active Accessibility oggetti, valori a 32 bit che identificano categorie di oggetti accessibili all'interno di una finestra.  Microsoft Active Accessibility server e i provider di Automazione interfaccia utente Microsoft usano gli identificatori di oggetto per determinare l'oggetto a cui fa riferimento una richiesta di messaggio [**WM \_ GETOBJECT.**](wm-getobject.md)

I client ricevono questi valori nella funzione di callback [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) e li usano per identificare le parti di una finestra. I server usano questi valori per identificare le parti corrispondenti di una finestra quando chiamano [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) o quando rispondono al [**messaggio WM \_ GETOBJECT.**](wm-getobject.md)

I server possono definire ID oggetto personalizzati per identificare altre categorie di oggetti all'interno delle applicazioni. Agli ID oggetto personalizzati devono essere assegnati valori positivi perché Microsoft Active Accessibility riserva zero e tutti i valori negativi per gli identificatori di oggetto standard seguenti.

Le costanti seguenti sono definite in winuser.h:



| Costante                                                                                                                                                                                    | Descrizione                                                                                                                                                                                                                                                                                                                                            |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OBJID_ALERT"></span><span id="objid_alert"></span><dl> <dt>**AVVISO \_ OBJID**</dt> </dl>                                     | Avviso associato a una finestra o a un'applicazione. Le finestre di messaggio fornite dal sistema sono gli unici elementi dell'interfaccia utente che inviano eventi con questo identificatore di oggetto. Le applicazioni server non possono usare le **funzioni AccessibleObjectFrom**_X_ con questo identificatore di oggetto. Si tratta di un problema noto con Microsoft Active Accessibility.<br/>          |
| <span id="OBJID_CARET"></span><span id="objid_caret"></span><dl> <dt>**PUNTO DI \_ CARET OBJID**</dt> </dl>                                     | Barra di inserimento del testo (punto di inserimento) nella finestra.<br/>                                                                                                                                                                                                                                                                                               |
| <span id="OBJID_CLIENT"></span><span id="objid_client"></span><dl> <dt>**OBJID \_ CLIENT**</dt> </dl>                                  | Area client della finestra. Nella maggior parte dei casi, il sistema operativo controlla gli elementi frame e l'oggetto client contiene tutti gli elementi controllati dall'applicazione. I server elaborano solo i [**messaggi WM \_ GETOBJECT**](wm-getobject.md) in cui *lParam* è OBJID \_ CLIENT, OBJID \_ WINDOW o un identificatore di oggetto personalizzato.<br/> |
| <span id="OBJID_CURSOR"></span><span id="objid_cursor"></span><dl> <dt>**CURSORE \_ OBJID**</dt> </dl>                                  | Puntatore del mouse. Nel sistema è presente un solo puntatore del mouse e non è un elemento figlio di alcuna finestra.<br/>                                                                                                                                                                                                                                      |
| <span id="OBJID_HSCROLL"></span><span id="objid_hscroll"></span><dl> <dt>**OBJID \_ HSCROLL**</dt> </dl>                               | Barra di scorrimento orizzontale della finestra.<br/>                                                                                                                                                                                                                                                                                                         |
| <span id="OBJID_NATIVEOM"></span><span id="objid_nativeom"></span><dl> <dt>**OBJID \_ NATIVEOM**</dt> </dl>                            | In risposta a questo identificatore di oggetto, le applicazioni di terze parti possono esporre il proprio modello a oggetti. Le applicazioni di terze parti possono restituire qualsiasi interfaccia COM in risposta a questo identificatore di oggetto.<br/>                                                                                                                                             |
| <span id="OBJID_MENU"></span><span id="objid_menu"></span><dl> <dt>**OBJID \_ MENU**</dt> </dl>                                        | Barra dei menu della finestra.<br/>                                                                                                                                                                                                                                                                                                                      |
| <span id="OBJID_QUERYCLASSNAMEIDX"></span><span id="objid_queryclassnameidx"></span><dl> <dt>**OBJID \_ QUERYCLASSNAMEIDX**</dt> </dl> | Identificatore di oggetto utilizzato Oleacc.dll internamente. Per altre informazioni, vedere [Appendice F: Valori degli identificatori di oggetto per OBJID \_ QUERYCLASSNAMEIDX.](appendix-f--object-identifier-values-for-objid-queryclassnameidx.md)<br/>                                                                                                                  |
| <span id="OBJID_SIZEGRIP"></span><span id="objid_sizegrip"></span><dl> <dt>**OBJID \_ SIZEGRIP**</dt> </dl>                            | Ridimensionamento della finestra: componente frame facoltativo che si trova nell'angolo inferiore destro della cornice della finestra.<br/>                                                                                                                                                                                                                                  |
| <span id="OBJID_SOUND"></span><span id="objid_sound"></span><dl> <dt>**AUDIO \_ OBJID**</dt> </dl>                                     | Oggetto audio. Gli oggetti sonori non hanno posizioni dello schermo o elementi figlio, ma hanno attributi di nome e stato. Sono elementi figlio dell'applicazione che riproduce il suono.<br/>                                                                                                                                                         |
| <span id="OBJID_SYSMENU"></span><span id="objid_sysmenu"></span><dl> <dt>**OBJID \_ SYSMENU**</dt> </dl>                               | Menu di sistema della finestra.<br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="OBJID_TITLEBAR"></span><span id="objid_titlebar"></span><dl> <dt>**BARRA DEL TITOLO \_ OBJID**</dt> </dl>                            | Barra del titolo della finestra.<br/>                                                                                                                                                                                                                                                                                                                     |
| <span id="OBJID_VSCROLL"></span><span id="objid_vscroll"></span><dl> <dt>**OBJID \_ VSCROLL**</dt> </dl>                               | Barra di scorrimento verticale della finestra.<br/>                                                                                                                                                                                                                                                                                                           |
| <span id="OBJID_WINDOW"></span><span id="objid_window"></span><dl> <dt>**FINESTRA \_ OBJID**</dt> </dl>                                  | La finestra stessa anziché un oggetto figlio.<br/>                                                                                                                                                                                                                                                                                               |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



 

 





