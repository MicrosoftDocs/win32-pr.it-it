---
description: Rappresenta una cartella shell. Questo oggetto contiene proprietà e metodi che consentono di recuperare informazioni sulla cartella.
ms.assetid: f1e82c61-205e-47c8-bc7c-6a52410a672e
title: Oggetto Folder (Shldisp.h)
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
ms.openlocfilehash: baf180149419178b489f3ba00042c561268b36e7b7ed7b0e2afab54b68f78466
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032619"
---
# <a name="folder-object"></a>Oggetto Folder

Rappresenta una cartella shell. Questo oggetto contiene proprietà e metodi che consentono di recuperare informazioni sulla cartella.

## <a name="members"></a>Membri

**L'oggetto Folder** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'oggetto Folder** dispone di questi metodi.



| Metodo                                      | Descrizione                                                                                                                |
|:--------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------|
| [**CopyHere**](folder-copyhere.md)         | Copia uno o più elementi in una cartella.<br/>                                                                            |
| [**GetDetailsOf**](folder-getdetailsof.md) | Recupera i dettagli relativi a un elemento in una cartella. Ad esempio, la dimensione, il tipo o l'ora dell'ultima modifica.<br/> |
| [**Elementi**](folder-items.md)               | Recupera un [**oggetto FolderItems**](folderitems.md) che rappresenta la raccolta di elementi nella cartella.<br/>    |
| [**MoveHere**](folder-movehere.md)         | Sposta uno o più elementi in questa cartella.<br/>                                                                          |
| [**NewFolder**](folder-newfolder.md)       | Crea una nuova cartella.<br/>                                                                                           |
| [**ParseName**](folder-parsename.md)       | Crea e restituisce un [**oggetto FolderItem**](folderitem.md) che rappresenta un elemento specificato.<br/>                 |



 

### <a name="properties"></a>Proprietà

**L'oggetto Folder** ha queste proprietà.



| Proprietà                                               | Tipo di accesso          | Descrizione                                          |
|:-------------------------------------------------------|:---------------------|:-----------------------------------------------------|
| [**Applicazione**](folder-application.md)<br/>   | Sola lettura<br/> | Contiene l'oggetto Application della cartella.<br/> |
| [**Padre**](folder-parent.md)<br/>             | Sola lettura<br/> | Non implementato.<br/>                          |
| [**Cartella padre**](folder-parentfolder.md)<br/> | Sola lettura<br/> | Contiene **l'oggetto Folder** padre.<br/>    |
| [**Titolo**](folder-title.md)<br/>               | Sola lettura<br/> | Contiene il titolo della cartella.<br/>         |



 

## <a name="remarks"></a>Commenti

> [!Note]  
> Non tutti i metodi vengono implementati per tutte le cartelle. Ad esempio, il [**metodo ParseName**](folder-parsename.md) non è implementato per la cartella Pannello di controllo (CSIDL \_ CONTROLS). Se si tenta di chiamare un metodo non implementato, viene generato 0x800A01BD errore di tipo decimale 445.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app desktop XP \[\]<br/>                 |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl> |



 

 




