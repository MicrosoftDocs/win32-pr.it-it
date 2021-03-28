---
description: Contiene l'oggetto applicazione della cartella.
ms.assetid: 1dba83eb-1af6-42d9-b2c9-ab7767888efe
title: Proprietà Folder. Application (shldisp. h)
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
ms.openlocfilehash: 13a6a90dd324498c332f7bf580ff5ec987a0c5b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484037"
---
# <a name="folderapplication-property"></a>Proprietà Folder. Application

Contiene l'oggetto applicazione della cartella.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
Application = Folder.Application
```



## <a name="property-value"></a>Valore proprietà

Riferimento all'oggetto applicazione.

## <a name="remarks"></a>Commenti

La proprietà dell' **applicazione** restituisce l'oggetto di automazione supportato dall'applicazione che contiene il controllo WebBrowser, se tale oggetto è accessibile. In caso contrario, questa proprietà restituisce l'oggetto di automazione del controllo WebBrowser.

Utilizzare questa proprietà con i comandi **set** e **CreateObject** oppure con il comando **GetObject** per creare e modificare un'istanza dell'applicazione Internet Explorer.

> [!Note]  
> Non tutti i metodi sono implementati per tutte le cartelle. Il metodo [**ParseName**](folder-parsename.md) , ad esempio, non è implementato per la cartella del pannello di controllo ( \_ controlli CSIDL). Se si tenta di chiamare un metodo non implementato, viene generato un errore 0x800A01BD (decimale 445).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>                 |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl> |



 

 




