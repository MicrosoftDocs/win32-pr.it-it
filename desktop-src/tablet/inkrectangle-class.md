---
description: Rappresenta l'accesso a un rettangolo.
ms.assetid: 78e6c29c-0f43-46a5-9d30-948de5f369c8
title: Classe InkRectangle (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkRectangle
- InkRectangle.IInkRectangle
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: d643696fe19523bac93ebca71cf885cd93b8570a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319169"
---
# <a name="inkrectangle-class"></a>Classe InkRectangle

Rappresenta l'accesso a un rettangolo.

**InkRectangle** dispone di questi tipi di membri:

-   [Interfacce](#interfaces)
-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="interfaces"></a>Interfacce

La classe **InkRectangle** definisce queste interfacce.



| Interfaccia         | Descrizione                                                            |
|:------------------|:-----------------------------------------------------------------------|
| **IInkRectangle** | Questo oggetto implementa l'interfaccia com **IInkRectangle** .<br/> |



 

### <a name="methods"></a>Metodi

La classe **InkRectangle** dispone di questi metodi.



| Metodo                                            | Descrizione                                                                        |
|:--------------------------------------------------|:-----------------------------------------------------------------------------------|
| [**GetRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-getrectangle) | Recupera gli elementi dell'oggetto **InkRectangle** in una singola chiamata.<br/> |
| [**Serectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-setrectangle) | Modifica gli elementi dell'oggetto **InkRectangle** in una singola chiamata.<br/>  |



 

### <a name="properties"></a>Proprietà

La classe **InkRectangle** dispone di queste proprietà.



| Proprietà                                         | Tipo di accesso           | Descrizione                                                        |
|:-------------------------------------------------|:----------------------|:-------------------------------------------------------------------|
| [**Ultimo**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_bottom)<br/> | Lettura/Scrittura<br/> | Ottiene o imposta la posizione inferiore del rettangolo.<br/>      |
| [**Data**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_data)<br/>     | Lettura/Scrittura<br/> | Ottiene o imposta l'accesso allo struct rettangolo (solo C++).<br/> |
| [**Sinistra**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_left)<br/>     | Lettura/Scrittura<br/> | Ottiene o imposta la posizione sinistra del rettangolo.<br/>        |
| [**Ok**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_right)<br/>   | Lettura/Scrittura<br/> | Ottiene o imposta la posizione destra del rettangolo.<br/>       |
| [**In alto**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_top)<br/>       | Lettura/Scrittura<br/> | Ottiene o imposta la posizione superiore del rettangolo.<br/>         |



 

## <a name="remarks"></a>Commenti

> [!Note]  
> Un punto si trova all'interno di un **InkRectangle** se si trova sul lato [**sinistro**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_left) o [**superiore**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_top) oppure si trova all'interno di tutti e quattro i lati. Un punto sul lato [**destro**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_right) o [**inferiore**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_bottom) viene considerato all'esterno del rettangolo.

 

È possibile creare un'istanza di questo oggetto chiamando il metodo [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) .

> [!Note]  
> Non è possibile usare **InkRectangle** se è più grande di Long \_ Max (2 ^ 31-1) in una delle due dimensioni.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



 

