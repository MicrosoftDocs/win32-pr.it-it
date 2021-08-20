---
description: Inoltra gli eventi generati da un oggetto ShellFolderView specificato ai gestori eventi ShellFolderViewOC corrispondenti.
title: Oggetto ShellFolderViewOC (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderViewOC
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b50f549c-a79d-4411-a18e-a181b4b924e3
ms.openlocfilehash: bc00dc285c1bcca72e998ecb22f75af56dd085542d0f191c484c096e5e511cce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857673"
---
# <a name="shellfolderviewoc-object"></a>Oggetto ShellFolderViewOC

Inoltra gli eventi generati da un oggetto [**ShellFolderView**](shellfolderview.md) specificato ai gestori **eventi ShellFolderViewOC** corrispondenti.

## <a name="members"></a>Membri

**L'oggetto ShellFolderViewOC** ha questi tipi di membri:

-   [Eventi](#events)
-   [Metodi](#methods)

### <a name="events"></a>Eventi

**L'oggetto ShellFolderViewOC** include questi eventi.



| Event                                                          | Descrizione                                                                                                                     |
|:---------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [**EnumDone**](shellfolderviewoc-enumdone.md)                 | Indica che [**l'oggetto ShellFolderView**](shellfolderview.md) ha terminato l'enumerazione del contenuto della cartella.<br/> |
| [**SelectionChanged**](shellfolderviewoc-selectionchanged.md) | Indica che lo stato di selezione di uno o più elementi nella visualizzazione è stato modificato.<br/>                                     |



 

### <a name="methods"></a>Metodi

**L'oggetto ShellFolderViewOC** dispone di questi metodi.



| Metodo                                                   | Descrizione                                                                                                                                                 |
|:---------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SetFolderView**](shellfolderviewoc-setfolderview.md) | Inoltra gli eventi dell'oggetto [**ShellFolderView**](shellfolderview.md) specificato al gestore eventi **ShellFolderViewOC** corrispondente.<br/> |



 

## <a name="remarks"></a>Commenti

[**L'oggetto ShellFolderView**](shellfolderview.md) genera due eventi, [**EnumDone**](shellfolderviewoc-enumdone.md) e [**SelectionChanged,**](shellfolderviewoc-selectionchanged.md)che vengono in genere gestiti dalle applicazioni. Tuttavia, alcune applicazioni devono gestire gli eventi da una serie di **oggetti ShellFolderView.** Ad esempio, un'applicazione potrebbe ospitare un controllo WebBrowser che consente agli utenti di spostarsi tra una serie di cartelle. Ogni cartella ha un proprio **oggetto ShellFolderView** con gli eventi associati. La gestione di questi eventi può essere difficile.

**L'oggetto ShellFolderViewOC** semplifica la gestione degli eventi per tali scenari. Consente alle applicazioni di gestire gli eventi per tutti [**gli oggetti ShellFolderView**](shellfolderview.md) con una singola coppia di gestori eventi **ShellFolderViewOC.** Ogni volta che l'utente passa a una nuova cartella, l'applicazione passa l'oggetto **ShellFolderView** associato all'oggetto **ShellFolderViewOC** chiamando [**SetFolderView**](shellfolderviewoc-setfolderview.md). Quindi, quando viene generato un evento [**EnumDone**](shellfolderviewoc-enumdone.md) o [**SelectionChanged,**](shellfolderviewoc-selectionchanged.md) l'oggetto **ShellFolderViewOC** inoltra l'evento al proprio gestore per l'elaborazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app desktop XP \[\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5.0 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ShellFolderView**](shellfolderview.md)
</dt> </dl>

 

 




