---
title: Identificatori di oggetto (winuser. h)
description: In questo argomento vengono descritti gli identificatori di oggetto Active Accessibility Microsoft, i valori a 32 bit che identificano le categorie di oggetti accessibili all'interno di una finestra.
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
ms.openlocfilehash: 1fa2cf2099c5177be6f295ef6455646762525b26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327469"
---
# <a name="object-identifiers-winuserh"></a>Identificatori di oggetto (winuser. h)

In questo argomento vengono descritti gli identificatori di oggetto Active Accessibility Microsoft, i valori a 32 bit che identificano le *categorie* di oggetti accessibili all'interno di una finestra. I server Microsoft Active Accessibility e i provider di automazione interfaccia utente Microsoft utilizzano gli identificatori di oggetto per determinare l'oggetto a cui fa riferimento una richiesta di messaggio [**WM \_ GetObject**](wm-getobject.md) .

I client ricevono questi valori nella funzione di callback [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) e li usano per identificare le parti di una finestra. I server utilizzano questi valori per identificare le parti corrispondenti di una finestra quando si chiama [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) o quando si risponde al messaggio [**WM \_ GetObject**](wm-getobject.md) .

I server possono definire ID oggetto personalizzati per identificare altre categorie di oggetti all'interno delle applicazioni. Agli ID oggetto personalizzati devono essere assegnati valori positivi perché Microsoft Active Accessibility riserva zero e tutti i valori negativi per gli identificatori di oggetto standard seguenti.

Le costanti seguenti sono definite in winuser. h:



| Costante                                                                                                                                                                                    | Descrizione                                                                                                                                                                                                                                                                                                                                            |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OBJID_ALERT"></span><span id="objid_alert"></span><dl> <dt>**\_avviso ObjID**</dt> </dl>                                     | Avviso associato a una finestra o a un'applicazione. Le finestre di messaggio fornite dal sistema sono gli unici elementi dell'interfaccia utente che inviano eventi con questo identificatore di oggetto. Le applicazioni server non possono utilizzare le funzioni **AccessibleObjectFrom**_X_ con questo identificatore di oggetto. Si tratta di un problema noto con Microsoft Active Accessibility.<br/>          |
| <span id="OBJID_CARET"></span><span id="objid_caret"></span><dl> <dt>**punto di \_ inserimento ObjID**</dt> </dl>                                     | Barra di inserimento del testo (cursore) nella finestra.<br/>                                                                                                                                                                                                                                                                                               |
| <span id="OBJID_CLIENT"></span><span id="objid_client"></span><dl> <dt>**\_client ObjID**</dt> </dl>                                  | Area client della finestra. Nella maggior parte dei casi, il sistema operativo controlla gli elementi del frame e l'oggetto client contiene tutti gli elementi controllati dall'applicazione. I server elaborano solo i messaggi [**WM \_ GetObject**](wm-getobject.md) in cui *lParam* è il \_ client ObjID, la finestra objid \_ o un identificatore di oggetto personalizzato.<br/> |
| <span id="OBJID_CURSOR"></span><span id="objid_cursor"></span><dl> <dt>**\_cursore ObjID**</dt> </dl>                                  | Puntatore del mouse. Nel sistema è presente un solo puntatore del mouse e non è un elemento figlio di alcuna finestra.<br/>                                                                                                                                                                                                                                      |
| <span id="OBJID_HSCROLL"></span><span id="objid_hscroll"></span><dl> <dt>**\_HSCROLL ObjID**</dt> </dl>                               | Barra di scorrimento orizzontale della finestra.<br/>                                                                                                                                                                                                                                                                                                         |
| <span id="OBJID_NATIVEOM"></span><span id="objid_nativeom"></span><dl> <dt>**\_NATIVEOM ObjID**</dt> </dl>                            | In risposta a questo identificatore di oggetto, le applicazioni di terze parti possono esporre il proprio modello a oggetti. Le applicazioni di terze parti possono restituire qualsiasi interfaccia COM in risposta a questo identificatore di oggetto.<br/>                                                                                                                                             |
| <span id="OBJID_MENU"></span><span id="objid_menu"></span><dl> <dt>**\_menu ObjID**</dt> </dl>                                        | Barra dei menu della finestra.<br/>                                                                                                                                                                                                                                                                                                                      |
| <span id="OBJID_QUERYCLASSNAMEIDX"></span><span id="objid_queryclassnameidx"></span><dl> <dt>**\_QUERYCLASSNAMEIDX ObjID**</dt> </dl> | Identificatore di oggetto che Oleacc.dll utilizza internamente. Per ulteriori informazioni, vedere [Appendice F: valori identificatore oggetto per objid \_ QUERYCLASSNAMEIDX](appendix-f--object-identifier-values-for-objid-queryclassnameidx.md).<br/>                                                                                                                  |
| <span id="OBJID_SIZEGRIP"></span><span id="objid_sizegrip"></span><dl> <dt>**\_SIZEGRIP ObjID**</dt> </dl>                            | Grip delle dimensioni della finestra: un componente del frame facoltativo posizionato nell'angolo inferiore destro della cornice della finestra.<br/>                                                                                                                                                                                                                                  |
| <span id="OBJID_SOUND"></span><span id="objid_sound"></span><dl> <dt>**OBJID \_ suono**</dt> </dl>                                     | Oggetto audio. Gli oggetti audio non hanno posizioni dello schermo o elementi figlio, ma hanno attributi di nome e stato. Sono elementi figlio dell'applicazione che sta suonando il suono.<br/>                                                                                                                                                         |
| <span id="OBJID_SYSMENU"></span><span id="objid_sysmenu"></span><dl> <dt>**\_SYSMENU ObjID**</dt> </dl>                               | Menu di sistema della finestra.<br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="OBJID_TITLEBAR"></span><span id="objid_titlebar"></span><dl> <dt>**barra del titolo OBJID \_**</dt> </dl>                            | Barra del titolo della finestra.<br/>                                                                                                                                                                                                                                                                                                                     |
| <span id="OBJID_VSCROLL"></span><span id="objid_vscroll"></span><dl> <dt>**\_VSCROLL ObjID**</dt> </dl>                               | Barra di scorrimento verticale della finestra.<br/>                                                                                                                                                                                                                                                                                                           |
| <span id="OBJID_WINDOW"></span><span id="objid_window"></span><dl> <dt>**\_finestra ObjID**</dt> </dl>                                  | La finestra stessa anziché un oggetto figlio.<br/>                                                                                                                                                                                                                                                                                               |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



 

 





