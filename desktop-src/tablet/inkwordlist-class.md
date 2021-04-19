---
description: Rappresenta un elenco di parole che è possibile utilizzare per migliorare il risultato del riconoscimento.
ms.assetid: d189fd13-ec69-45dc-8be4-fea48f337636
title: Classe InkWord (Msinkaut. h)
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
ms.openlocfilehash: 7f3bbf077758bfd0449f5bca1ba3739342fa3658
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317931"
---
# <a name="inkwordlist-class"></a>Classe InkWord

Rappresenta un elenco di parole che è possibile utilizzare per migliorare il risultato del riconoscimento.

L' **InkWord** è costituito da questi tipi di membri:

-   [Interfacce](#interfaces)
-   [Metodi](#methods)

### <a name="interfaces"></a>Interfacce

La classe **InkWord** definisce queste interfacce.



| Interfaccia        | Descrizione                                                           |
|:-----------------|:----------------------------------------------------------------------|
| **IInkWordList** | Questo oggetto implementa l'interfaccia com **IInkWordList** .<br/> |



 

### <a name="methods"></a>Metodi

La classe **InkWord** ha questi metodi.



| Metodo                                       | Descrizione                                                             |
|:---------------------------------------------|:------------------------------------------------------------------------|
| [**AddWord**](/windows/win32/api/msinkaut/nf-msinkaut-iinkwordlist-addword)       | Aggiunge una singola parola all'oggetto **InkWord**.<br/>                   |
| [**Unione**](/windows/win32/api/msinkaut/nf-msinkaut-iinkwordlist-merge)           | Unisce un altro **InkWord** a in questo **InkWord**.<br/> |
| [**RemoveWord**](/windows/win32/api/msinkaut/nf-msinkaut-iinkwordlist-removeword) | Rimuove una singola parola da un oggetto **InkWord**.<br/>                |



 

## <a name="remarks"></a>Commenti

È possibile creare un'istanza di questo oggetto chiamando il metodo [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) in C++.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist)
</dt> <dt>

[Costanti controllo oggetto](factoid-constants.md)
</dt> <dt>

[**Classe InkRecognizerContext**](inkrecognizercontext-class.md)
</dt> </dl>

 

