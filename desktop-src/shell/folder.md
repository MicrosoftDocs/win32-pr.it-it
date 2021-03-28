---
description: Rappresenta una cartella della shell. Questo oggetto contiene proprietà e metodi che consentono di recuperare informazioni sulla cartella.
ms.assetid: f1e82c61-205e-47c8-bc7c-6a52410a672e
title: Oggetto Folder (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder
api_type:
- COM
api_location:
- Shldisp.h
ms.openlocfilehash: d37966b13a182161c1a6248c93eabaf5dfa3597c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524490"
---
# <a name="folder-object"></a>Oggetto Folder

Rappresenta una cartella della shell. Questo oggetto contiene proprietà e metodi che consentono di recuperare informazioni sulla cartella.

## <a name="members"></a>Membri

L'oggetto **cartella** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'oggetto **Folder** presenta questi metodi.



| Metodo                                      | Descrizione                                                                                                                |
|:--------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------|
| [**CopyHere**](folder-copyhere.md)         | Copia un elemento o elementi in una cartella.<br/>                                                                            |
| [**GetDetailsOf**](folder-getdetailsof.md) | Recupera i dettagli relativi a un elemento in una cartella. Ad esempio, le dimensioni, il tipo o l'ora dell'Ultima modifica.<br/> |
| [**Elementi**](folder-items.md)               | Recupera un oggetto [**FolderItems**](folderitems.md) che rappresenta la raccolta di elementi nella cartella.<br/>    |
| [**MoveHere**](folder-movehere.md)         | Sposta un elemento o elementi in questa cartella.<br/>                                                                          |
| [**NewFolder**](folder-newfolder.md)       | Crea una nuova cartella.<br/>                                                                                           |
| [**ParseName**](folder-parsename.md)       | Crea e restituisce un oggetto [**FolderItem**](folderitem.md) che rappresenta un elemento specificato.<br/>                 |



 

### <a name="properties"></a>Proprietà

L'oggetto **Folder** dispone di queste proprietà.



| Proprietà                                               | Tipo di accesso          | Descrizione                                          |
|:-------------------------------------------------------|:---------------------|:-----------------------------------------------------|
| [**Applicazione**](folder-application.md)<br/>   | Sola lettura<br/> | Contiene l'oggetto applicazione della cartella.<br/> |
| [**Padre**](folder-parent.md)<br/>             | Sola lettura<br/> | Non implementato.<br/>                          |
| [**ParentFolder**](folder-parentfolder.md)<br/> | Sola lettura<br/> | Contiene l'oggetto **cartella** padre.<br/>    |
| [**Titolo**](folder-title.md)<br/>               | Sola lettura<br/> | Contiene il titolo della cartella.<br/>         |



 

## <a name="remarks"></a>Commenti

> [!Note]  
> Non tutti i metodi sono implementati per tutte le cartelle. Il metodo [**ParseName**](folder-parsename.md) , ad esempio, non è implementato per la cartella del pannello di controllo ( \_ controlli CSIDL). Se si tenta di chiamare un metodo non implementato, viene generato un errore 0x800A01BD (decimale 445).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>                 |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl> |



 

 




