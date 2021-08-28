---
description: La proprietà PATCHNEWSUMMARYCOMMENTS aggiorna la proprietà Riepilogo commenti di un'installazione amministrativa durante l'applicazione di patch.
ms.assetid: 555813d8-6cb2-4b93-aa01-32d30b75b3d5
title: PatchNEWSUMMARYCOMMENTS - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eef7a67b960b41e55caf5251a33ac6d3198147b92bcab895a2ca711af330acd9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074781"
---
# <a name="patchnewsummarycomments-property"></a>PatchNEWSUMMARYCOMMENTS - proprietà

La **proprietà PATCHNEWSUMMARYCOMMENTS** aggiorna la proprietà [**Riepilogo**](comments-summary.md) commenti di un'installazione amministrativa durante l'applicazione di patch. Questa proprietà viene impostata solo da una trasformazione in un file msp. Il file msp deve includere una trasformazione che aggiunge questa proprietà alla [tabella Property e](property-table.md) ne imposta il valore. Il programma di installazione scrive quindi il valore **di PATCHNEWSUMMARYCOMMENTS** nella [**proprietà Revision Number Summary.**](revision-number-summary.md)

## <a name="remarks"></a>Commenti

Le [**proprietà PATCHNEWPACKAGECODE**](patchnewpackagecode.md), **PATCHNEWSUMMARYCOMMENTS** e [**PATCHNEWSUMMARYSUBJECT**](patchnewsummarysubject.md) vengono usate per aggiornare le informazioni di riepilogo quando viene installata una patch in un'immagine amministrativa.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Vedere i [Windows di installazione Run-Time](windows-installer-portal.md) per informazioni sul Service Pack Windows minimo richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




