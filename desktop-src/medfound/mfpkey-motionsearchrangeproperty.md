---
description: Specifica l'intervallo usato nelle ricerche di movimento.
ms.assetid: b2026f47-ac39-4276-8359-c939b202f00c
title: Proprietà MFPKEY_MOTIONSEARCHRANGE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c557ea1a462192434222e425dccb8b9a0e291986
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227003"
---
# <a name="mfpkey_motionsearchrange-property"></a>\_Proprietà MOTIONSEARCHRANGE di MFPKEY

Specifica l'intervallo usato nelle ricerche di movimento.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCMotionSearchRange

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

0

## <a name="remarks"></a>Commenti

Questa proprietà può essere impostata su uno dei valori seguenti. H indica l'intervallo orizzontale e V indica l'intervallo verticale. Tutti gli intervalli sono specificati in pixel.



| Valore | Range                                |
|-------|--------------------------------------|
| 0     | + 63.75/-64,0 H, + 31.75/-32.0 V       |
| 1     | +127,75/-128,0 H, +63,75/-64,0 V     |
| 2     | + 511.75/-512.0 H, + 127.75/-128.0 V   |
| 3     | + 1023.75/-1024.0 H, + 255.75/-256.0 V |
| -1    | Macroblocco-Adaptive (automatico)      |



 

Questa proprietà controlla le dimensioni dell'area del frame in cui il codec eseguirà la ricerca di un elemento che potrebbe aver esposto il movimento tra frame. Una finestra di ricerca più ampia consente di trovare un movimento più veloce, ma richiederà più tempo della CPU. I requisiti della CPU sono approssimativamente doppi a ogni livello.

La modalità automatica (-1) consente di selezionare in modo dinamico la modalità più efficiente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




