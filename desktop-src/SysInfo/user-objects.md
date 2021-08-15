---
description: Gli oggetti dell'interfaccia utente supportano un solo handle per oggetto. I processi non possono ereditare o duplicare gli handle per gli oggetti utente. I processi in una sessione non possono fare riferimento a un handle utente in un'altra sessione.
ms.assetid: 07edc049-26d9-4f42-a5e7-e1f4c8435a6c
title: Oggetti utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 368c3cdb5c0927a5773bad818064442f654159fefba2b2dfa4d0cb4c08d17ff8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118884328"
---
# <a name="user-objects"></a>Oggetti utente

Gli oggetti dell'interfaccia utente supportano un solo handle per oggetto. I processi non possono ereditare o duplicare gli handle per gli oggetti utente. I processi in una sessione non possono fare riferimento a un handle utente in un'altra sessione.

Esiste un limite teorico di 65.536 handle utente per sessione. Tuttavia, il numero massimo di handle utente che possono essere aperti per sessione è in genere inferiore, poiché è interessato dalla memoria disponibile. Esiste anche un limite predefinito per processo di handle utente. Per modificare questo limite, impostare il valore del Registro di sistema seguente:

**HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Windows** \\ **USERProcessHandleQuota**

Questo valore può essere impostato su un numero compreso tra 200 e 18.000.

## <a name="handles-to-user-objects"></a>Handle per oggetti utente

Gli handle per gli oggetti utente sono pubblici per tutti i processi. In altre informazioni, qualsiasi processo può usare l'handle dell'oggetto utente, a condizione che il processo abbia accesso di sicurezza all'oggetto.

Nella figura seguente un'applicazione crea un oggetto finestra. La [**funzione CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) crea l'oggetto finestra e restituisce un handle di oggetto.

![applicazione che crea un oggetto finestra](images/cshob-01.png)

Dopo aver creato l'oggetto finestra, l'applicazione può usare l'handle di finestra per visualizzare o modificare la finestra. L'handle rimane valido fino a quando l'oggetto finestra non viene eliminato.

Nella figura successiva l'applicazione elimina l'oggetto finestra. La [**funzione DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) rimuove l'oggetto finestra dalla memoria, che invalida l'handle della finestra.

![eliminazione di un oggetto finestra](images/cshob-02.png)

## <a name="managing-user-objects"></a>Gestione degli oggetti utente

Nella tabella seguente sono elencati gli oggetti utente, insieme alle funzioni creator e destroyer di ogni oggetto. Le funzioni creator creano l'oggetto e un handle di oggetto o semplicemente restituiscono l'handle di oggetto esistente. Le funzioni destroyer rimuovono l'oggetto dalla memoria, che invalida l'handle dell'oggetto.



| Oggetto utente       | Funzione Creator                                                                                                                                                                                                                                                              | Funzione Destroyer                                                                                   |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| Tabella dei tasti di scelta rapida | [**CreateAcceleratorTable**](/windows/win32/api/winuser/nf-winuser-createacceleratortablea)                                                                                                                                                                                                               | [**DestroyAcceleratorTable**](/windows/win32/api/winuser/nf-winuser-destroyacceleratortable)                                    |
| Cursore             | [**CreateCaret**](/windows/win32/api/winuser/nf-winuser-createcaret)                                                                                                                                                                                                                                     | [**DestroyCaret**](/windows/win32/api/winuser/nf-winuser-destroycaret)                                                          |
| Cursore            | [**CreateCursor**](/windows/win32/api/winuser/nf-winuser-createcursor), [**LoadCursor**](/windows/win32/api/winuser/nf-winuser-loadcursora), [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea)                                                                                                                                                   | [**DestroyCursor**](/windows/win32/api/winuser/nf-winuser-destroycursor)                                                        |
| Conversazione DDE  | [**DdeConnect**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect), [ **DdeConnectList**](/windows/win32/api/ddeml/nf-ddeml-ddeconnectlist)                                                                                                                                                                                      | [**DdeDisconnect**](/windows/win32/api/ddeml/nf-ddeml-ddedisconnect), [ **DdeDisconnectList**](/windows/win32/api/ddeml/nf-ddeml-ddedisconnectlist) |
| Gancio              | [**Setwindowshookex**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa)                                                                                                                                                                                                                           | [**UnhookWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-unhookwindowshookex)                                            |
| Icona              | [**CreateIconIndirect**](/windows/win32/api/winuser/nf-winuser-createiconindirect), [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona), [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea)                                                                                                                                           | [**DestroyIcon**](/windows/win32/api/winuser/nf-winuser-destroyicon)                                                            |
| Menu              | [**CreateMenu**](/windows/win32/api/winuser/nf-winuser-createmenu), [**CreatePopupMenu**](/windows/win32/api/winuser/nf-winuser-createpopupmenu), [**LoadMenu**](/windows/win32/api/winuser/nf-winuser-loadmenua), [**LoadMenuIndirect**](/windows/win32/api/winuser/nf-winuser-loadmenuindirecta)                                                                                          | [**DestroyMenu**](/windows/win32/api/winuser/nf-winuser-destroymenu)                                                            |
| Finestra            | [**CreateWindow,**](/windows/win32/api/winuser/nf-winuser-createwindowa) [**CreateWindowEx,**](/windows/win32/api/winuser/nf-winuser-createwindowexa) [**CreateDialogParam,**](/windows/win32/api/winuser/nf-winuser-createdialogparama) [**CreateDialogIndirectParam,**](/windows/win32/api/winuser/nf-winuser-createdialogindirectparama) [**CreateMDIWindow**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa) | [**Destroywindow**](/windows/win32/api/winuser/nf-winuser-destroywindow)                                                        |
| Posizione della finestra   | [**BeginDeferWindowPos**](/windows/win32/api/winuser/nf-winuser-begindeferwindowpos)                                                                                                                                                                                                                     | [**EndDeferWindowPos**](/windows/win32/api/winuser/nf-winuser-enddeferwindowpos)                                                |



 

 

 
