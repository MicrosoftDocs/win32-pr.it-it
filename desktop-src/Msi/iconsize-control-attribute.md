---
description: Un file di icona può contenere diverse dimensioni della stessa immagine di icona.
ms.assetid: 2d4d3689-a45a-4088-b466-e2b3bf4c8fb5
title: Attributo del controllo IconSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f7323d9c3d8dc9bef1bfd4cd275a20dfcadaa3be946bc78fd358a2d6484db53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894201"
---
# <a name="iconsize-control-attribute"></a>Attributo del controllo IconSize

Un file di icona può contenere diverse dimensioni della stessa immagine di icona. Questi bit specificano le dimensioni dell'immagine dell'icona da caricare. Se nessuno dei bit è impostato, viene caricata la prima immagine. Se è **impostato solo msidbControlAttributesIconSize16,** viene caricata la prima immagine 16x16. Se è impostato **solo msidbControlAttributesIconSize32,** viene caricata la prima immagine 32x32. Se **msidbControlAttributesIconSize48** è impostato, viene caricata la prima immagine 48x48.

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

Per impostare questo attributo in un controllo , includere i bit IconSize nella colonna Attributes del record del controllo nella [tabella Control](control-table.md).

Se il bit [FixedSize](fixedsize-control-attribute.md) non è impostato, l'immagine caricata viene ridotta o adattata al controllo icona. Se il bit [FixedSize](fixedsize-control-attribute.md) è impostato e l'immagine caricata è più piccola del controllo icona, l'immagine viene visualizzata al centro all'interno del controllo. Se il bit [FixedSize](fixedsize-control-attribute.md) è impostato e l'immagine caricata è più grande del controllo icona, l'immagine viene ridotta per adattarsi al controllo.

Vedere [Attributi di](control-attributes.md) controllo e il controllo che è necessario creare in [Controlli](controls.md).

 

 



