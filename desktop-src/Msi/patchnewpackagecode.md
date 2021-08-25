---
description: La proprietà PATCHNEWPACKAGECODE aggiorna la proprietà Riepilogo numero revisione di un'immagine amministrativa durante l'applicazione di patch.
ms.assetid: 5ca0058a-b4eb-48df-89eb-fbc7da7224e8
title: PatchNEWPACKAGECODE - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65d7e64729643fa1b6449838496416d10e1ec12374762b3f702b306a146338f5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926164"
---
# <a name="patchnewpackagecode-property"></a>PatchNEWPACKAGECODE - proprietà

La **proprietà PATCHNEWPACKAGECODE** aggiorna la [**proprietà Riepilogo numero**](revision-number-summary.md) revisione di un'immagine amministrativa durante l'applicazione di patch. Questa proprietà viene impostata solo da una trasformazione in un file msp. Il file msp deve includere una trasformazione che aggiunge questa proprietà alla [tabella Property e](property-table.md) ne imposta il valore. Il programma di installazione scrive quindi il valore **di PATCHNEWPACKAGECODE** nella **proprietà Revision Number Summary.**

## <a name="remarks"></a>Commenti

Le **proprietà PATCHNEWPACKAGECODE**, [**PATCHNEWSUMMARYCOMMENTS**](patchnewsummarycomments.md)e [**PATCHNEWSUMMARYSUBJECT**](patchnewsummarysubject.md) vengono usate per aggiornare le informazioni di riepilogo quando viene installata una patch in un'immagine amministrativa.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Vedere i [Windows di installazione Run-Time](windows-installer-portal.md) per informazioni sul Service Pack Windows minimo richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




