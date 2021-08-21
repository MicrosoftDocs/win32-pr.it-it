---
description: Contiene l'oggetto Application della cartella.
ms.assetid: 1dba83eb-1af6-42d9-b2c9-ab7767888efe
title: Proprietà Folder.Application (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.Application
api_type:
- COM
api_location:
- Shldisp.h
ms.openlocfilehash: 41c0c3efd2664e7f3544ee5f58e4e1c530d97ca7ef754030c082103598011a10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117860356"
---
# <a name="folderapplication-property"></a>Folder.Application - proprietà

Contiene l'oggetto Application della cartella.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
Application = Folder.Application
```



## <a name="property-value"></a>Valore proprietà

Riferimento all'oggetto all'oggetto Application.

## <a name="remarks"></a>Commenti

La **proprietà Application** restituisce l'oggetto di automazione supportato dall'applicazione che contiene il controllo WebBrowser, se tale oggetto è accessibile. In caso contrario, questa proprietà restituisce l'oggetto di automazione del controllo WebBrowser.

Usare questa proprietà con i **comandi Set** e **CreateObject** o con il **comando GetObject** per creare e modificare un'istanza del Internet Explorer appliato.

> [!Note]  
> Non tutti i metodi vengono implementati per tutte le cartelle. Ad esempio, il [**metodo ParseName**](folder-parsename.md) non è implementato per la cartella Pannello di controllo (CSIDL \_ CONTROLS). Se si tenta di chiamare un metodo non implementato, viene generato 0x800A01BD errore di tipo decimale 445.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app \[ desktop XP\]<br/>                 |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl> |



 

 




