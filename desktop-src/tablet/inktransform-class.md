---
description: Rappresenta una matrice 3x3 che, a sua volta, rappresenta una trasformazione affine.
ms.assetid: 79abff2e-d1d3-4a32-9ac2-f46c1b21f742
title: Classe InkTransform (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkTransform
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 61641f0fed8ec98321e155f82ff9a35150e7fdcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319168"
---
# <a name="inktransform-class"></a>Classe InkTransform

Rappresenta una matrice 3x3 che, a sua volta, rappresenta una trasformazione affine.

**InkTransform** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La classe **InkTransform** dispone di questi metodi.



| Metodo                                                  | Descrizione                                                                                                                 |
|:--------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [**GetTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-gettransform)       | Recupera **InkTransform** come 6 float.<br/>                                                                      |
| [**Riflettere**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-reflect)                 | Riflette la trasformazione in direzioni orizzontali o verticali.<br/>                                          |
| [**Reset**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-reset)                     | Reimposta lo stato originale della trasformazione.<br/>                                                                      |
| [**Ruota**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-rotate)                   | Ruota la trasformazione in base a un angolo misurato in gradi e, facoltativamente, specifica un punto centrale per la rotazione.<br/> |
| [**ScaleTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-scaletransform) | Ridimensiona la trasformazione in base ai fattori X e Y.<br/>                                                                         |
| [**SetTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-settransform)       | Modifica **InkTransform** utilizzando 6 float.<br/>                                                                    |
| [**Taglio**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-shear)                     | Applica una cesoia con i fattori orizzontali e verticali specificati.<br/>                                              |
| [**Traduci**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-translate)             | Sposta la trasformazione in base ai componenti orizzontali e verticali specificati.<br/>                                         |



 

### <a name="properties"></a>Proprietà

La classe **InkTransform** dispone di queste proprietà.



| Proprietà                                     | Tipo di accesso           | Descrizione                                                                                          |
|:---------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------|
| [**Data**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_data)<br/> | Lettura/Scrittura<br/> | Ottiene o imposta la versione di automazione dello struct di proprietà di WIN32.<br/>                            |
| [**eDx**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_edx)<br/>   | Lettura/Scrittura<br/> | Ottiene o imposta il numero reale che specifica l'elemento nella terza riga, prima colonna.<br/>   |
| [**eDy**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_edy)<br/>   | Lettura/Scrittura<br/> | Ottiene o imposta il numero reale che specifica l'elemento nella terza riga, seconda colonna.<br/>  |
| [**eM11**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em11)<br/> | Lettura/Scrittura<br/> | Ottiene o imposta il numero reale che specifica l'elemento nella prima riga, prima colonna.<br/>   |
| [**eM12**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em12)<br/> | Lettura/Scrittura<br/> | Ottiene o imposta il numero reale che specifica l'elemento nella prima riga, seconda colonna.<br/>  |
| [**eM21**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em21)<br/> | Lettura/Scrittura<br/> | Ottiene o imposta il numero reale che specifica l'elemento nella seconda riga, prima colonna.<br/>  |
| [**eM22**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em22)<br/> | Lettura/Scrittura<br/> | Ottiene o imposta il numero reale che specifica l'elemento nella seconda riga, seconda colonna.<br/> |



 

## <a name="remarks"></a>Commenti

È possibile creare un'istanza di questo oggetto chiamando il metodo [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) in C++.

L'oggetto archivia solo sei dei nove numeri in una matrice 3x3 perché tutte le matrici 3x3 che rappresentano le trasformazioni affini hanno la stessa terza colonna (0, 0, 1). Questo oggetto a sua volta viene usato per descrivere le operazioni di trasformazione, ad esempio lo scorrimento, il taglio, il ridimensionamento o la rotazione in un oggetto [**InkRenderer**](inkrenderer-class.md) , un oggetto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) o una raccolta [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) .

> [!Note]  
> L'oggetto InkTransform è correlato alla [**struttura di**](/windows/win32/api/wingdi/ns-wingdi-xform)  .

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



 

