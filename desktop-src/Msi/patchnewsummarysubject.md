---
description: La proprietà PATCHNEWSUMMARYSUBJECT aggiorna la proprietà Subject Summary di un'immagine amministrativa durante l'applicazione di patch.
ms.assetid: 8aee1905-59a4-4818-b073-4bc401a6963d
title: PatchNEWSUMMARYSUBJECT - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 912fe9ea21605625135b385a400fd5136c993c1d0dd0e3bfadd6a2b6699d21e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926169"
---
# <a name="patchnewsummarysubject-property"></a>PatchNEWSUMMARYSUBJECT - proprietà

La **proprietà PATCHNEWSUMMARYSUBJECT** aggiorna la proprietà [**Subject Summary**](subject-summary.md) di un'immagine amministrativa durante l'applicazione di patch. Questa proprietà viene impostata solo da una trasformazione in un file msp. Il file msp deve includere una trasformazione che aggiunge questa proprietà alla [tabella Property e](property-table.md) ne imposta il valore. Il programma di installazione scrive quindi il valore **di PATCHNEWSUMMARYSUBJECT** nella [**proprietà Revision Number Summary.**](revision-number-summary.md)

## <a name="remarks"></a>Commenti

Le [**proprietà PATCHNEWPACKAGECODE**](patchnewpackagecode.md), [**PATCHNEWSUMMARYCOMMENTS**](patchnewsummarycomments.md)e **PATCHNEWSUMMARYSUBJECT** vengono usate per aggiornare le informazioni di riepilogo quando viene installata una patch in un'immagine amministrativa.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Vedere i [Windows di installazione Run-Time](windows-installer-portal.md) per informazioni sul Service Pack Windows minimo richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




