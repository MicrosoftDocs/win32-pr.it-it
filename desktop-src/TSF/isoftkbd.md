---
title: Interfaccia ISoftKbd (Softkbdc. h)
description: L'interfaccia ISoftKbd viene utilizzata dalle applicazioni e dai servizi di testo per implementare una tastiera soft.
ms.assetid: 804634bd-646e-459f-9fbb-cd6929b11fab
keywords:
- Framework servizi di testo interfaccia ISoftKbd
- Framework dei servizi di testo dell'interfaccia ISoftKbd, descritto
topic_type:
- apiref
api_name:
- ISoftKbd
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e046964616fc564aa2e0c3d0098ee2186cdaf8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300947"
---
# <a name="isoftkbd-interface"></a>Interfaccia ISoftKbd

L'interfaccia **ISoftKbd** viene utilizzata dalle applicazioni e dai servizi di testo per implementare una tastiera soft.

## <a name="members"></a>Membri

L'interfaccia **ISoftKbd** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ISoftKbd** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ISoftKbd** dispone di questi metodi.



| Metodo                                                                                        | Descrizione                                                                                                   |
|:----------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [**AdviseSoftKeyboardEventSink**](isoftkbd-advisesoftkeyboardeventsink.md)                   | Installa un sink di evento della tastiera soft per gestire le notifiche OnKeySelection dalla tastiera soft.<br/> |
| [**CreateSoftKeyboardLayoutFromResource**](isoftkbd-createsoftkeyboardlayoutfromresource.md) | Crea un layout di tastiera soft dalla risorsa specificata.<br/>                                        |
| [**CreateSoftKeyboardLayoutFromXMLFile**](isoftkbd-createsoftkeyboardlayoutfromxmlfile.md)   | Crea un layout di tastiera soft dal file XML specificato.<br/>                                        |
| [**CreateSoftKeyboardWindow**](isoftkbd-createsoftkeyboardwindow.md)                         | Crea una finestra della tastiera soft.<br/>                                                                    |
| [**DestroySoftKeyboardWindow**](isoftkbd-destroysoftkeyboardwindow.md)                       | Elimina una finestra della tastiera soft.<br/>                                                                   |
| [**EnumSoftKeyboard**](isoftkbd-enumsoftkeyboard.md)                                         | Enumera le possibili tastiere flessibili che supportano la lingua specificata.<br/>                        |
| [**GetSoftKeyboardColors**](isoftkbd-getsoftkeyboardcolors.md)                               | Recupera il colore della tastiera flessibile corrispondente al tipo di colore fornito.<br/>                        |
| [**GetSoftKeyboardPosSize**](isoftkbd-getsoftkeyboardpossize.md)                             | Recupera la posizione iniziale e le dimensioni di una tastiera soft.<br/>                                       |
| [**GetSoftKeyboardTextFont**](isoftkbd-getsoftkeyboardtextfont.md)                           | Recupera il tipo di carattere del testo utilizzato da una tastiera soft.<br/>                                                   |
| [**GetSoftKeyboardTypeMode**](isoftkbd-getsoftkeyboardtypemode.md)                           | Recupera la modalità del tipo per una tastiera soft.<br/>                                                       |
| [**Inizializzare**](isoftkbd-initialize.md)                                                     | Inizializza tutti i campi necessari per una tastiera morbida e genera layout di tastiera soft standard.<br/> |
| [**SelectSoftKeyboard**](isoftkbd-selectsoftkeyboard.md)                                     | Seleziona la tastiera soft specificata.<br/>                                                               |
| [**SetKeyboardLabelText**](isoftkbd-setkeyboardlabeltext.md)                                 | Imposta il testo dell'etichetta dal layout per una tastiera soft.<br/>                                           |
| [**SetKeyboardLabelTextCombination**](isoftkbd-setkeyboardlabeltextcombination.md)           | Imposta una combinazione di etichetta e testo utilizzati per descrivere una tastiera soft.<br/>                             |
| [**SetSoftKeyboardColors**](isoftkbd-setsoftkeyboardcolors.md)                               | Imposta il colore della tastiera flessibile corrispondente al tipo di colore fornito.<br/>                             |
| [**SetSoftKeyboardPosSize**](isoftkbd-setsoftkeyboardpossize.md)                             | Imposta la posizione iniziale e la dimensione di una tastiera soft.<br/>                                            |
| [**SetSoftKeyboardTextFont**](isoftkbd-setsoftkeyboardtextfont.md)                           | Imposta il tipo di carattere del testo utilizzato da una tastiera soft.<br/>                                                        |
| [**SetSoftKeyboardTypeMode**](isoftkbd-setsoftkeyboardtypemode.md)                           | Imposta la modalità del tipo per una tastiera soft.<br/>                                                            |
| [**ShowKeysForKeyScanMode**](isoftkbd-showkeysforkeyscanmode.md)                             | Visualizza le chiavi usate per la modalità di analisi della chiave per una tastiera soft.<br/>                                  |
| [**ShowSoftKeyboard**](isoftkbd-showsoftkeyboard.md)                                         | Visualizza una tastiera soft.<br/>                                                                          |
| [**UnadviseSoftKeyboardEventSink**](isoftkbd-unadvisesoftkeyboardeventsink.md)               | Rimuove un sink di evento della tastiera flessibile.<br/>                                                                |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Componente ridistribuibile<br/>          | TSF 1,0 su Windows 2000 Professional<br/>                                        |
| Intestazione<br/>                   | <dl> <dt>Softkbdc. h</dt> </dl>  |
| IDL<br/>                      | <dl> <dt>Softkbd. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



 

