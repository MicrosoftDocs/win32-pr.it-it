---
description: Rappresenta un elenco di parole che possono essere usate per migliorare il risultato del riconoscimento.
ms.assetid: d189fd13-ec69-45dc-8be4-fea48f337636
title: Classe InkWordList (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkWordList
- InkWordList.IInkWordList
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: fe46cf8f1befaf2717cfcf0a8e131113ed4552843bd3b6572364c27f3418ab34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119938671"
---
# <a name="inkwordlist-class"></a>Classe InkWordList

Rappresenta un elenco di parole che possono essere usate per migliorare il risultato del riconoscimento.

**InkWordList** ha questi tipi di membri:

-   [Interfacce](#interfaces)
-   [Metodi](#methods)

### <a name="interfaces"></a>Interfacce

La **classe InkWordList** definisce queste interfacce.



| Interfaccia        | Descrizione                                                           |
|:-----------------|:----------------------------------------------------------------------|
| **IInkWordList** | Questo oggetto implementa **l'interfaccia COM IInkWordList.**<br/> |



 

### <a name="methods"></a>Metodi

La **classe InkWordList** ha questi metodi.



| Metodo                                       | Descrizione                                                             |
|:---------------------------------------------|:------------------------------------------------------------------------|
| [**AddWord**](/windows/win32/api/msinkaut/nf-msinkaut-iinkwordlist-addword)       | Aggiunge una singola parola a **InkWordList.**<br/>                   |
| [**Unione**](/windows/win32/api/msinkaut/nf-msinkaut-iinkwordlist-merge)           | Unisce un altro **oggetto InkWordList** a in **questo oggetto InkWordList.**<br/> |
| [**RemoveWord**](/windows/win32/api/msinkaut/nf-msinkaut-iinkwordlist-removeword) | Rimuove una singola parola da **un oggetto InkWordList.**<br/>                |



 

## <a name="remarks"></a>Commenti

È possibile creare un'istanza di questo oggetto chiamando il [**metodo CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) in C++.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist)
</dt> <dt>

[Costanti factoid](factoid-constants.md)
</dt> <dt>

[**Classe InkRecognizerContext**](inkrecognizercontext-class.md)
</dt> </dl>

 

