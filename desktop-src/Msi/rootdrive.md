---
description: La proprietà ROOTDRIVE Specifica l'unità predefinita per la directory di destinazione dell'installazione.
ms.assetid: 9f36dc2a-2fb5-4787-a630-c7cc93ef51ec
title: Proprietà ROOTDRIVE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e16f64b50105727d307867b5ed2910aed042cd28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326369"
---
# <a name="rootdrive-property"></a>Proprietà ROOTDRIVE

La proprietà **ROOTDRIVE** specifica l'unità predefinita per la directory di destinazione dell'installazione. Se nella colonna directory della [tabella directory](directory-table.md) è indicata la directory di destinazione radice in base a un nome di proprietà non definito, il programma di installazione utilizzerà il valore della proprietà **ROOTDRIVE** per risolvere il percorso della directory di destinazione.

Se **ROOTDRIVE** non è impostato a una riga di comando o creato nella [tabella delle proprietà](property-table.md), il programma di installazione imposta questa proprietà. Durante un' [installazione amministrativa](administrative-installation.md) , il programma di installazione imposta **ROOTDRIVE** sulla prima unità di rete connessa che trova in cui è possibile scrivere. Se non si tratta di un'installazione amministrativa o se il programma di installazione non è in grado di trovare unità di rete, il programma di installazione imposta **ROOTDRIVE** sull'unità locale che può essere scritta per avere maggiore spazio libero.

Il valore di questa proprietà deve terminare con ' \\ '.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




