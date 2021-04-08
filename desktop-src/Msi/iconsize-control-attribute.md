---
description: Un file di icona può avere diverse dimensioni della stessa immagine dell'icona.
ms.assetid: 2d4d3689-a45a-4088-b466-e2b3bf4c8fb5
title: Attributo di controllo IconSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cb615a53c589ebc2ad2cafb8a2ff7dec902865e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049901"
---
# <a name="iconsize-control-attribute"></a>Attributo di controllo IconSize

Un file di icona può avere diverse dimensioni della stessa immagine dell'icona. Questi bit specificano le dimensioni dell'immagine dell'icona da caricare. Se non è impostato alcun bit, viene caricata la prima immagine. Se viene impostato solo **msidbControlAttributesIconSize16** , viene caricata la prima immagine di 16x16. Se è impostato solo **msidbControlAttributesIconSize32** , viene caricata la prima immagine di 32x32. Se è impostato **msidbControlAttributesIconSize48** , viene caricata la prima immagine di 48x48.

## <a name="valid-controls"></a>Controlli validi

[CheckBox](checkbox-control.md)

[Icona](icon-control.md)

[Pulsante](pushbutton-control.md)

[RadioButtonGroup](radiobuttongroup-control.md)

## <a name="value"></a>Valore



| Decimal | Valore esadecimale | Descrizione                          |
|---------|-------------|--------------------------------------|
| 2097152 | 0x00200000  | **msidbControlAttributesIconSize16** |
| 4194304 | 0x00400000  | **msidbControlAttributesIconSize32** |
| 6291456 | 0x00600000  | **msidbControlAttributesIconSize48** |



 

## <a name="remarks"></a>Commenti

Per impostare questo attributo su un controllo, includere i bit IconSize nella colonna Attributes del record del controllo nella tabella del [controllo](control-table.md).

Se il bit [FixedSize](fixedsize-control-attribute.md) non è impostato, l'immagine caricata viene compattata o estesa per adattarsi al controllo icona. Se il bit [FixedSize](fixedsize-control-attribute.md) è impostato e l'immagine caricata è inferiore al controllo Icon, l'immagine viene visualizzata al centro all'interno del controllo. Se il bit [FixedSize](fixedsize-control-attribute.md) è impostato e l'immagine caricata è più grande del controllo Icon, l'immagine viene ridotta per adattarsi al controllo.

Vedere [gli attributi del controllo](control-attributes.md) e il controllo che è necessario creare sotto i [controlli](controls.md).

 

 



