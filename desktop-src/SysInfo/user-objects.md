---
description: Gli oggetti dell'interfaccia utente supportano un solo handle per oggetto. I processi non possono ereditare o duplicare gli handle per gli oggetti utente. I processi in una sessione non possono fare riferimento a un handle utente in un'altra sessione.
ms.assetid: 07edc049-26d9-4f42-a5e7-e1f4c8435a6c
title: Oggetti utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5ed8afcf0f1d0e4c232cf503bc2c7ba86dca42d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104564311"
---
# <a name="user-objects"></a>Oggetti utente

Gli oggetti dell'interfaccia utente supportano un solo handle per oggetto. I processi non possono ereditare o duplicare gli handle per gli oggetti utente. I processi in una sessione non possono fare riferimento a un handle utente in un'altra sessione.

È previsto un limite teorico di 65.536 handle utente per sessione. Tuttavia, il numero massimo di handle utente che è possibile aprire per sessione è in genere inferiore, in quanto è interessato dalla memoria disponibile. È anche previsto un limite predefinito per ogni processo degli handle utente. Per modificare questo limite, impostare il valore del registro di sistema seguente:

**HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Windows** \\ **USERProcessHandleQuota**

Questo valore può essere impostato su un numero compreso tra 200 e 18.000.

## <a name="handles-to-user-objects"></a>Handle per gli oggetti utente

Gli handle per gli oggetti utente sono pubblici per tutti i processi. Ovvero, qualsiasi processo può utilizzare l'handle dell'oggetto utente, purché il processo disponga dell'accesso di sicurezza all'oggetto.

Nell'illustrazione seguente, un'applicazione crea un oggetto finestra. La funzione [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) crea l'oggetto finestra e restituisce un handle dell'oggetto.

![applicazione creazione di un oggetto finestra](images/cshob-01.png)

Una volta creato l'oggetto finestra, l'applicazione può utilizzare l'handle della finestra per visualizzare o modificare la finestra. L'handle rimane valido fino a quando l'oggetto finestra non viene eliminato definitivamente.

Nella figura seguente l'applicazione elimina definitivamente l'oggetto finestra. La funzione [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) rimuove l'oggetto finestra dalla memoria, che invalida l'handle della finestra.

![eliminazione definitiva di un oggetto finestra](images/cshob-02.png)

## <a name="managing-user-objects"></a>Gestione degli oggetti utente

La tabella seguente elenca gli oggetti utente, insieme alle funzioni di autore e distruttore di ogni oggetto. Le funzioni Creator creano l'oggetto e un handle di oggetto o semplicemente restituiscono l'handle di oggetto esistente. Le funzioni di distruttore rimuovono l'oggetto dalla memoria, che invalida l'handle dell'oggetto.



| Oggetto utente       | Funzione Creator                                                                                                                                                                                                                                                              | Funzione Destroyer                                                                                   |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| Tabella dei tasti di scelta rapida | [**CreateAcceleratorTable**](/windows/win32/api/winuser/nf-winuser-createacceleratortablea)                                                                                                                                                                                                               | [**DestroyAcceleratorTable**](/windows/win32/api/winuser/nf-winuser-destroyacceleratortable)                                    |
| Cursore             | [**CreateCaret**](/windows/win32/api/winuser/nf-winuser-createcaret)                                                                                                                                                                                                                                     | [**DestroyCaret**](/windows/win32/api/winuser/nf-winuser-destroycaret)                                                          |
| Cursore            | [**CreateCursor**](/windows/win32/api/winuser/nf-winuser-createcursor), [**LoadCursor**](/windows/win32/api/winuser/nf-winuser-loadcursora), [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea)                                                                                                                                                   | [**DestroyCursor**](/windows/win32/api/winuser/nf-winuser-destroycursor)                                                        |
| Conversazione DDE  | [**DdeConnect**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect), [ **DdeConnectList**](/windows/win32/api/ddeml/nf-ddeml-ddeconnectlist)                                                                                                                                                                                      | [**DdeDisconnect**](/windows/win32/api/ddeml/nf-ddeml-ddedisconnect), [ **DdeDisconnectList**](/windows/win32/api/ddeml/nf-ddeml-ddedisconnectlist) |
| Gancio              | [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa)                                                                                                                                                                                                                           | [**UnhookWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-unhookwindowshookex)                                            |
| Icona              | [**CreateIconIndirect**](/windows/win32/api/winuser/nf-winuser-createiconindirect), [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona), [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea)                                                                                                                                           | [**DestroyIcon**](/windows/win32/api/winuser/nf-winuser-destroyicon)                                                            |
| Menu              | [**CreateMenu**](/windows/win32/api/winuser/nf-winuser-createmenu), [**CreatePopupMenu**](/windows/win32/api/winuser/nf-winuser-createpopupmenu), [**LoadMenu**](/windows/win32/api/winuser/nf-winuser-loadmenua), [**LoadMenuIndirect**](/windows/win32/api/winuser/nf-winuser-loadmenuindirecta)                                                                                          | [**DestroyMenu**](/windows/win32/api/winuser/nf-winuser-destroymenu)                                                            |
| Finestra            | [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa), [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa), [**CreateDialogParam**](/windows/win32/api/winuser/nf-winuser-createdialogparama), [**CreateDialogIndirectParam**](/windows/win32/api/winuser/nf-winuser-createdialogindirectparama), [**CreateMDIWindow**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa) | [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow)                                                        |
| Posizione della finestra   | [**BeginDeferWindowPos**](/windows/win32/api/winuser/nf-winuser-begindeferwindowpos)                                                                                                                                                                                                                     | [**EndDeferWindowPos**](/windows/win32/api/winuser/nf-winuser-enddeferwindowpos)                                                |



 

 

 
