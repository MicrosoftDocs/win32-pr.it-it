---
description: Rappresenta una matrice 3x3 che, a sua volta, rappresenta una trasformazione affine.
ms.assetid: 79abff2e-d1d3-4a32-9ac2-f46c1b21f742
title: Classe InkTransform (Msinkaut.h)
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
ms.openlocfilehash: 4bdc93e2c80f1a7ef4a8eacf1a58288c008e1354cda702e492deb2990e8938d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119938661"
---
# <a name="inktransform-class"></a>Classe InkTransform

Rappresenta una matrice 3x3 che, a sua volta, rappresenta una trasformazione affine.

**InkTransform** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe InkTransform** include questi metodi.



| Metodo                                                  | Descrizione                                                                                                                 |
|:--------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [**GetTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-gettransform)       | Recupera **InkTransform** come 6 float.<br/>                                                                      |
| [**Riflettere**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-reflect)                 | Riflette la trasformazione in direzione orizzontale o verticale.<br/>                                          |
| [**Reset**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-reset)                     | Reimposta lo stato originale della trasformazione.<br/>                                                                      |
| [**Ruota**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-rotate)                   | Ruota la trasformazione di un angolo misurato in gradi e, facoltativamente, specifica un punto centrale per la rotazione.<br/> |
| [**ScaleTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-scaletransform) | Ridimensiona la trasformazione in base ai fattori X e Y.<br/>                                                                         |
| [**SetTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-settransform)       | Modifica **InkTransform** usando 6 float.<br/>                                                                    |
| [**Taglio**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-shear)                     | Applica una barra con i fattori orizzontali e verticali specificati.<br/>                                              |
| [**Traduci**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-translate)             | Sposta la trasformazione in base ai componenti orizzontale e verticale specificati.<br/>                                         |



 

### <a name="properties"></a>Proprietà

La **classe InkTransform** ha queste proprietà.



| Proprietà                                     | Tipo di accesso           | Descrizione                                                                                          |
|:---------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------|
| [**Dati**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_data)<br/> | Lettura/Scrittura<br/> | Ottiene o imposta la versione di Automazione dello struct XFORM WIN32.<br/>                            |
| [**Edx**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_edx)<br/>   | Lettura/Scrittura<br/> | Ottiene o imposta il numero reale che specifica l'elemento nella terza riga, la prima colonna.<br/>   |
| [**Edy**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_edy)<br/>   | Lettura/Scrittura<br/> | Ottiene o imposta il numero reale che specifica l'elemento nella terza riga, seconda colonna.<br/>  |
| [**eM11**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em11)<br/> | Lettura/Scrittura<br/> | Ottiene o imposta il numero reale che specifica l'elemento nella prima riga, prima colonna.<br/>   |
| [**eM12**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em12)<br/> | Lettura/Scrittura<br/> | Ottiene o imposta il numero reale che specifica l'elemento nella prima riga, seconda colonna.<br/>  |
| [**eM21**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em21)<br/> | Lettura/Scrittura<br/> | Ottiene o imposta il numero reale che specifica l'elemento nella seconda riga, la prima colonna.<br/>  |
| [**eM22**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em22)<br/> | Lettura/Scrittura<br/> | Ottiene o imposta il numero reale che specifica l'elemento nella seconda riga, seconda colonna.<br/> |



 

## <a name="remarks"></a>Commenti

È possibile creare un'istanza di questo oggetto chiamando il [**metodo CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) in C++.

L'oggetto archivia solo sei dei nove numeri in una matrice 3x3 perché tutte le matrici 3x3 che rappresentano trasformazioni affine hanno la stessa terza colonna (0, 0, 1). Questo oggetto viene a sua volta usato per descrivere operazioni di trasformazione, ad esempio spostamento, traslatura, ridimensionamento o rotazione in un oggetto [**InkRenderer,**](inkrenderer-class.md) [**in un oggetto IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) o in una raccolta [InkStrokes.](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))

> [!Note]  
> **L'oggetto InkTransform** è correlato alla [**struttura XFORM.**](/windows/win32/api/wingdi/ns-wingdi-xform)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



 

